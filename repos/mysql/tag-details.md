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
$ docker pull mysql@sha256:17c90cde7cbe56a334e0513768adf67ee5b29491f17df765102134388d20fe0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:c296d65ee6ab3ce2f608c1d1b2bdd3c08b087a5834101d76a6db2e00875216cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236856592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa03bf950b7fca40d7e1cae1ed638fadbc63b679ff74f1efb7d626e4c042ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fd76abbeb40b742af6aea70a2a70b73d1bfebcbac90053f0b7afc6505d518`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559d1bfb3bdb6d611f5e6c1f759de333193229ccab1ba120cedb27bd59dd327`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 783.5 KB (783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2257dfd80e5f7f4d03e9de86ad0b2d16b4581f4806faf8f47cda3c2183f19`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17cf5ce963905fef25d94f1a8cab2790e69f8dc27dd25ecef15adc1c89719b3`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff1798e33ce31cc9052a2d9a2e52f0235890142d7e400fb45c99eeb1d0a47cc`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ce10052616570c2b3b5863801d011d502e83c4dc016a10baedfb575af1529`  
		Last Modified: Sat, 18 Oct 2025 00:13:24 GMT  
		Size: 47.8 MB (47786071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46b44d7c262c6d21ffc28f69f07a1099ab6c200b9143a5f6c19eaa2ef18787`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d610e0f99daba87a52dd89c5e749e34ac351618c3247d6c31e53b29747baaea8`  
		Last Modified: Sat, 18 Oct 2025 01:00:21 GMT  
		Size: 132.0 MB (131961222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cf40c4e15f5bc3f3b39c070a7840d54921e5cd5c63b9302daaf4d663eb18b`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:1852a1650dfd0228d1354e78cbac5cf9d15cf6ab1f4e4f72ca062113ee2bcbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6732224879892fa7d8f6ee7f25c94858ccc54919e942411918cc1948a00a91a3`

```dockerfile
```

-	Layers:
	-	`sha256:1a32a4104c592d2fb8ecf0eff3905c10054b60862ba74d5336429c99ccbb7141`  
		Last Modified: Sat, 18 Oct 2025 03:02:23 GMT  
		Size: 14.8 MB (14804934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c30447d861a7a5b639b99eedebb7201c763ae961977c0cef3c63e8211404ca`  
		Last Modified: Sat, 18 Oct 2025 03:02:24 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:17c90cde7cbe56a334e0513768adf67ee5b29491f17df765102134388d20fe0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c296d65ee6ab3ce2f608c1d1b2bdd3c08b087a5834101d76a6db2e00875216cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236856592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa03bf950b7fca40d7e1cae1ed638fadbc63b679ff74f1efb7d626e4c042ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fd76abbeb40b742af6aea70a2a70b73d1bfebcbac90053f0b7afc6505d518`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559d1bfb3bdb6d611f5e6c1f759de333193229ccab1ba120cedb27bd59dd327`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 783.5 KB (783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2257dfd80e5f7f4d03e9de86ad0b2d16b4581f4806faf8f47cda3c2183f19`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17cf5ce963905fef25d94f1a8cab2790e69f8dc27dd25ecef15adc1c89719b3`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff1798e33ce31cc9052a2d9a2e52f0235890142d7e400fb45c99eeb1d0a47cc`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ce10052616570c2b3b5863801d011d502e83c4dc016a10baedfb575af1529`  
		Last Modified: Sat, 18 Oct 2025 00:13:24 GMT  
		Size: 47.8 MB (47786071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46b44d7c262c6d21ffc28f69f07a1099ab6c200b9143a5f6c19eaa2ef18787`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d610e0f99daba87a52dd89c5e749e34ac351618c3247d6c31e53b29747baaea8`  
		Last Modified: Sat, 18 Oct 2025 01:00:21 GMT  
		Size: 132.0 MB (131961222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cf40c4e15f5bc3f3b39c070a7840d54921e5cd5c63b9302daaf4d663eb18b`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1852a1650dfd0228d1354e78cbac5cf9d15cf6ab1f4e4f72ca062113ee2bcbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6732224879892fa7d8f6ee7f25c94858ccc54919e942411918cc1948a00a91a3`

```dockerfile
```

-	Layers:
	-	`sha256:1a32a4104c592d2fb8ecf0eff3905c10054b60862ba74d5336429c99ccbb7141`  
		Last Modified: Sat, 18 Oct 2025 03:02:23 GMT  
		Size: 14.8 MB (14804934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c30447d861a7a5b639b99eedebb7201c763ae961977c0cef3c63e8211404ca`  
		Last Modified: Sat, 18 Oct 2025 03:02:24 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:17c90cde7cbe56a334e0513768adf67ee5b29491f17df765102134388d20fe0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c296d65ee6ab3ce2f608c1d1b2bdd3c08b087a5834101d76a6db2e00875216cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236856592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa03bf950b7fca40d7e1cae1ed638fadbc63b679ff74f1efb7d626e4c042ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fd76abbeb40b742af6aea70a2a70b73d1bfebcbac90053f0b7afc6505d518`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559d1bfb3bdb6d611f5e6c1f759de333193229ccab1ba120cedb27bd59dd327`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 783.5 KB (783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2257dfd80e5f7f4d03e9de86ad0b2d16b4581f4806faf8f47cda3c2183f19`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17cf5ce963905fef25d94f1a8cab2790e69f8dc27dd25ecef15adc1c89719b3`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff1798e33ce31cc9052a2d9a2e52f0235890142d7e400fb45c99eeb1d0a47cc`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ce10052616570c2b3b5863801d011d502e83c4dc016a10baedfb575af1529`  
		Last Modified: Sat, 18 Oct 2025 00:13:24 GMT  
		Size: 47.8 MB (47786071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46b44d7c262c6d21ffc28f69f07a1099ab6c200b9143a5f6c19eaa2ef18787`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d610e0f99daba87a52dd89c5e749e34ac351618c3247d6c31e53b29747baaea8`  
		Last Modified: Sat, 18 Oct 2025 01:00:21 GMT  
		Size: 132.0 MB (131961222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cf40c4e15f5bc3f3b39c070a7840d54921e5cd5c63b9302daaf4d663eb18b`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1852a1650dfd0228d1354e78cbac5cf9d15cf6ab1f4e4f72ca062113ee2bcbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6732224879892fa7d8f6ee7f25c94858ccc54919e942411918cc1948a00a91a3`

```dockerfile
```

-	Layers:
	-	`sha256:1a32a4104c592d2fb8ecf0eff3905c10054b60862ba74d5336429c99ccbb7141`  
		Last Modified: Sat, 18 Oct 2025 03:02:23 GMT  
		Size: 14.8 MB (14804934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c30447d861a7a5b639b99eedebb7201c763ae961977c0cef3c63e8211404ca`  
		Last Modified: Sat, 18 Oct 2025 03:02:24 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:20f1175efd1a9ead968e17dc54e0ee1582477f059592b2b1904894736becd925
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:902368b688a8aba1d9de3f59110e4b3cb1a5ea76d370c1c29fa64f724a110cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235870437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f51417dfdbf3f6c2434b2fff64530fba6e0f244c616cb62846faaaf18f65135`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b558e90d6fc975fa2a3f53fea4da93097ed99a881f1b1deb0fa402babe5a43b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015ed6adb6c4babaa64aca8599fbdb4961051bc2aa736754ff623179ee7b8126`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064123821702dc2bfea097496e07dd37de0f1f2fe1efedcbad96dad1737a879`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4221635d1cb8be70e7a3ed5f1d6a499f1880d16d4609d7b66d561ed28514f055`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41fa75920fa26cf9e535361ab9c99603fa046bd3c7f9168bb0bfbe1896a1e9e`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0c0d6464b62936f81dbfb49cceebacca53ebc40e3f27a58ff9b1deeb2cfacb`  
		Last Modified: Sat, 18 Oct 2025 00:13:23 GMT  
		Size: 49.8 MB (49835234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc0d02e80992b59ac2ece9a1689c8fda20cb6ddfe9038b1f209c348ef1cf49f`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c44f22ceaa6fefe0ad316cdbdc40330b810336461a0a1e147edda440f67ab`  
		Last Modified: Sat, 18 Oct 2025 03:02:39 GMT  
		Size: 128.9 MB (128925787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6768abefd521f255f4a35cc21173aeeac6822dff0861a46fc5a390617f85a509`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810776de36a8ac26c55c424d1434215c2bb5718f36289ce4b3286fa66663d4ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:e3a4ce0e81a844f3a1b82fd30c38776d9f3524bad2835d53628284398824bd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de15c3956b5aa0b213081193632b9587d02509be43a10466d50dac837ff23410`

```dockerfile
```

-	Layers:
	-	`sha256:44a88059b74ff32929db6b13476c5a1200e9c303908ad3b084baf0a29182cc5e`  
		Last Modified: Sat, 18 Oct 2025 03:02:35 GMT  
		Size: 14.5 MB (14528113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:749b722dd01d17eef59ea7d398f092c009a037087a5e411e23778de9852a5fc4`  
		Last Modified: Sat, 18 Oct 2025 03:02:36 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:bced38c0ca97bd00c8fbc877a019ff141f014608b0762e6e1978cc76e63f473f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:e57032a8a261c966eaf4f6e9496628a442c87ac633af69465b1c743bb5c11487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183363738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90603554f2e9fec103f1c118fe99e6ada833c172c8bcbcf81b2c9b403ddfd7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Tue, 23 Sep 2025 19:30:29 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.0.43-1debian12
# Tue, 23 Sep 2025 19:30:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7116db692c2d6a6bca4f6267b64bc88427acbf1890c3135821fd429d4c868b`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c784a6aa987f15bf3eb92024bc2ce23e04bd5adcd3b73f49e588747f2fc55ba0`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 4.4 MB (4423008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f240eb51eca211c492b1dcffd2e2878d794a80e8d33522cfb014d211b5e19fb`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 1.2 MB (1248673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ecadba8cdfb788ce9d2b969f978cdfdb922902097d9d1e2ed9a68a366638b9`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f14f0bce068fbef747e8f389d2ff704f27ec742d95bd99901c6cb3ec8ad7cb5`  
		Last Modified: Tue, 21 Oct 2025 01:45:39 GMT  
		Size: 15.3 MB (15294283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64545fcead137ddede1b3d5c552fc20d1f5ae25c03a55358657cb764d8b26f`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cfd4d2d3ffd74d5cf5c827d6dc452790cd818308fa0dce00b4c4c58bb4ea1a`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e9f8804b15885ad4165d6dce706cd5df740c09962feb25da13acc38b75a86c`  
		Last Modified: Tue, 21 Oct 2025 03:20:50 GMT  
		Size: 134.2 MB (134159190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788ca063ad9453372cd44673a2dc98cd2e96c32977827751d4963b41af723ef8`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de92fb75f3db0fcaeb5d8940c3b87ba92e4933f3a45cefa1024b47f518b4a4`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f411408fdf1e599d4071821452396bf109e032bf9c25ee4e2f6d2941c129bcbc`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:80d4df781f7e88cedf681a72477cccb8ec21a04bae35330f65894e6e3accecbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af71be371a0ee13d5981831c141323f8af216132965ebcbc6bb7945d9ea2c6d3`

```dockerfile
```

-	Layers:
	-	`sha256:acfadec0732510e347800cf734ba0e2f5e633e40f2410bcdcea4140b0538527c`  
		Last Modified: Tue, 21 Oct 2025 09:02:21 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22809225ba2a4343119907daa10a1e92c85b66f06dcc39d483249d40696d924d`  
		Last Modified: Tue, 21 Oct 2025 09:02:22 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:bced38c0ca97bd00c8fbc877a019ff141f014608b0762e6e1978cc76e63f473f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e57032a8a261c966eaf4f6e9496628a442c87ac633af69465b1c743bb5c11487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183363738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90603554f2e9fec103f1c118fe99e6ada833c172c8bcbcf81b2c9b403ddfd7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Tue, 23 Sep 2025 19:30:29 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.0.43-1debian12
# Tue, 23 Sep 2025 19:30:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7116db692c2d6a6bca4f6267b64bc88427acbf1890c3135821fd429d4c868b`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c784a6aa987f15bf3eb92024bc2ce23e04bd5adcd3b73f49e588747f2fc55ba0`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 4.4 MB (4423008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f240eb51eca211c492b1dcffd2e2878d794a80e8d33522cfb014d211b5e19fb`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 1.2 MB (1248673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ecadba8cdfb788ce9d2b969f978cdfdb922902097d9d1e2ed9a68a366638b9`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f14f0bce068fbef747e8f389d2ff704f27ec742d95bd99901c6cb3ec8ad7cb5`  
		Last Modified: Tue, 21 Oct 2025 01:45:39 GMT  
		Size: 15.3 MB (15294283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64545fcead137ddede1b3d5c552fc20d1f5ae25c03a55358657cb764d8b26f`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cfd4d2d3ffd74d5cf5c827d6dc452790cd818308fa0dce00b4c4c58bb4ea1a`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e9f8804b15885ad4165d6dce706cd5df740c09962feb25da13acc38b75a86c`  
		Last Modified: Tue, 21 Oct 2025 03:20:50 GMT  
		Size: 134.2 MB (134159190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788ca063ad9453372cd44673a2dc98cd2e96c32977827751d4963b41af723ef8`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de92fb75f3db0fcaeb5d8940c3b87ba92e4933f3a45cefa1024b47f518b4a4`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f411408fdf1e599d4071821452396bf109e032bf9c25ee4e2f6d2941c129bcbc`  
		Last Modified: Tue, 21 Oct 2025 01:45:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:80d4df781f7e88cedf681a72477cccb8ec21a04bae35330f65894e6e3accecbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af71be371a0ee13d5981831c141323f8af216132965ebcbc6bb7945d9ea2c6d3`

```dockerfile
```

-	Layers:
	-	`sha256:acfadec0732510e347800cf734ba0e2f5e633e40f2410bcdcea4140b0538527c`  
		Last Modified: Tue, 21 Oct 2025 09:02:21 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22809225ba2a4343119907daa10a1e92c85b66f06dcc39d483249d40696d924d`  
		Last Modified: Tue, 21 Oct 2025 09:02:22 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:20f1175efd1a9ead968e17dc54e0ee1582477f059592b2b1904894736becd925
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:902368b688a8aba1d9de3f59110e4b3cb1a5ea76d370c1c29fa64f724a110cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235870437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f51417dfdbf3f6c2434b2fff64530fba6e0f244c616cb62846faaaf18f65135`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b558e90d6fc975fa2a3f53fea4da93097ed99a881f1b1deb0fa402babe5a43b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015ed6adb6c4babaa64aca8599fbdb4961051bc2aa736754ff623179ee7b8126`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064123821702dc2bfea097496e07dd37de0f1f2fe1efedcbad96dad1737a879`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4221635d1cb8be70e7a3ed5f1d6a499f1880d16d4609d7b66d561ed28514f055`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41fa75920fa26cf9e535361ab9c99603fa046bd3c7f9168bb0bfbe1896a1e9e`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0c0d6464b62936f81dbfb49cceebacca53ebc40e3f27a58ff9b1deeb2cfacb`  
		Last Modified: Sat, 18 Oct 2025 00:13:23 GMT  
		Size: 49.8 MB (49835234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc0d02e80992b59ac2ece9a1689c8fda20cb6ddfe9038b1f209c348ef1cf49f`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c44f22ceaa6fefe0ad316cdbdc40330b810336461a0a1e147edda440f67ab`  
		Last Modified: Sat, 18 Oct 2025 03:02:39 GMT  
		Size: 128.9 MB (128925787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6768abefd521f255f4a35cc21173aeeac6822dff0861a46fc5a390617f85a509`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810776de36a8ac26c55c424d1434215c2bb5718f36289ce4b3286fa66663d4ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e3a4ce0e81a844f3a1b82fd30c38776d9f3524bad2835d53628284398824bd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de15c3956b5aa0b213081193632b9587d02509be43a10466d50dac837ff23410`

```dockerfile
```

-	Layers:
	-	`sha256:44a88059b74ff32929db6b13476c5a1200e9c303908ad3b084baf0a29182cc5e`  
		Last Modified: Sat, 18 Oct 2025 03:02:35 GMT  
		Size: 14.5 MB (14528113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:749b722dd01d17eef59ea7d398f092c009a037087a5e411e23778de9852a5fc4`  
		Last Modified: Sat, 18 Oct 2025 03:02:36 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:20f1175efd1a9ead968e17dc54e0ee1582477f059592b2b1904894736becd925
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:902368b688a8aba1d9de3f59110e4b3cb1a5ea76d370c1c29fa64f724a110cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235870437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f51417dfdbf3f6c2434b2fff64530fba6e0f244c616cb62846faaaf18f65135`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b558e90d6fc975fa2a3f53fea4da93097ed99a881f1b1deb0fa402babe5a43b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015ed6adb6c4babaa64aca8599fbdb4961051bc2aa736754ff623179ee7b8126`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064123821702dc2bfea097496e07dd37de0f1f2fe1efedcbad96dad1737a879`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4221635d1cb8be70e7a3ed5f1d6a499f1880d16d4609d7b66d561ed28514f055`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41fa75920fa26cf9e535361ab9c99603fa046bd3c7f9168bb0bfbe1896a1e9e`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0c0d6464b62936f81dbfb49cceebacca53ebc40e3f27a58ff9b1deeb2cfacb`  
		Last Modified: Sat, 18 Oct 2025 00:13:23 GMT  
		Size: 49.8 MB (49835234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc0d02e80992b59ac2ece9a1689c8fda20cb6ddfe9038b1f209c348ef1cf49f`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c44f22ceaa6fefe0ad316cdbdc40330b810336461a0a1e147edda440f67ab`  
		Last Modified: Sat, 18 Oct 2025 03:02:39 GMT  
		Size: 128.9 MB (128925787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6768abefd521f255f4a35cc21173aeeac6822dff0861a46fc5a390617f85a509`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810776de36a8ac26c55c424d1434215c2bb5718f36289ce4b3286fa66663d4ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e3a4ce0e81a844f3a1b82fd30c38776d9f3524bad2835d53628284398824bd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de15c3956b5aa0b213081193632b9587d02509be43a10466d50dac837ff23410`

```dockerfile
```

-	Layers:
	-	`sha256:44a88059b74ff32929db6b13476c5a1200e9c303908ad3b084baf0a29182cc5e`  
		Last Modified: Sat, 18 Oct 2025 03:02:35 GMT  
		Size: 14.5 MB (14528113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:749b722dd01d17eef59ea7d398f092c009a037087a5e411e23778de9852a5fc4`  
		Last Modified: Sat, 18 Oct 2025 03:02:36 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44`

```console
$ docker pull mysql@sha256:89a43274213cccf817edcf635bbc1bfdd392eeebac716e843de2ca7b338dbf31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-bookworm`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.44-debian`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.44-oracle`

```console
$ docker pull mysql@sha256:89a43274213cccf817edcf635bbc1bfdd392eeebac716e843de2ca7b338dbf31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oraclelinux9`

```console
$ docker pull mysql@sha256:89a43274213cccf817edcf635bbc1bfdd392eeebac716e843de2ca7b338dbf31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f5ef4f6a1d2b1e59a4ecc8bc39a4a8af0b257f6541e114d2bad1437d7ceb0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230489157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2668c01420a284ff59db3fd2572ea5ed161fa644d30553f4c9d349aced0a3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 21 Oct 2025 16:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Oct 2025 16:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b724db88999ae7094bfb75218d9c2b010387ac848176f4854ec6aab91f72e`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf432ee766a24a12f24dd6d4b4afb19e3f413ca687abb834820da2c25994a1`  
		Last Modified: Tue, 21 Oct 2025 23:42:37 GMT  
		Size: 48.8 MB (48762226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e625c6ed2b41e7bde64c5f71e2ec315f11d0e97ab5e3108da05d08e01d5f6de`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b19e58c3ba338241c6e902403358d300179c7837b24a9e204c66fb660f655`  
		Last Modified: Tue, 21 Oct 2025 23:42:57 GMT  
		Size: 126.4 MB (126447877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fafa8e66b968a6fb6fcb1aaf772c841fa11e97e94502936b0e02c636d62e577`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5670e3d652a63a10adc605194d1aa99e68f7ae2570dac43c26d5fd5d6b7cd281`  
		Last Modified: Tue, 21 Oct 2025 23:42:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:77b6119be06a6e19f15876e47a455ff8d78d25e77441718bc619131844cdcdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14669010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7346efa99ba288630a01b6f13072c7b8523f2482f02044b9ead2fb387bc29ad9`

```dockerfile
```

-	Layers:
	-	`sha256:790ee1c80facffada39fd46d9ec1e17ac963e92b8eae5dca8e909b6cef3e9dc7`  
		Last Modified: Wed, 22 Oct 2025 00:02:36 GMT  
		Size: 14.6 MB (14633808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0429dc33e0019d37881fe3eb379844c03028e5a486b2a9793755c14097c47348`  
		Last Modified: Wed, 22 Oct 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:17c90cde7cbe56a334e0513768adf67ee5b29491f17df765102134388d20fe0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:c296d65ee6ab3ce2f608c1d1b2bdd3c08b087a5834101d76a6db2e00875216cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236856592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa03bf950b7fca40d7e1cae1ed638fadbc63b679ff74f1efb7d626e4c042ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fd76abbeb40b742af6aea70a2a70b73d1bfebcbac90053f0b7afc6505d518`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559d1bfb3bdb6d611f5e6c1f759de333193229ccab1ba120cedb27bd59dd327`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 783.5 KB (783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2257dfd80e5f7f4d03e9de86ad0b2d16b4581f4806faf8f47cda3c2183f19`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17cf5ce963905fef25d94f1a8cab2790e69f8dc27dd25ecef15adc1c89719b3`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff1798e33ce31cc9052a2d9a2e52f0235890142d7e400fb45c99eeb1d0a47cc`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ce10052616570c2b3b5863801d011d502e83c4dc016a10baedfb575af1529`  
		Last Modified: Sat, 18 Oct 2025 00:13:24 GMT  
		Size: 47.8 MB (47786071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46b44d7c262c6d21ffc28f69f07a1099ab6c200b9143a5f6c19eaa2ef18787`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d610e0f99daba87a52dd89c5e749e34ac351618c3247d6c31e53b29747baaea8`  
		Last Modified: Sat, 18 Oct 2025 01:00:21 GMT  
		Size: 132.0 MB (131961222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cf40c4e15f5bc3f3b39c070a7840d54921e5cd5c63b9302daaf4d663eb18b`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:1852a1650dfd0228d1354e78cbac5cf9d15cf6ab1f4e4f72ca062113ee2bcbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6732224879892fa7d8f6ee7f25c94858ccc54919e942411918cc1948a00a91a3`

```dockerfile
```

-	Layers:
	-	`sha256:1a32a4104c592d2fb8ecf0eff3905c10054b60862ba74d5336429c99ccbb7141`  
		Last Modified: Sat, 18 Oct 2025 03:02:23 GMT  
		Size: 14.8 MB (14804934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c30447d861a7a5b639b99eedebb7201c763ae961977c0cef3c63e8211404ca`  
		Last Modified: Sat, 18 Oct 2025 03:02:24 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:17c90cde7cbe56a334e0513768adf67ee5b29491f17df765102134388d20fe0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c296d65ee6ab3ce2f608c1d1b2bdd3c08b087a5834101d76a6db2e00875216cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236856592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa03bf950b7fca40d7e1cae1ed638fadbc63b679ff74f1efb7d626e4c042ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fd76abbeb40b742af6aea70a2a70b73d1bfebcbac90053f0b7afc6505d518`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559d1bfb3bdb6d611f5e6c1f759de333193229ccab1ba120cedb27bd59dd327`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 783.5 KB (783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2257dfd80e5f7f4d03e9de86ad0b2d16b4581f4806faf8f47cda3c2183f19`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17cf5ce963905fef25d94f1a8cab2790e69f8dc27dd25ecef15adc1c89719b3`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff1798e33ce31cc9052a2d9a2e52f0235890142d7e400fb45c99eeb1d0a47cc`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ce10052616570c2b3b5863801d011d502e83c4dc016a10baedfb575af1529`  
		Last Modified: Sat, 18 Oct 2025 00:13:24 GMT  
		Size: 47.8 MB (47786071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46b44d7c262c6d21ffc28f69f07a1099ab6c200b9143a5f6c19eaa2ef18787`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d610e0f99daba87a52dd89c5e749e34ac351618c3247d6c31e53b29747baaea8`  
		Last Modified: Sat, 18 Oct 2025 01:00:21 GMT  
		Size: 132.0 MB (131961222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cf40c4e15f5bc3f3b39c070a7840d54921e5cd5c63b9302daaf4d663eb18b`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1852a1650dfd0228d1354e78cbac5cf9d15cf6ab1f4e4f72ca062113ee2bcbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6732224879892fa7d8f6ee7f25c94858ccc54919e942411918cc1948a00a91a3`

```dockerfile
```

-	Layers:
	-	`sha256:1a32a4104c592d2fb8ecf0eff3905c10054b60862ba74d5336429c99ccbb7141`  
		Last Modified: Sat, 18 Oct 2025 03:02:23 GMT  
		Size: 14.8 MB (14804934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c30447d861a7a5b639b99eedebb7201c763ae961977c0cef3c63e8211404ca`  
		Last Modified: Sat, 18 Oct 2025 03:02:24 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:17c90cde7cbe56a334e0513768adf67ee5b29491f17df765102134388d20fe0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c296d65ee6ab3ce2f608c1d1b2bdd3c08b087a5834101d76a6db2e00875216cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236856592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa03bf950b7fca40d7e1cae1ed638fadbc63b679ff74f1efb7d626e4c042ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fd76abbeb40b742af6aea70a2a70b73d1bfebcbac90053f0b7afc6505d518`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559d1bfb3bdb6d611f5e6c1f759de333193229ccab1ba120cedb27bd59dd327`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 783.5 KB (783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2257dfd80e5f7f4d03e9de86ad0b2d16b4581f4806faf8f47cda3c2183f19`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17cf5ce963905fef25d94f1a8cab2790e69f8dc27dd25ecef15adc1c89719b3`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff1798e33ce31cc9052a2d9a2e52f0235890142d7e400fb45c99eeb1d0a47cc`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ce10052616570c2b3b5863801d011d502e83c4dc016a10baedfb575af1529`  
		Last Modified: Sat, 18 Oct 2025 00:13:24 GMT  
		Size: 47.8 MB (47786071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46b44d7c262c6d21ffc28f69f07a1099ab6c200b9143a5f6c19eaa2ef18787`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d610e0f99daba87a52dd89c5e749e34ac351618c3247d6c31e53b29747baaea8`  
		Last Modified: Sat, 18 Oct 2025 01:00:21 GMT  
		Size: 132.0 MB (131961222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cf40c4e15f5bc3f3b39c070a7840d54921e5cd5c63b9302daaf4d663eb18b`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1852a1650dfd0228d1354e78cbac5cf9d15cf6ab1f4e4f72ca062113ee2bcbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6732224879892fa7d8f6ee7f25c94858ccc54919e942411918cc1948a00a91a3`

```dockerfile
```

-	Layers:
	-	`sha256:1a32a4104c592d2fb8ecf0eff3905c10054b60862ba74d5336429c99ccbb7141`  
		Last Modified: Sat, 18 Oct 2025 03:02:23 GMT  
		Size: 14.8 MB (14804934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c30447d861a7a5b639b99eedebb7201c763ae961977c0cef3c63e8211404ca`  
		Last Modified: Sat, 18 Oct 2025 03:02:24 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7`

```console
$ docker pull mysql@sha256:d3c43fb95f76fe27a6195e6d9a020bfb4d5b5b66027f56a2007cbfa5cbf74ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oracle`

```console
$ docker pull mysql@sha256:d3c43fb95f76fe27a6195e6d9a020bfb4d5b5b66027f56a2007cbfa5cbf74ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oraclelinux9`

```console
$ docker pull mysql@sha256:d3c43fb95f76fe27a6195e6d9a020bfb4d5b5b66027f56a2007cbfa5cbf74ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:e0e81e2a9d38248893cb99ebe623359001e7feedc12617ec38589f8e52f8f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:a04a60356334e1626dac5d4112ffa034b1e5b2f924eccf2c0e1d5e9513bb7a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275362860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbb21ac6e2a564ebe755fd077cfb79101602ec73f64b6e771e06419393d9de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4ab4514f3f70fa2330887139eb97081f25773cc9f80e3343f80f8c6d6af79`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41962a6e179c9630f56de1dc1368caf7b8399e3f3e0380f1ea5071f45d80f6`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c273bf16257d1e1a07bc95d589cc2edb505bfe35634e15131e245c40de4c`  
		Last Modified: Sat, 18 Oct 2025 00:12:40 GMT  
		Size: 6.8 MB (6819546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7bb6f233809aa02e940808745b6dc2ead230f9b1b8014b6dc43239cb37021c`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14016e5704e9f43fb6a9fbb23dae339f98687d697b92770b1e531790ee61bf66`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec820315573127dd853c96854b89163d1b3ab1391255a222edfb876eca7b45`  
		Last Modified: Sat, 18 Oct 2025 00:12:43 GMT  
		Size: 49.3 MB (49286447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab5c52ff909849cbd904a4255c1ddfa85b4dee19e47d4de85ae40eb9b1bc1e`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df181eca63856fca89bc5f93aaea67c105b5565dca29c095fb856bbca46fd0`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 169.0 MB (168967326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e127489368459c556965f2b35c97b5055e709ec8bf3fe4c20cbe6a58a2162`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:227443b5e664e0ac4121d18211f9d55a6f29907049d55f7630a10d84ec574f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7a61aabf216d0948ccabb7c40f9318074a8c54d68b1db5cdaf37fe9abdae9f`

```dockerfile
```

-	Layers:
	-	`sha256:50a66f9d377b015a692d476a32002aa1b6f12f9c58380af5a9d4f986414edee2`  
		Last Modified: Sat, 18 Oct 2025 03:03:14 GMT  
		Size: 17.7 MB (17699301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96513412703073e1d666b1e1e022722407349f85c6c72486f107685272bc9c90`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:e0e81e2a9d38248893cb99ebe623359001e7feedc12617ec38589f8e52f8f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a04a60356334e1626dac5d4112ffa034b1e5b2f924eccf2c0e1d5e9513bb7a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275362860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbb21ac6e2a564ebe755fd077cfb79101602ec73f64b6e771e06419393d9de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4ab4514f3f70fa2330887139eb97081f25773cc9f80e3343f80f8c6d6af79`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41962a6e179c9630f56de1dc1368caf7b8399e3f3e0380f1ea5071f45d80f6`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c273bf16257d1e1a07bc95d589cc2edb505bfe35634e15131e245c40de4c`  
		Last Modified: Sat, 18 Oct 2025 00:12:40 GMT  
		Size: 6.8 MB (6819546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7bb6f233809aa02e940808745b6dc2ead230f9b1b8014b6dc43239cb37021c`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14016e5704e9f43fb6a9fbb23dae339f98687d697b92770b1e531790ee61bf66`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec820315573127dd853c96854b89163d1b3ab1391255a222edfb876eca7b45`  
		Last Modified: Sat, 18 Oct 2025 00:12:43 GMT  
		Size: 49.3 MB (49286447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab5c52ff909849cbd904a4255c1ddfa85b4dee19e47d4de85ae40eb9b1bc1e`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df181eca63856fca89bc5f93aaea67c105b5565dca29c095fb856bbca46fd0`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 169.0 MB (168967326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e127489368459c556965f2b35c97b5055e709ec8bf3fe4c20cbe6a58a2162`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:227443b5e664e0ac4121d18211f9d55a6f29907049d55f7630a10d84ec574f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7a61aabf216d0948ccabb7c40f9318074a8c54d68b1db5cdaf37fe9abdae9f`

```dockerfile
```

-	Layers:
	-	`sha256:50a66f9d377b015a692d476a32002aa1b6f12f9c58380af5a9d4f986414edee2`  
		Last Modified: Sat, 18 Oct 2025 03:03:14 GMT  
		Size: 17.7 MB (17699301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96513412703073e1d666b1e1e022722407349f85c6c72486f107685272bc9c90`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:e0e81e2a9d38248893cb99ebe623359001e7feedc12617ec38589f8e52f8f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a04a60356334e1626dac5d4112ffa034b1e5b2f924eccf2c0e1d5e9513bb7a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275362860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbb21ac6e2a564ebe755fd077cfb79101602ec73f64b6e771e06419393d9de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4ab4514f3f70fa2330887139eb97081f25773cc9f80e3343f80f8c6d6af79`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41962a6e179c9630f56de1dc1368caf7b8399e3f3e0380f1ea5071f45d80f6`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c273bf16257d1e1a07bc95d589cc2edb505bfe35634e15131e245c40de4c`  
		Last Modified: Sat, 18 Oct 2025 00:12:40 GMT  
		Size: 6.8 MB (6819546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7bb6f233809aa02e940808745b6dc2ead230f9b1b8014b6dc43239cb37021c`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14016e5704e9f43fb6a9fbb23dae339f98687d697b92770b1e531790ee61bf66`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec820315573127dd853c96854b89163d1b3ab1391255a222edfb876eca7b45`  
		Last Modified: Sat, 18 Oct 2025 00:12:43 GMT  
		Size: 49.3 MB (49286447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab5c52ff909849cbd904a4255c1ddfa85b4dee19e47d4de85ae40eb9b1bc1e`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df181eca63856fca89bc5f93aaea67c105b5565dca29c095fb856bbca46fd0`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 169.0 MB (168967326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e127489368459c556965f2b35c97b5055e709ec8bf3fe4c20cbe6a58a2162`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:227443b5e664e0ac4121d18211f9d55a6f29907049d55f7630a10d84ec574f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7a61aabf216d0948ccabb7c40f9318074a8c54d68b1db5cdaf37fe9abdae9f`

```dockerfile
```

-	Layers:
	-	`sha256:50a66f9d377b015a692d476a32002aa1b6f12f9c58380af5a9d4f986414edee2`  
		Last Modified: Sat, 18 Oct 2025 03:03:14 GMT  
		Size: 17.7 MB (17699301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96513412703073e1d666b1e1e022722407349f85c6c72486f107685272bc9c90`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5`

```console
$ docker pull mysql@sha256:2b12787d18c595d7c7b71806462a3f398b2502a491acfed255d46d81d537fb79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oracle`

```console
$ docker pull mysql@sha256:2b12787d18c595d7c7b71806462a3f398b2502a491acfed255d46d81d537fb79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oraclelinux9`

```console
$ docker pull mysql@sha256:2b12787d18c595d7c7b71806462a3f398b2502a491acfed255d46d81d537fb79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0`

```console
$ docker pull mysql@sha256:2b12787d18c595d7c7b71806462a3f398b2502a491acfed255d46d81d537fb79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oracle`

```console
$ docker pull mysql@sha256:2b12787d18c595d7c7b71806462a3f398b2502a491acfed255d46d81d537fb79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oraclelinux9`

```console
$ docker pull mysql@sha256:2b12787d18c595d7c7b71806462a3f398b2502a491acfed255d46d81d537fb79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:e0e81e2a9d38248893cb99ebe623359001e7feedc12617ec38589f8e52f8f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:a04a60356334e1626dac5d4112ffa034b1e5b2f924eccf2c0e1d5e9513bb7a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275362860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbb21ac6e2a564ebe755fd077cfb79101602ec73f64b6e771e06419393d9de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4ab4514f3f70fa2330887139eb97081f25773cc9f80e3343f80f8c6d6af79`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41962a6e179c9630f56de1dc1368caf7b8399e3f3e0380f1ea5071f45d80f6`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c273bf16257d1e1a07bc95d589cc2edb505bfe35634e15131e245c40de4c`  
		Last Modified: Sat, 18 Oct 2025 00:12:40 GMT  
		Size: 6.8 MB (6819546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7bb6f233809aa02e940808745b6dc2ead230f9b1b8014b6dc43239cb37021c`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14016e5704e9f43fb6a9fbb23dae339f98687d697b92770b1e531790ee61bf66`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec820315573127dd853c96854b89163d1b3ab1391255a222edfb876eca7b45`  
		Last Modified: Sat, 18 Oct 2025 00:12:43 GMT  
		Size: 49.3 MB (49286447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab5c52ff909849cbd904a4255c1ddfa85b4dee19e47d4de85ae40eb9b1bc1e`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df181eca63856fca89bc5f93aaea67c105b5565dca29c095fb856bbca46fd0`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 169.0 MB (168967326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e127489368459c556965f2b35c97b5055e709ec8bf3fe4c20cbe6a58a2162`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:227443b5e664e0ac4121d18211f9d55a6f29907049d55f7630a10d84ec574f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7a61aabf216d0948ccabb7c40f9318074a8c54d68b1db5cdaf37fe9abdae9f`

```dockerfile
```

-	Layers:
	-	`sha256:50a66f9d377b015a692d476a32002aa1b6f12f9c58380af5a9d4f986414edee2`  
		Last Modified: Sat, 18 Oct 2025 03:03:14 GMT  
		Size: 17.7 MB (17699301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96513412703073e1d666b1e1e022722407349f85c6c72486f107685272bc9c90`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:e0e81e2a9d38248893cb99ebe623359001e7feedc12617ec38589f8e52f8f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a04a60356334e1626dac5d4112ffa034b1e5b2f924eccf2c0e1d5e9513bb7a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275362860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbb21ac6e2a564ebe755fd077cfb79101602ec73f64b6e771e06419393d9de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4ab4514f3f70fa2330887139eb97081f25773cc9f80e3343f80f8c6d6af79`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41962a6e179c9630f56de1dc1368caf7b8399e3f3e0380f1ea5071f45d80f6`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c273bf16257d1e1a07bc95d589cc2edb505bfe35634e15131e245c40de4c`  
		Last Modified: Sat, 18 Oct 2025 00:12:40 GMT  
		Size: 6.8 MB (6819546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7bb6f233809aa02e940808745b6dc2ead230f9b1b8014b6dc43239cb37021c`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14016e5704e9f43fb6a9fbb23dae339f98687d697b92770b1e531790ee61bf66`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec820315573127dd853c96854b89163d1b3ab1391255a222edfb876eca7b45`  
		Last Modified: Sat, 18 Oct 2025 00:12:43 GMT  
		Size: 49.3 MB (49286447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab5c52ff909849cbd904a4255c1ddfa85b4dee19e47d4de85ae40eb9b1bc1e`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df181eca63856fca89bc5f93aaea67c105b5565dca29c095fb856bbca46fd0`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 169.0 MB (168967326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e127489368459c556965f2b35c97b5055e709ec8bf3fe4c20cbe6a58a2162`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:227443b5e664e0ac4121d18211f9d55a6f29907049d55f7630a10d84ec574f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7a61aabf216d0948ccabb7c40f9318074a8c54d68b1db5cdaf37fe9abdae9f`

```dockerfile
```

-	Layers:
	-	`sha256:50a66f9d377b015a692d476a32002aa1b6f12f9c58380af5a9d4f986414edee2`  
		Last Modified: Sat, 18 Oct 2025 03:03:14 GMT  
		Size: 17.7 MB (17699301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96513412703073e1d666b1e1e022722407349f85c6c72486f107685272bc9c90`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:e0e81e2a9d38248893cb99ebe623359001e7feedc12617ec38589f8e52f8f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a04a60356334e1626dac5d4112ffa034b1e5b2f924eccf2c0e1d5e9513bb7a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275362860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbb21ac6e2a564ebe755fd077cfb79101602ec73f64b6e771e06419393d9de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4ab4514f3f70fa2330887139eb97081f25773cc9f80e3343f80f8c6d6af79`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41962a6e179c9630f56de1dc1368caf7b8399e3f3e0380f1ea5071f45d80f6`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c273bf16257d1e1a07bc95d589cc2edb505bfe35634e15131e245c40de4c`  
		Last Modified: Sat, 18 Oct 2025 00:12:40 GMT  
		Size: 6.8 MB (6819546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7bb6f233809aa02e940808745b6dc2ead230f9b1b8014b6dc43239cb37021c`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14016e5704e9f43fb6a9fbb23dae339f98687d697b92770b1e531790ee61bf66`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec820315573127dd853c96854b89163d1b3ab1391255a222edfb876eca7b45`  
		Last Modified: Sat, 18 Oct 2025 00:12:43 GMT  
		Size: 49.3 MB (49286447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab5c52ff909849cbd904a4255c1ddfa85b4dee19e47d4de85ae40eb9b1bc1e`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df181eca63856fca89bc5f93aaea67c105b5565dca29c095fb856bbca46fd0`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 169.0 MB (168967326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e127489368459c556965f2b35c97b5055e709ec8bf3fe4c20cbe6a58a2162`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:227443b5e664e0ac4121d18211f9d55a6f29907049d55f7630a10d84ec574f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7a61aabf216d0948ccabb7c40f9318074a8c54d68b1db5cdaf37fe9abdae9f`

```dockerfile
```

-	Layers:
	-	`sha256:50a66f9d377b015a692d476a32002aa1b6f12f9c58380af5a9d4f986414edee2`  
		Last Modified: Sat, 18 Oct 2025 03:03:14 GMT  
		Size: 17.7 MB (17699301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96513412703073e1d666b1e1e022722407349f85c6c72486f107685272bc9c90`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:e0e81e2a9d38248893cb99ebe623359001e7feedc12617ec38589f8e52f8f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:a04a60356334e1626dac5d4112ffa034b1e5b2f924eccf2c0e1d5e9513bb7a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275362860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbb21ac6e2a564ebe755fd077cfb79101602ec73f64b6e771e06419393d9de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4ab4514f3f70fa2330887139eb97081f25773cc9f80e3343f80f8c6d6af79`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41962a6e179c9630f56de1dc1368caf7b8399e3f3e0380f1ea5071f45d80f6`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c273bf16257d1e1a07bc95d589cc2edb505bfe35634e15131e245c40de4c`  
		Last Modified: Sat, 18 Oct 2025 00:12:40 GMT  
		Size: 6.8 MB (6819546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7bb6f233809aa02e940808745b6dc2ead230f9b1b8014b6dc43239cb37021c`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14016e5704e9f43fb6a9fbb23dae339f98687d697b92770b1e531790ee61bf66`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec820315573127dd853c96854b89163d1b3ab1391255a222edfb876eca7b45`  
		Last Modified: Sat, 18 Oct 2025 00:12:43 GMT  
		Size: 49.3 MB (49286447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab5c52ff909849cbd904a4255c1ddfa85b4dee19e47d4de85ae40eb9b1bc1e`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df181eca63856fca89bc5f93aaea67c105b5565dca29c095fb856bbca46fd0`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 169.0 MB (168967326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e127489368459c556965f2b35c97b5055e709ec8bf3fe4c20cbe6a58a2162`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:227443b5e664e0ac4121d18211f9d55a6f29907049d55f7630a10d84ec574f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7a61aabf216d0948ccabb7c40f9318074a8c54d68b1db5cdaf37fe9abdae9f`

```dockerfile
```

-	Layers:
	-	`sha256:50a66f9d377b015a692d476a32002aa1b6f12f9c58380af5a9d4f986414edee2`  
		Last Modified: Sat, 18 Oct 2025 03:03:14 GMT  
		Size: 17.7 MB (17699301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96513412703073e1d666b1e1e022722407349f85c6c72486f107685272bc9c90`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:17c90cde7cbe56a334e0513768adf67ee5b29491f17df765102134388d20fe0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:c296d65ee6ab3ce2f608c1d1b2bdd3c08b087a5834101d76a6db2e00875216cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236856592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa03bf950b7fca40d7e1cae1ed638fadbc63b679ff74f1efb7d626e4c042ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fd76abbeb40b742af6aea70a2a70b73d1bfebcbac90053f0b7afc6505d518`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559d1bfb3bdb6d611f5e6c1f759de333193229ccab1ba120cedb27bd59dd327`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 783.5 KB (783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2257dfd80e5f7f4d03e9de86ad0b2d16b4581f4806faf8f47cda3c2183f19`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17cf5ce963905fef25d94f1a8cab2790e69f8dc27dd25ecef15adc1c89719b3`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff1798e33ce31cc9052a2d9a2e52f0235890142d7e400fb45c99eeb1d0a47cc`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ce10052616570c2b3b5863801d011d502e83c4dc016a10baedfb575af1529`  
		Last Modified: Sat, 18 Oct 2025 00:13:24 GMT  
		Size: 47.8 MB (47786071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46b44d7c262c6d21ffc28f69f07a1099ab6c200b9143a5f6c19eaa2ef18787`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d610e0f99daba87a52dd89c5e749e34ac351618c3247d6c31e53b29747baaea8`  
		Last Modified: Sat, 18 Oct 2025 01:00:21 GMT  
		Size: 132.0 MB (131961222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cf40c4e15f5bc3f3b39c070a7840d54921e5cd5c63b9302daaf4d663eb18b`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:1852a1650dfd0228d1354e78cbac5cf9d15cf6ab1f4e4f72ca062113ee2bcbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6732224879892fa7d8f6ee7f25c94858ccc54919e942411918cc1948a00a91a3`

```dockerfile
```

-	Layers:
	-	`sha256:1a32a4104c592d2fb8ecf0eff3905c10054b60862ba74d5336429c99ccbb7141`  
		Last Modified: Sat, 18 Oct 2025 03:02:23 GMT  
		Size: 14.8 MB (14804934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c30447d861a7a5b639b99eedebb7201c763ae961977c0cef3c63e8211404ca`  
		Last Modified: Sat, 18 Oct 2025 03:02:24 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:17c90cde7cbe56a334e0513768adf67ee5b29491f17df765102134388d20fe0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c296d65ee6ab3ce2f608c1d1b2bdd3c08b087a5834101d76a6db2e00875216cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236856592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa03bf950b7fca40d7e1cae1ed638fadbc63b679ff74f1efb7d626e4c042ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fd76abbeb40b742af6aea70a2a70b73d1bfebcbac90053f0b7afc6505d518`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559d1bfb3bdb6d611f5e6c1f759de333193229ccab1ba120cedb27bd59dd327`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 783.5 KB (783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2257dfd80e5f7f4d03e9de86ad0b2d16b4581f4806faf8f47cda3c2183f19`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17cf5ce963905fef25d94f1a8cab2790e69f8dc27dd25ecef15adc1c89719b3`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff1798e33ce31cc9052a2d9a2e52f0235890142d7e400fb45c99eeb1d0a47cc`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ce10052616570c2b3b5863801d011d502e83c4dc016a10baedfb575af1529`  
		Last Modified: Sat, 18 Oct 2025 00:13:24 GMT  
		Size: 47.8 MB (47786071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46b44d7c262c6d21ffc28f69f07a1099ab6c200b9143a5f6c19eaa2ef18787`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d610e0f99daba87a52dd89c5e749e34ac351618c3247d6c31e53b29747baaea8`  
		Last Modified: Sat, 18 Oct 2025 01:00:21 GMT  
		Size: 132.0 MB (131961222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cf40c4e15f5bc3f3b39c070a7840d54921e5cd5c63b9302daaf4d663eb18b`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1852a1650dfd0228d1354e78cbac5cf9d15cf6ab1f4e4f72ca062113ee2bcbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6732224879892fa7d8f6ee7f25c94858ccc54919e942411918cc1948a00a91a3`

```dockerfile
```

-	Layers:
	-	`sha256:1a32a4104c592d2fb8ecf0eff3905c10054b60862ba74d5336429c99ccbb7141`  
		Last Modified: Sat, 18 Oct 2025 03:02:23 GMT  
		Size: 14.8 MB (14804934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c30447d861a7a5b639b99eedebb7201c763ae961977c0cef3c63e8211404ca`  
		Last Modified: Sat, 18 Oct 2025 03:02:24 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:17c90cde7cbe56a334e0513768adf67ee5b29491f17df765102134388d20fe0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c296d65ee6ab3ce2f608c1d1b2bdd3c08b087a5834101d76a6db2e00875216cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236856592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa03bf950b7fca40d7e1cae1ed638fadbc63b679ff74f1efb7d626e4c042ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fd76abbeb40b742af6aea70a2a70b73d1bfebcbac90053f0b7afc6505d518`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559d1bfb3bdb6d611f5e6c1f759de333193229ccab1ba120cedb27bd59dd327`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 783.5 KB (783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2257dfd80e5f7f4d03e9de86ad0b2d16b4581f4806faf8f47cda3c2183f19`  
		Last Modified: Sat, 18 Oct 2025 00:13:18 GMT  
		Size: 6.8 MB (6819784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17cf5ce963905fef25d94f1a8cab2790e69f8dc27dd25ecef15adc1c89719b3`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff1798e33ce31cc9052a2d9a2e52f0235890142d7e400fb45c99eeb1d0a47cc`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ce10052616570c2b3b5863801d011d502e83c4dc016a10baedfb575af1529`  
		Last Modified: Sat, 18 Oct 2025 00:13:24 GMT  
		Size: 47.8 MB (47786071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46b44d7c262c6d21ffc28f69f07a1099ab6c200b9143a5f6c19eaa2ef18787`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d610e0f99daba87a52dd89c5e749e34ac351618c3247d6c31e53b29747baaea8`  
		Last Modified: Sat, 18 Oct 2025 01:00:21 GMT  
		Size: 132.0 MB (131961222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cf40c4e15f5bc3f3b39c070a7840d54921e5cd5c63b9302daaf4d663eb18b`  
		Last Modified: Sat, 18 Oct 2025 00:13:17 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1852a1650dfd0228d1354e78cbac5cf9d15cf6ab1f4e4f72ca062113ee2bcbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6732224879892fa7d8f6ee7f25c94858ccc54919e942411918cc1948a00a91a3`

```dockerfile
```

-	Layers:
	-	`sha256:1a32a4104c592d2fb8ecf0eff3905c10054b60862ba74d5336429c99ccbb7141`  
		Last Modified: Sat, 18 Oct 2025 03:02:23 GMT  
		Size: 14.8 MB (14804934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c30447d861a7a5b639b99eedebb7201c763ae961977c0cef3c63e8211404ca`  
		Last Modified: Sat, 18 Oct 2025 03:02:24 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9b15d1b834f7cf8133db26b4a01b9b1f8e58089716cb12b0210d9c1537504ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6eaf15ba78fc08cc39646f9e1c999e08c2032dfc9eb2103cd2b7906cf9f72f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 21 Oct 2025 16:22:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:22:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:22:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f2f68fb5ab86fa561be30daaad4f29e4d3c10415090ba46c26fff4252ceb0`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8ef29f1ae281e68aab04912174892d539d70dc6fcf544c8eee869a5072f9b`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79ac6abc40f2cf613005d34d19078f244cc371afdce47ec7d28606f58714bc`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 6.4 MB (6445103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2494d47728e2e98dd7cbf8a0a639c383747cab7eca6467d20aa7017a07ac1897`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608d450c0f8ad9d91f7b0485a4df7f25f51f7b4b3723f7a043424f292220512`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acfa02adee414654ea2ef93c7e747fbecdfc292335120318ae04a69bd594953`  
		Last Modified: Tue, 21 Oct 2025 23:41:40 GMT  
		Size: 46.7 MB (46678409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c304a359bf3589a80a46da06c55b729fe8d355dcb1f9cac137231d673fc07bd`  
		Last Modified: Tue, 21 Oct 2025 23:41:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a1ab98b1553da0f147b88feadef5a0fad9ed4a5af28aa8e785f3e16f9346`  
		Last Modified: Wed, 22 Oct 2025 00:02:39 GMT  
		Size: 129.3 MB (129304391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fa7759aa969f832b473668f180c610a0a1c7af4e347ad900e6073941ae798`  
		Last Modified: Tue, 21 Oct 2025 23:41:37 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3293b794c6eae1073f766ad1d6c9b1ab717f76369fc27b2d2a05dd556e70ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14945257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0acfc2384c84e7c9731a147255c11c3ee43f8a0ddba88cdaf3e6bd08f694e`

```dockerfile
```

-	Layers:
	-	`sha256:bde543acfac176129de05dc7a2a9fa6d9e55813ba3683b1ddf104fd394a5ba48`  
		Last Modified: Wed, 22 Oct 2025 00:02:29 GMT  
		Size: 14.9 MB (14910701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfade1b1ade5fecd4a2dee8c960405d98646752701b824ee07a5aef8afe170d2`  
		Last Modified: Wed, 22 Oct 2025 00:02:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:e0e81e2a9d38248893cb99ebe623359001e7feedc12617ec38589f8e52f8f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a04a60356334e1626dac5d4112ffa034b1e5b2f924eccf2c0e1d5e9513bb7a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275362860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbb21ac6e2a564ebe755fd077cfb79101602ec73f64b6e771e06419393d9de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4ab4514f3f70fa2330887139eb97081f25773cc9f80e3343f80f8c6d6af79`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41962a6e179c9630f56de1dc1368caf7b8399e3f3e0380f1ea5071f45d80f6`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c273bf16257d1e1a07bc95d589cc2edb505bfe35634e15131e245c40de4c`  
		Last Modified: Sat, 18 Oct 2025 00:12:40 GMT  
		Size: 6.8 MB (6819546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7bb6f233809aa02e940808745b6dc2ead230f9b1b8014b6dc43239cb37021c`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14016e5704e9f43fb6a9fbb23dae339f98687d697b92770b1e531790ee61bf66`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec820315573127dd853c96854b89163d1b3ab1391255a222edfb876eca7b45`  
		Last Modified: Sat, 18 Oct 2025 00:12:43 GMT  
		Size: 49.3 MB (49286447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab5c52ff909849cbd904a4255c1ddfa85b4dee19e47d4de85ae40eb9b1bc1e`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df181eca63856fca89bc5f93aaea67c105b5565dca29c095fb856bbca46fd0`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 169.0 MB (168967326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e127489368459c556965f2b35c97b5055e709ec8bf3fe4c20cbe6a58a2162`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:227443b5e664e0ac4121d18211f9d55a6f29907049d55f7630a10d84ec574f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7a61aabf216d0948ccabb7c40f9318074a8c54d68b1db5cdaf37fe9abdae9f`

```dockerfile
```

-	Layers:
	-	`sha256:50a66f9d377b015a692d476a32002aa1b6f12f9c58380af5a9d4f986414edee2`  
		Last Modified: Sat, 18 Oct 2025 03:03:14 GMT  
		Size: 17.7 MB (17699301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96513412703073e1d666b1e1e022722407349f85c6c72486f107685272bc9c90`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:e0e81e2a9d38248893cb99ebe623359001e7feedc12617ec38589f8e52f8f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a04a60356334e1626dac5d4112ffa034b1e5b2f924eccf2c0e1d5e9513bb7a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275362860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbb21ac6e2a564ebe755fd077cfb79101602ec73f64b6e771e06419393d9de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4ab4514f3f70fa2330887139eb97081f25773cc9f80e3343f80f8c6d6af79`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41962a6e179c9630f56de1dc1368caf7b8399e3f3e0380f1ea5071f45d80f6`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c273bf16257d1e1a07bc95d589cc2edb505bfe35634e15131e245c40de4c`  
		Last Modified: Sat, 18 Oct 2025 00:12:40 GMT  
		Size: 6.8 MB (6819546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7bb6f233809aa02e940808745b6dc2ead230f9b1b8014b6dc43239cb37021c`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14016e5704e9f43fb6a9fbb23dae339f98687d697b92770b1e531790ee61bf66`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec820315573127dd853c96854b89163d1b3ab1391255a222edfb876eca7b45`  
		Last Modified: Sat, 18 Oct 2025 00:12:43 GMT  
		Size: 49.3 MB (49286447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab5c52ff909849cbd904a4255c1ddfa85b4dee19e47d4de85ae40eb9b1bc1e`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df181eca63856fca89bc5f93aaea67c105b5565dca29c095fb856bbca46fd0`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 169.0 MB (168967326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e127489368459c556965f2b35c97b5055e709ec8bf3fe4c20cbe6a58a2162`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:227443b5e664e0ac4121d18211f9d55a6f29907049d55f7630a10d84ec574f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7a61aabf216d0948ccabb7c40f9318074a8c54d68b1db5cdaf37fe9abdae9f`

```dockerfile
```

-	Layers:
	-	`sha256:50a66f9d377b015a692d476a32002aa1b6f12f9c58380af5a9d4f986414edee2`  
		Last Modified: Sat, 18 Oct 2025 03:03:14 GMT  
		Size: 17.7 MB (17699301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96513412703073e1d666b1e1e022722407349f85c6c72486f107685272bc9c90`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
