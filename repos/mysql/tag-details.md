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
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:a3dff78d876222746a0bacc36dd7e4bf9e673c85fb7ee0d12ed25bd32c43c19b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:b78f5d6aafa5dc34a3059dca6ee713d7f083f07a198a8f68fc01a14d678bc201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3197d59eb3b270cf21bc1166fa726f9c511438416b421504068301df90c3172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:39:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8814198b348b66d583fd7eab3c27ed9fd2edf3fe5844c12a56c94230e59510fd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644bff8d1583288ae12fe4c4761b7fc6e1d148d9d4b2b7fcc2d2984dc85696a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2a1b215567315cfdf7dcea1347592fc81e54aac13227186b35d5cd12b5f6a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 6.2 MB (6171337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aee539d1d907fe1d21a43ed53f8daee7ee52f5fbfca20e9725fc21bca2d361b`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1b3148b2fad8250bce5821f4575dd76393968e0aac18bcccbea74175707d4`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b535e661c2b536f703dbb410389514e949c4b68a4a74c7b1c1804c1bbe6502`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 49.9 MB (49918729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e72585209f459a999b3a7f73317cc541ffa8721adf4a0b06f9ad33545489e0`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b38f497959225271d3c779fdf8a21adbb2c05020b27816d98872b41cf5c42d9`  
		Last Modified: Thu, 19 Feb 2026 19:39:47 GMT  
		Size: 128.1 MB (128098546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b08b5b90553f7dea17f1fff6a39bf88a13e0e266afcb7af388de5a526ab2cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b381ad27e95d68690db72792d0fce61f952ad2dc7e2cc86607ada9de63e97c2`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3559243fd98926e1a82257d1f4d965992aab2ade91371b92fe38d99a1cf603a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3833b6d77fc33c7add63d663c6f10b0bdfc987b3bc3eefcc225d64baf0d2e9b`

```dockerfile
```

-	Layers:
	-	`sha256:876a2cf55ca350df3b05936144da022805c4d7068971f6a36e6d5b3a02e2decd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 15.0 MB (14957519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b98dc30f5d0c251b6930a2d32c7572d1184a915a92b4f7a19775b5da6597784`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:24f018298bcbfff3770904820c23f6db7d5033b1415b234a229310f4dff5e1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb5f28655d7ad1807d26bb50bacb76a54095b3de822dd2f3ddd9b24e72e463`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f24742a9fbbcd1c84449b17cd44dcfd6a8eacab5c2ecedfc31d492e6baae4bf`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d57483dd938574daf05a0f780eee5081b8a1f26709a433d4b042970f51b6a2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70153b20ac4709fdbb0cf37c35ca71d5ddc83bb0641f3c1ccd7f5eb7ee0fc245`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 5.8 MB (5792781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ab58c394ba9b7ae18289771dfa437939f58c7a5965fa2d30d97dae6bbce31b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acfead654c5bb7e9066ad8410ab01d9cdf3f58182d1be417dec1d1981b9b74`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28899343ee2a0b46a80775326257208473edcf6d7a954248c1681f59149a0035`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 48.8 MB (48776902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307de4f40b805e8a179cf3ff0b13267272c19a5b7a5ab53b3ab81173b97a8e88`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2daf384b8610ca57bfabfebf923e59de7752a7fe3cbafa14b8991299cc39cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:31 GMT  
		Size: 126.7 MB (126683031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddffbe9ca7048b17d7cbfe8c813ec8db2e0ad4b66df4a3f445c40145ecba76e5`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463732daebc0c995a2155cade1c43c5b16e97a6eb09ceddd51de2aa2d8eb5fd4`  
		Last Modified: Thu, 19 Feb 2026 19:39:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:407521dab2442ecb468e479a574fd9aad05a632f828f3f40d47edf185a80ca90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6317c6b8f183daab9b5e16320d0d0fa8083f3bbaae1911fc95a6dcf01b89cb4`

```dockerfile
```

-	Layers:
	-	`sha256:a68a098ceb2397fc684b9a178ac53683aa42b68b0da56a6799ec720e9c964499`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 15.0 MB (14955867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe13821ce42ded98cbe2703fd1ba00a16a3475989fd1bf9660a60cf4f9fee6bd`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:1ae7ba07e714856c61aa0d559a8f1a788eb8f25bd0b5b71738a1bdd6798bc022
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:6e36c730c6f33608f4111ee753ccf77a80ce8a0972c1acecefdc136210912ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d49db580cdf0a4d4d0defed1cc6ea4cb679d73e66336f060cd31adaa9201fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 24 Feb 2026 19:24:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 19:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:24:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Feb 2026 19:24:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 24 Feb 2026 19:24:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Feb 2026 19:24:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Feb 2026 19:24:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657e91376c7d5da431965d4b812f1693a459c30acf08b2a96e7c443aa7343c7e`  
		Last Modified: Tue, 24 Feb 2026 19:25:15 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d231f1c991d4752b66c9d2ef772da83b4d8dd7f4cfdd3e9e9d4cf94d5f6e657a`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 4.4 MB (4423382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d061d7ccd461e2167ef1482c381b785c6bdd04068cb34b755a5e88b0fc171e`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 1.2 MB (1248716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa2c3ae56c89301373a9bb40694f30b56d7e507f5202572e8bddbf2b12a3705`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e0ff956f5a06808e9f26016ccb153f26315964e2c0e53b711ba032b2751c4`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 15.3 MB (15295914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67727143d2c41a51bc9411b9beb2a69c499c2a414f7e4477d9cf1a7555fdcb6b`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e16ee554bcd8e804fff0befd89f54c880175ce69bb0d67d5e34c3fda2b045e`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466a5d223e9732813556f9208263c4160cd5a24c05c679650d52040d1e5c9f3b`  
		Last Modified: Tue, 24 Feb 2026 19:25:20 GMT  
		Size: 134.2 MB (134249415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bd41ee2f07ae7ee50edd2b36ac75b0ffbf507ea5c3e77740f511f79272da58`  
		Last Modified: Tue, 24 Feb 2026 19:25:18 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3dd23b42d1465cff0c705238dc1b1470107fa8a913101d21ce7b475a0ed74c`  
		Last Modified: Tue, 24 Feb 2026 19:25:18 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bddcc0d82ed376f6ee4fbb71cb81a1b52c4fa76a8c6e45b3b02d53b4754bb5d`  
		Last Modified: Tue, 24 Feb 2026 19:25:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:eb4315b039a8d75a1622faec9647ccbe215d056dfcc3ddbca01f033815e325c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54e2b4dd2fbd06132b4b1ce0d79a30d4a1bfd694468bdda120cf8a1076f845`

```dockerfile
```

-	Layers:
	-	`sha256:17a928d99d27680c27913a03b9f38590f7ac2fd43403b50d0bb123b70a7df4f3`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb212ff3a80a156523a32078970d6651799772a0a8d1531e432cd58ad7db232`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:1ae7ba07e714856c61aa0d559a8f1a788eb8f25bd0b5b71738a1bdd6798bc022
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:6e36c730c6f33608f4111ee753ccf77a80ce8a0972c1acecefdc136210912ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d49db580cdf0a4d4d0defed1cc6ea4cb679d73e66336f060cd31adaa9201fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 24 Feb 2026 19:24:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 19:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:24:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Feb 2026 19:24:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 24 Feb 2026 19:24:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Feb 2026 19:24:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Feb 2026 19:24:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657e91376c7d5da431965d4b812f1693a459c30acf08b2a96e7c443aa7343c7e`  
		Last Modified: Tue, 24 Feb 2026 19:25:15 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d231f1c991d4752b66c9d2ef772da83b4d8dd7f4cfdd3e9e9d4cf94d5f6e657a`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 4.4 MB (4423382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d061d7ccd461e2167ef1482c381b785c6bdd04068cb34b755a5e88b0fc171e`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 1.2 MB (1248716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa2c3ae56c89301373a9bb40694f30b56d7e507f5202572e8bddbf2b12a3705`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e0ff956f5a06808e9f26016ccb153f26315964e2c0e53b711ba032b2751c4`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 15.3 MB (15295914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67727143d2c41a51bc9411b9beb2a69c499c2a414f7e4477d9cf1a7555fdcb6b`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e16ee554bcd8e804fff0befd89f54c880175ce69bb0d67d5e34c3fda2b045e`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466a5d223e9732813556f9208263c4160cd5a24c05c679650d52040d1e5c9f3b`  
		Last Modified: Tue, 24 Feb 2026 19:25:20 GMT  
		Size: 134.2 MB (134249415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bd41ee2f07ae7ee50edd2b36ac75b0ffbf507ea5c3e77740f511f79272da58`  
		Last Modified: Tue, 24 Feb 2026 19:25:18 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3dd23b42d1465cff0c705238dc1b1470107fa8a913101d21ce7b475a0ed74c`  
		Last Modified: Tue, 24 Feb 2026 19:25:18 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bddcc0d82ed376f6ee4fbb71cb81a1b52c4fa76a8c6e45b3b02d53b4754bb5d`  
		Last Modified: Tue, 24 Feb 2026 19:25:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:eb4315b039a8d75a1622faec9647ccbe215d056dfcc3ddbca01f033815e325c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54e2b4dd2fbd06132b4b1ce0d79a30d4a1bfd694468bdda120cf8a1076f845`

```dockerfile
```

-	Layers:
	-	`sha256:17a928d99d27680c27913a03b9f38590f7ac2fd43403b50d0bb123b70a7df4f3`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb212ff3a80a156523a32078970d6651799772a0a8d1531e432cd58ad7db232`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:a3dff78d876222746a0bacc36dd7e4bf9e673c85fb7ee0d12ed25bd32c43c19b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b78f5d6aafa5dc34a3059dca6ee713d7f083f07a198a8f68fc01a14d678bc201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3197d59eb3b270cf21bc1166fa726f9c511438416b421504068301df90c3172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:39:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8814198b348b66d583fd7eab3c27ed9fd2edf3fe5844c12a56c94230e59510fd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644bff8d1583288ae12fe4c4761b7fc6e1d148d9d4b2b7fcc2d2984dc85696a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2a1b215567315cfdf7dcea1347592fc81e54aac13227186b35d5cd12b5f6a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 6.2 MB (6171337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aee539d1d907fe1d21a43ed53f8daee7ee52f5fbfca20e9725fc21bca2d361b`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1b3148b2fad8250bce5821f4575dd76393968e0aac18bcccbea74175707d4`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b535e661c2b536f703dbb410389514e949c4b68a4a74c7b1c1804c1bbe6502`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 49.9 MB (49918729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e72585209f459a999b3a7f73317cc541ffa8721adf4a0b06f9ad33545489e0`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b38f497959225271d3c779fdf8a21adbb2c05020b27816d98872b41cf5c42d9`  
		Last Modified: Thu, 19 Feb 2026 19:39:47 GMT  
		Size: 128.1 MB (128098546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b08b5b90553f7dea17f1fff6a39bf88a13e0e266afcb7af388de5a526ab2cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b381ad27e95d68690db72792d0fce61f952ad2dc7e2cc86607ada9de63e97c2`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3559243fd98926e1a82257d1f4d965992aab2ade91371b92fe38d99a1cf603a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3833b6d77fc33c7add63d663c6f10b0bdfc987b3bc3eefcc225d64baf0d2e9b`

```dockerfile
```

-	Layers:
	-	`sha256:876a2cf55ca350df3b05936144da022805c4d7068971f6a36e6d5b3a02e2decd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 15.0 MB (14957519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b98dc30f5d0c251b6930a2d32c7572d1184a915a92b4f7a19775b5da6597784`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:24f018298bcbfff3770904820c23f6db7d5033b1415b234a229310f4dff5e1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb5f28655d7ad1807d26bb50bacb76a54095b3de822dd2f3ddd9b24e72e463`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f24742a9fbbcd1c84449b17cd44dcfd6a8eacab5c2ecedfc31d492e6baae4bf`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d57483dd938574daf05a0f780eee5081b8a1f26709a433d4b042970f51b6a2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70153b20ac4709fdbb0cf37c35ca71d5ddc83bb0641f3c1ccd7f5eb7ee0fc245`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 5.8 MB (5792781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ab58c394ba9b7ae18289771dfa437939f58c7a5965fa2d30d97dae6bbce31b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acfead654c5bb7e9066ad8410ab01d9cdf3f58182d1be417dec1d1981b9b74`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28899343ee2a0b46a80775326257208473edcf6d7a954248c1681f59149a0035`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 48.8 MB (48776902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307de4f40b805e8a179cf3ff0b13267272c19a5b7a5ab53b3ab81173b97a8e88`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2daf384b8610ca57bfabfebf923e59de7752a7fe3cbafa14b8991299cc39cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:31 GMT  
		Size: 126.7 MB (126683031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddffbe9ca7048b17d7cbfe8c813ec8db2e0ad4b66df4a3f445c40145ecba76e5`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463732daebc0c995a2155cade1c43c5b16e97a6eb09ceddd51de2aa2d8eb5fd4`  
		Last Modified: Thu, 19 Feb 2026 19:39:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:407521dab2442ecb468e479a574fd9aad05a632f828f3f40d47edf185a80ca90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6317c6b8f183daab9b5e16320d0d0fa8083f3bbaae1911fc95a6dcf01b89cb4`

```dockerfile
```

-	Layers:
	-	`sha256:a68a098ceb2397fc684b9a178ac53683aa42b68b0da56a6799ec720e9c964499`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 15.0 MB (14955867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe13821ce42ded98cbe2703fd1ba00a16a3475989fd1bf9660a60cf4f9fee6bd`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:a3dff78d876222746a0bacc36dd7e4bf9e673c85fb7ee0d12ed25bd32c43c19b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b78f5d6aafa5dc34a3059dca6ee713d7f083f07a198a8f68fc01a14d678bc201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3197d59eb3b270cf21bc1166fa726f9c511438416b421504068301df90c3172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:39:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8814198b348b66d583fd7eab3c27ed9fd2edf3fe5844c12a56c94230e59510fd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644bff8d1583288ae12fe4c4761b7fc6e1d148d9d4b2b7fcc2d2984dc85696a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2a1b215567315cfdf7dcea1347592fc81e54aac13227186b35d5cd12b5f6a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 6.2 MB (6171337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aee539d1d907fe1d21a43ed53f8daee7ee52f5fbfca20e9725fc21bca2d361b`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1b3148b2fad8250bce5821f4575dd76393968e0aac18bcccbea74175707d4`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b535e661c2b536f703dbb410389514e949c4b68a4a74c7b1c1804c1bbe6502`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 49.9 MB (49918729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e72585209f459a999b3a7f73317cc541ffa8721adf4a0b06f9ad33545489e0`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b38f497959225271d3c779fdf8a21adbb2c05020b27816d98872b41cf5c42d9`  
		Last Modified: Thu, 19 Feb 2026 19:39:47 GMT  
		Size: 128.1 MB (128098546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b08b5b90553f7dea17f1fff6a39bf88a13e0e266afcb7af388de5a526ab2cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b381ad27e95d68690db72792d0fce61f952ad2dc7e2cc86607ada9de63e97c2`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3559243fd98926e1a82257d1f4d965992aab2ade91371b92fe38d99a1cf603a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3833b6d77fc33c7add63d663c6f10b0bdfc987b3bc3eefcc225d64baf0d2e9b`

```dockerfile
```

-	Layers:
	-	`sha256:876a2cf55ca350df3b05936144da022805c4d7068971f6a36e6d5b3a02e2decd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 15.0 MB (14957519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b98dc30f5d0c251b6930a2d32c7572d1184a915a92b4f7a19775b5da6597784`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:24f018298bcbfff3770904820c23f6db7d5033b1415b234a229310f4dff5e1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb5f28655d7ad1807d26bb50bacb76a54095b3de822dd2f3ddd9b24e72e463`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f24742a9fbbcd1c84449b17cd44dcfd6a8eacab5c2ecedfc31d492e6baae4bf`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d57483dd938574daf05a0f780eee5081b8a1f26709a433d4b042970f51b6a2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70153b20ac4709fdbb0cf37c35ca71d5ddc83bb0641f3c1ccd7f5eb7ee0fc245`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 5.8 MB (5792781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ab58c394ba9b7ae18289771dfa437939f58c7a5965fa2d30d97dae6bbce31b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acfead654c5bb7e9066ad8410ab01d9cdf3f58182d1be417dec1d1981b9b74`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28899343ee2a0b46a80775326257208473edcf6d7a954248c1681f59149a0035`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 48.8 MB (48776902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307de4f40b805e8a179cf3ff0b13267272c19a5b7a5ab53b3ab81173b97a8e88`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2daf384b8610ca57bfabfebf923e59de7752a7fe3cbafa14b8991299cc39cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:31 GMT  
		Size: 126.7 MB (126683031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddffbe9ca7048b17d7cbfe8c813ec8db2e0ad4b66df4a3f445c40145ecba76e5`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463732daebc0c995a2155cade1c43c5b16e97a6eb09ceddd51de2aa2d8eb5fd4`  
		Last Modified: Thu, 19 Feb 2026 19:39:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:407521dab2442ecb468e479a574fd9aad05a632f828f3f40d47edf185a80ca90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6317c6b8f183daab9b5e16320d0d0fa8083f3bbaae1911fc95a6dcf01b89cb4`

```dockerfile
```

-	Layers:
	-	`sha256:a68a098ceb2397fc684b9a178ac53683aa42b68b0da56a6799ec720e9c964499`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 15.0 MB (14955867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe13821ce42ded98cbe2703fd1ba00a16a3475989fd1bf9660a60cf4f9fee6bd`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45`

```console
$ docker pull mysql@sha256:a3dff78d876222746a0bacc36dd7e4bf9e673c85fb7ee0d12ed25bd32c43c19b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45` - linux; amd64

```console
$ docker pull mysql@sha256:b78f5d6aafa5dc34a3059dca6ee713d7f083f07a198a8f68fc01a14d678bc201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3197d59eb3b270cf21bc1166fa726f9c511438416b421504068301df90c3172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:39:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8814198b348b66d583fd7eab3c27ed9fd2edf3fe5844c12a56c94230e59510fd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644bff8d1583288ae12fe4c4761b7fc6e1d148d9d4b2b7fcc2d2984dc85696a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2a1b215567315cfdf7dcea1347592fc81e54aac13227186b35d5cd12b5f6a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 6.2 MB (6171337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aee539d1d907fe1d21a43ed53f8daee7ee52f5fbfca20e9725fc21bca2d361b`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1b3148b2fad8250bce5821f4575dd76393968e0aac18bcccbea74175707d4`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b535e661c2b536f703dbb410389514e949c4b68a4a74c7b1c1804c1bbe6502`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 49.9 MB (49918729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e72585209f459a999b3a7f73317cc541ffa8721adf4a0b06f9ad33545489e0`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b38f497959225271d3c779fdf8a21adbb2c05020b27816d98872b41cf5c42d9`  
		Last Modified: Thu, 19 Feb 2026 19:39:47 GMT  
		Size: 128.1 MB (128098546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b08b5b90553f7dea17f1fff6a39bf88a13e0e266afcb7af388de5a526ab2cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b381ad27e95d68690db72792d0fce61f952ad2dc7e2cc86607ada9de63e97c2`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:3559243fd98926e1a82257d1f4d965992aab2ade91371b92fe38d99a1cf603a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3833b6d77fc33c7add63d663c6f10b0bdfc987b3bc3eefcc225d64baf0d2e9b`

```dockerfile
```

-	Layers:
	-	`sha256:876a2cf55ca350df3b05936144da022805c4d7068971f6a36e6d5b3a02e2decd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 15.0 MB (14957519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b98dc30f5d0c251b6930a2d32c7572d1184a915a92b4f7a19775b5da6597784`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:24f018298bcbfff3770904820c23f6db7d5033b1415b234a229310f4dff5e1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb5f28655d7ad1807d26bb50bacb76a54095b3de822dd2f3ddd9b24e72e463`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f24742a9fbbcd1c84449b17cd44dcfd6a8eacab5c2ecedfc31d492e6baae4bf`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d57483dd938574daf05a0f780eee5081b8a1f26709a433d4b042970f51b6a2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70153b20ac4709fdbb0cf37c35ca71d5ddc83bb0641f3c1ccd7f5eb7ee0fc245`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 5.8 MB (5792781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ab58c394ba9b7ae18289771dfa437939f58c7a5965fa2d30d97dae6bbce31b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acfead654c5bb7e9066ad8410ab01d9cdf3f58182d1be417dec1d1981b9b74`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28899343ee2a0b46a80775326257208473edcf6d7a954248c1681f59149a0035`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 48.8 MB (48776902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307de4f40b805e8a179cf3ff0b13267272c19a5b7a5ab53b3ab81173b97a8e88`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2daf384b8610ca57bfabfebf923e59de7752a7fe3cbafa14b8991299cc39cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:31 GMT  
		Size: 126.7 MB (126683031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddffbe9ca7048b17d7cbfe8c813ec8db2e0ad4b66df4a3f445c40145ecba76e5`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463732daebc0c995a2155cade1c43c5b16e97a6eb09ceddd51de2aa2d8eb5fd4`  
		Last Modified: Thu, 19 Feb 2026 19:39:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:407521dab2442ecb468e479a574fd9aad05a632f828f3f40d47edf185a80ca90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6317c6b8f183daab9b5e16320d0d0fa8083f3bbaae1911fc95a6dcf01b89cb4`

```dockerfile
```

-	Layers:
	-	`sha256:a68a098ceb2397fc684b9a178ac53683aa42b68b0da56a6799ec720e9c964499`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 15.0 MB (14955867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe13821ce42ded98cbe2703fd1ba00a16a3475989fd1bf9660a60cf4f9fee6bd`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-bookworm`

```console
$ docker pull mysql@sha256:1ae7ba07e714856c61aa0d559a8f1a788eb8f25bd0b5b71738a1bdd6798bc022
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:6e36c730c6f33608f4111ee753ccf77a80ce8a0972c1acecefdc136210912ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d49db580cdf0a4d4d0defed1cc6ea4cb679d73e66336f060cd31adaa9201fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 24 Feb 2026 19:24:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 19:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:24:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Feb 2026 19:24:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 24 Feb 2026 19:24:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Feb 2026 19:24:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Feb 2026 19:24:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657e91376c7d5da431965d4b812f1693a459c30acf08b2a96e7c443aa7343c7e`  
		Last Modified: Tue, 24 Feb 2026 19:25:15 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d231f1c991d4752b66c9d2ef772da83b4d8dd7f4cfdd3e9e9d4cf94d5f6e657a`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 4.4 MB (4423382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d061d7ccd461e2167ef1482c381b785c6bdd04068cb34b755a5e88b0fc171e`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 1.2 MB (1248716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa2c3ae56c89301373a9bb40694f30b56d7e507f5202572e8bddbf2b12a3705`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e0ff956f5a06808e9f26016ccb153f26315964e2c0e53b711ba032b2751c4`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 15.3 MB (15295914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67727143d2c41a51bc9411b9beb2a69c499c2a414f7e4477d9cf1a7555fdcb6b`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e16ee554bcd8e804fff0befd89f54c880175ce69bb0d67d5e34c3fda2b045e`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466a5d223e9732813556f9208263c4160cd5a24c05c679650d52040d1e5c9f3b`  
		Last Modified: Tue, 24 Feb 2026 19:25:20 GMT  
		Size: 134.2 MB (134249415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bd41ee2f07ae7ee50edd2b36ac75b0ffbf507ea5c3e77740f511f79272da58`  
		Last Modified: Tue, 24 Feb 2026 19:25:18 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3dd23b42d1465cff0c705238dc1b1470107fa8a913101d21ce7b475a0ed74c`  
		Last Modified: Tue, 24 Feb 2026 19:25:18 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bddcc0d82ed376f6ee4fbb71cb81a1b52c4fa76a8c6e45b3b02d53b4754bb5d`  
		Last Modified: Tue, 24 Feb 2026 19:25:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:eb4315b039a8d75a1622faec9647ccbe215d056dfcc3ddbca01f033815e325c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54e2b4dd2fbd06132b4b1ce0d79a30d4a1bfd694468bdda120cf8a1076f845`

```dockerfile
```

-	Layers:
	-	`sha256:17a928d99d27680c27913a03b9f38590f7ac2fd43403b50d0bb123b70a7df4f3`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb212ff3a80a156523a32078970d6651799772a0a8d1531e432cd58ad7db232`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-debian`

```console
$ docker pull mysql@sha256:1ae7ba07e714856c61aa0d559a8f1a788eb8f25bd0b5b71738a1bdd6798bc022
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-debian` - linux; amd64

```console
$ docker pull mysql@sha256:6e36c730c6f33608f4111ee753ccf77a80ce8a0972c1acecefdc136210912ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d49db580cdf0a4d4d0defed1cc6ea4cb679d73e66336f060cd31adaa9201fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 24 Feb 2026 19:24:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 19:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:24:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 24 Feb 2026 19:24:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 24 Feb 2026 19:24:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 Feb 2026 19:24:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 24 Feb 2026 19:24:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657e91376c7d5da431965d4b812f1693a459c30acf08b2a96e7c443aa7343c7e`  
		Last Modified: Tue, 24 Feb 2026 19:25:15 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d231f1c991d4752b66c9d2ef772da83b4d8dd7f4cfdd3e9e9d4cf94d5f6e657a`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 4.4 MB (4423382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d061d7ccd461e2167ef1482c381b785c6bdd04068cb34b755a5e88b0fc171e`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 1.2 MB (1248716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa2c3ae56c89301373a9bb40694f30b56d7e507f5202572e8bddbf2b12a3705`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e0ff956f5a06808e9f26016ccb153f26315964e2c0e53b711ba032b2751c4`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 15.3 MB (15295914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67727143d2c41a51bc9411b9beb2a69c499c2a414f7e4477d9cf1a7555fdcb6b`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e16ee554bcd8e804fff0befd89f54c880175ce69bb0d67d5e34c3fda2b045e`  
		Last Modified: Tue, 24 Feb 2026 19:25:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466a5d223e9732813556f9208263c4160cd5a24c05c679650d52040d1e5c9f3b`  
		Last Modified: Tue, 24 Feb 2026 19:25:20 GMT  
		Size: 134.2 MB (134249415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bd41ee2f07ae7ee50edd2b36ac75b0ffbf507ea5c3e77740f511f79272da58`  
		Last Modified: Tue, 24 Feb 2026 19:25:18 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3dd23b42d1465cff0c705238dc1b1470107fa8a913101d21ce7b475a0ed74c`  
		Last Modified: Tue, 24 Feb 2026 19:25:18 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bddcc0d82ed376f6ee4fbb71cb81a1b52c4fa76a8c6e45b3b02d53b4754bb5d`  
		Last Modified: Tue, 24 Feb 2026 19:25:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:eb4315b039a8d75a1622faec9647ccbe215d056dfcc3ddbca01f033815e325c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54e2b4dd2fbd06132b4b1ce0d79a30d4a1bfd694468bdda120cf8a1076f845`

```dockerfile
```

-	Layers:
	-	`sha256:17a928d99d27680c27913a03b9f38590f7ac2fd43403b50d0bb123b70a7df4f3`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb212ff3a80a156523a32078970d6651799772a0a8d1531e432cd58ad7db232`  
		Last Modified: Tue, 24 Feb 2026 19:25:16 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oracle`

```console
$ docker pull mysql@sha256:a3dff78d876222746a0bacc36dd7e4bf9e673c85fb7ee0d12ed25bd32c43c19b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b78f5d6aafa5dc34a3059dca6ee713d7f083f07a198a8f68fc01a14d678bc201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3197d59eb3b270cf21bc1166fa726f9c511438416b421504068301df90c3172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:39:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8814198b348b66d583fd7eab3c27ed9fd2edf3fe5844c12a56c94230e59510fd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644bff8d1583288ae12fe4c4761b7fc6e1d148d9d4b2b7fcc2d2984dc85696a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2a1b215567315cfdf7dcea1347592fc81e54aac13227186b35d5cd12b5f6a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 6.2 MB (6171337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aee539d1d907fe1d21a43ed53f8daee7ee52f5fbfca20e9725fc21bca2d361b`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1b3148b2fad8250bce5821f4575dd76393968e0aac18bcccbea74175707d4`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b535e661c2b536f703dbb410389514e949c4b68a4a74c7b1c1804c1bbe6502`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 49.9 MB (49918729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e72585209f459a999b3a7f73317cc541ffa8721adf4a0b06f9ad33545489e0`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b38f497959225271d3c779fdf8a21adbb2c05020b27816d98872b41cf5c42d9`  
		Last Modified: Thu, 19 Feb 2026 19:39:47 GMT  
		Size: 128.1 MB (128098546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b08b5b90553f7dea17f1fff6a39bf88a13e0e266afcb7af388de5a526ab2cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b381ad27e95d68690db72792d0fce61f952ad2dc7e2cc86607ada9de63e97c2`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3559243fd98926e1a82257d1f4d965992aab2ade91371b92fe38d99a1cf603a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3833b6d77fc33c7add63d663c6f10b0bdfc987b3bc3eefcc225d64baf0d2e9b`

```dockerfile
```

-	Layers:
	-	`sha256:876a2cf55ca350df3b05936144da022805c4d7068971f6a36e6d5b3a02e2decd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 15.0 MB (14957519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b98dc30f5d0c251b6930a2d32c7572d1184a915a92b4f7a19775b5da6597784`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:24f018298bcbfff3770904820c23f6db7d5033b1415b234a229310f4dff5e1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb5f28655d7ad1807d26bb50bacb76a54095b3de822dd2f3ddd9b24e72e463`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f24742a9fbbcd1c84449b17cd44dcfd6a8eacab5c2ecedfc31d492e6baae4bf`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d57483dd938574daf05a0f780eee5081b8a1f26709a433d4b042970f51b6a2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70153b20ac4709fdbb0cf37c35ca71d5ddc83bb0641f3c1ccd7f5eb7ee0fc245`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 5.8 MB (5792781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ab58c394ba9b7ae18289771dfa437939f58c7a5965fa2d30d97dae6bbce31b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acfead654c5bb7e9066ad8410ab01d9cdf3f58182d1be417dec1d1981b9b74`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28899343ee2a0b46a80775326257208473edcf6d7a954248c1681f59149a0035`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 48.8 MB (48776902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307de4f40b805e8a179cf3ff0b13267272c19a5b7a5ab53b3ab81173b97a8e88`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2daf384b8610ca57bfabfebf923e59de7752a7fe3cbafa14b8991299cc39cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:31 GMT  
		Size: 126.7 MB (126683031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddffbe9ca7048b17d7cbfe8c813ec8db2e0ad4b66df4a3f445c40145ecba76e5`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463732daebc0c995a2155cade1c43c5b16e97a6eb09ceddd51de2aa2d8eb5fd4`  
		Last Modified: Thu, 19 Feb 2026 19:39:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:407521dab2442ecb468e479a574fd9aad05a632f828f3f40d47edf185a80ca90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6317c6b8f183daab9b5e16320d0d0fa8083f3bbaae1911fc95a6dcf01b89cb4`

```dockerfile
```

-	Layers:
	-	`sha256:a68a098ceb2397fc684b9a178ac53683aa42b68b0da56a6799ec720e9c964499`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 15.0 MB (14955867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe13821ce42ded98cbe2703fd1ba00a16a3475989fd1bf9660a60cf4f9fee6bd`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oraclelinux9`

```console
$ docker pull mysql@sha256:a3dff78d876222746a0bacc36dd7e4bf9e673c85fb7ee0d12ed25bd32c43c19b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b78f5d6aafa5dc34a3059dca6ee713d7f083f07a198a8f68fc01a14d678bc201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3197d59eb3b270cf21bc1166fa726f9c511438416b421504068301df90c3172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:38:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:39:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8814198b348b66d583fd7eab3c27ed9fd2edf3fe5844c12a56c94230e59510fd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644bff8d1583288ae12fe4c4761b7fc6e1d148d9d4b2b7fcc2d2984dc85696a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2a1b215567315cfdf7dcea1347592fc81e54aac13227186b35d5cd12b5f6a`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 6.2 MB (6171337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aee539d1d907fe1d21a43ed53f8daee7ee52f5fbfca20e9725fc21bca2d361b`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1b3148b2fad8250bce5821f4575dd76393968e0aac18bcccbea74175707d4`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b535e661c2b536f703dbb410389514e949c4b68a4a74c7b1c1804c1bbe6502`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 49.9 MB (49918729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e72585209f459a999b3a7f73317cc541ffa8721adf4a0b06f9ad33545489e0`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b38f497959225271d3c779fdf8a21adbb2c05020b27816d98872b41cf5c42d9`  
		Last Modified: Thu, 19 Feb 2026 19:39:47 GMT  
		Size: 128.1 MB (128098546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b08b5b90553f7dea17f1fff6a39bf88a13e0e266afcb7af388de5a526ab2cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b381ad27e95d68690db72792d0fce61f952ad2dc7e2cc86607ada9de63e97c2`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3559243fd98926e1a82257d1f4d965992aab2ade91371b92fe38d99a1cf603a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3833b6d77fc33c7add63d663c6f10b0bdfc987b3bc3eefcc225d64baf0d2e9b`

```dockerfile
```

-	Layers:
	-	`sha256:876a2cf55ca350df3b05936144da022805c4d7068971f6a36e6d5b3a02e2decd`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 15.0 MB (14957519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b98dc30f5d0c251b6930a2d32c7572d1184a915a92b4f7a19775b5da6597784`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.9 KB (34910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:24f018298bcbfff3770904820c23f6db7d5033b1415b234a229310f4dff5e1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227901809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb5f28655d7ad1807d26bb50bacb76a54095b3de822dd2f3ddd9b24e72e463`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 19 Feb 2026 19:37:48 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:37:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 19 Feb 2026 19:38:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 19 Feb 2026 19:38:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:56 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f24742a9fbbcd1c84449b17cd44dcfd6a8eacab5c2ecedfc31d492e6baae4bf`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d57483dd938574daf05a0f780eee5081b8a1f26709a433d4b042970f51b6a2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70153b20ac4709fdbb0cf37c35ca71d5ddc83bb0641f3c1ccd7f5eb7ee0fc245`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 5.8 MB (5792781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ab58c394ba9b7ae18289771dfa437939f58c7a5965fa2d30d97dae6bbce31b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acfead654c5bb7e9066ad8410ab01d9cdf3f58182d1be417dec1d1981b9b74`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28899343ee2a0b46a80775326257208473edcf6d7a954248c1681f59149a0035`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 48.8 MB (48776902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307de4f40b805e8a179cf3ff0b13267272c19a5b7a5ab53b3ab81173b97a8e88`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2daf384b8610ca57bfabfebf923e59de7752a7fe3cbafa14b8991299cc39cb`  
		Last Modified: Thu, 19 Feb 2026 19:39:31 GMT  
		Size: 126.7 MB (126683031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddffbe9ca7048b17d7cbfe8c813ec8db2e0ad4b66df4a3f445c40145ecba76e5`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463732daebc0c995a2155cade1c43c5b16e97a6eb09ceddd51de2aa2d8eb5fd4`  
		Last Modified: Thu, 19 Feb 2026 19:39:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:407521dab2442ecb468e479a574fd9aad05a632f828f3f40d47edf185a80ca90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6317c6b8f183daab9b5e16320d0d0fa8083f3bbaae1911fc95a6dcf01b89cb4`

```dockerfile
```

-	Layers:
	-	`sha256:a68a098ceb2397fc684b9a178ac53683aa42b68b0da56a6799ec720e9c964499`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 15.0 MB (14955867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe13821ce42ded98cbe2703fd1ba00a16a3475989fd1bf9660a60cf4f9fee6bd`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 35.2 KB (35158 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oracle`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oraclelinux9`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oracle`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oraclelinux9`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oracle`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oraclelinux9`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:a2d126916bc2ba79a890a4bf62d305eb8b68fcbdd35c6e582d529df18faf5ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:72d4a1ab89486060136f570bde157a7780510b281019cef1f038c69b50f0b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233214443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82da5e68017f97388f8473c413b0607268c90d9fc5c92a9341cd516465b58f2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:38:06 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:06 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:39:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:39:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:39:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7842d0a781825f609325052d3dc7fe76d2e2bfb117f3382cbadef649fcd2ba`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b1584540670a35fe144ba7252116b41d0b80da97f3083c5083c0c1b92b019`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf0818490adb22647727408b5b7588c739d5fdadca007b22f0ce5cc6add3054`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 6.2 MB (6171335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c4bee94635dc46c84fab356af4ac785339fb01d4faefaa34e1789c3d23869`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8166b6846f27d7b8caaa43fd5653f4a78a5e8a2a438e6df3a79485264fc1693a`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6c694e6c507ee3f28dd7c56bcff71582430388a5a7750989d60f7aa5b0c7`  
		Last Modified: Thu, 19 Feb 2026 19:39:45 GMT  
		Size: 47.8 MB (47810240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5d964ef58058c1ae1ea7d7ee4c07c41cf5cb2bddd466b9f82dc3003d99201`  
		Last Modified: Thu, 19 Feb 2026 19:39:43 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385f68403ef29cadae2a2cf4c2566f0635bed21dbcdc0a3d4aefc161608b7d`  
		Last Modified: Thu, 19 Feb 2026 19:39:48 GMT  
		Size: 131.1 MB (131130972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8ea0845622c72f41a61be72f07b49462827db8a1c71c6d654a0bbc57e8212`  
		Last Modified: Thu, 19 Feb 2026 19:39:44 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:091c2f5bbbe7fde5643b8e33321b6622aa90709763675d27f0154cdde0947306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99d63840e6f753e38e8e90cf78d87a10ad523036f067e5808a8988a3b9a8c2`

```dockerfile
```

-	Layers:
	-	`sha256:2e8fa795fe6d756e987177cacf7acf762073994da3ed3d6d860a5b5efbcc5c81`  
		Last Modified: Thu, 19 Feb 2026 19:39:42 GMT  
		Size: 15.2 MB (15234340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97cebb3fd50889d1e844fed2d83690b3380936d6736b3eabd9eaf41d651b01c`  
		Last Modified: Thu, 19 Feb 2026 19:39:41 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a235c5bbb7235534ceca86d0dff98977aa854dd5b2ee507745458343d80454e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b98c7f94ccd94b493df7c94d379a722e19aa723c0c032abe775b1cb1b0d2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:17 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:42 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 19 Feb 2026 19:37:43 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:37:44 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 19 Feb 2026 19:38:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d1d41554dd9a7a489713aebc6d3e2099e83f1e57ea36cd65f3e6712b1fd86`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764c66a9f3a04a41a045c59fc461b600a84b0c17947e8d9398f40dac82b636a`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035f2de66f9c91aff891ba0b3ff82353afb2c22d858be8bc51455c8be8a0fce`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 5.8 MB (5792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85058089b80e52b2e7062c3af3a59bdce40996e883105a3394ffbadb263a6bf1`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926a00aef03949e3b97d3661b6ba0f43a3cdfe56c3d058a379f3f477c112478`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cab89f03edd577a8357ca81fae5d156c002d8283c42b5ef598a607cdf70578`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 46.7 MB (46699396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e50382fb5082a0403cbf34fb951cae60934ae6143c288fd28a144e48ae8bd8`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb27ccd1ce5edf46c906602461c3f2442b40beb430848b05a3842df218873c`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 129.5 MB (129546764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acecd2012154cf2abffd5f7fb2ae10392b541103cca7ac78283236d2c916ea1`  
		Last Modified: Thu, 19 Feb 2026 19:39:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a76a956afdbe20037d13b489a37f14ce904df1eb5e4d31e9df97e869e0b98323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d567331525ff74db22130d8d498383dc9d27e08331c26ba5876dc3dd1dd107`

```dockerfile
```

-	Layers:
	-	`sha256:a83fda6b26d6dea821d7d7736700d01c20d603ad69874763723aa37e1ef56229`  
		Last Modified: Thu, 19 Feb 2026 19:39:22 GMT  
		Size: 15.2 MB (15232760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b37a5ad7be1a3ad61ae320b9adfbb4dad2d4c8927680b48b3d7e4d5e16bfaf`  
		Last Modified: Thu, 19 Feb 2026 19:39:21 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:e5dc14f6e01c3e577e669337d2855c6d1561b30d8ef2c592e63e4e8a9a52650a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:44863da28ccefbacc0817390374f157d99612524ccf040dbf52e2d290129428c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266351592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8458fdfc578c6ef25b5963fdb0d7d47b561cdc93f1e67826a1cc31539d848719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:06 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:31 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:37:59 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357926362d314c15074e78be1fc6125ece4b938ab22c995af2c6cbf694564f36`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3702ac323ca4b4a5a071e2ae941528845543a7211a183a09806473a419f188f`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 783.6 KB (783552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658630c937c6aba78179e310d10d81fce707e7aab34520d1d1d2d77a70140e16`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 6.2 MB (6171333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b8ea7282676d52b836255c511c66e977b08617454c8ae63474851072bde71`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61941d436e8836def171233c8ca41146bd571bd057325849e7087ecd9ea5268d`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a19cdad3be6179ef0bf444fb3e9bce7a86b08b342dc339a24adf595fcf85b`  
		Last Modified: Thu, 19 Feb 2026 19:39:20 GMT  
		Size: 51.4 MB (51447578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af5f73db53aaea769b2c834e4ef1cce55187c1d44dd88d25d5ea8ba24b57f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ff001dec9cd0b344d9b44c3d3667bd274812dd35085ce276eb7c126598f9`  
		Last Modified: Thu, 19 Feb 2026 19:39:23 GMT  
		Size: 160.6 MB (160630778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a629f1008ffcda024abd3cba6f861c2282351a610601906cf46227dbc4c865c`  
		Last Modified: Thu, 19 Feb 2026 19:39:19 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a1e4cd3dafb2c89e8f24124f547c08105d2438121a0e3ba5fe90a6fbb3796bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bc5533092aa88f72e701449f4152d4b4c75fe8461ac001ab8ccaa6a919a8`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8eadaef55a0f175e7161d8b1706166e4608aca2acd0cdb0205602ec5d445e`  
		Last Modified: Thu, 19 Feb 2026 19:39:17 GMT  
		Size: 16.3 MB (16297430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ef59b124f5af95b003f659049bb2137cba42edf186813ffe15edcb5a77d3`  
		Last Modified: Thu, 19 Feb 2026 19:39:16 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a0a8658e3ccc3896b4bd0a615d274265ab0f539a48513e76de47278324f4a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a63af4712748c241f6264839c36667b0c9cb0e844be014358eac92a2f86df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:36:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 19 Feb 2026 19:37:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 19 Feb 2026 19:37:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:37:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 19 Feb 2026 19:38:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 19 Feb 2026 19:38:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 19 Feb 2026 19:38:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:50 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 19 Feb 2026 19:38:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a428306dd22fae952c306042a1a41fce1d00460056c42c8c77df208706f843`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eb38f4a27725ef790ede472bc63c94ad3e5bf1fb54c902338142ce3f53a65`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c160561713a8c87e28dda3b96208206820b192537a3a59ad8b4d771fa687ab1`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 5.8 MB (5792729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f97373d3c563391adbf899f7251fd5b8c0a6daae2f4883a7fdafc0f5d1a5f`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b8d4eb10dbbbe8a4d652aaa13b7b6e7e0e0b360e9e1d095a1dc96f270738`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc933cc4ee94163664d86b613bb75fd92fc86719b73afddc16920263e78229`  
		Last Modified: Thu, 19 Feb 2026 19:39:29 GMT  
		Size: 50.1 MB (50085731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce375f62cb9f2ed25679d0123a9d93c17ba93685fb65052afd56597b3240a44b`  
		Last Modified: Thu, 19 Feb 2026 19:39:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dcafb16fe99a2464586804da48600e1e3f2e18f6607a8dba68823d1bd349c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:32 GMT  
		Size: 158.9 MB (158940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e076b063968237512e358c13c25c18db6a5ba5f2c24e6aa2c02c47b3aae517`  
		Last Modified: Thu, 19 Feb 2026 19:39:28 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:93848d21b90cc142e5371b59a5ebbac84989ceffecf8e4343a7a9167821588b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1fcfa3ee9e8835c2f1bf9fb2a231d1c648f4a860545d1a268f9a80e244727`

```dockerfile
```

-	Layers:
	-	`sha256:a0b4e61d41f8814321428307706f2c1657d8f4da504a7cb2a204e193c4f838f2`  
		Last Modified: Thu, 19 Feb 2026 19:39:26 GMT  
		Size: 16.3 MB (16295886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b97d0287a91e90c6eef35f70e220c8c6edc3633321e614bed6128c5b86dd1c`  
		Last Modified: Thu, 19 Feb 2026 19:39:25 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
