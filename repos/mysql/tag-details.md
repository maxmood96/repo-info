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
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
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
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
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
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
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
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:3e646bcda0d9448ffa3d2024eef04e1bca95528ec19b9e8b76749da9d97d4a10
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
$ docker pull mysql@sha256:cc269b0380e0b2e24d5ad0363b6e095b1a73a9175e01de339e8ebafd992aebe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231476460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53ed023c640f3691333cfaab5b10885e657c868d70ef9aaa5986cfa5c5de5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d056aa081a5e7fbec8f34a9ff92fda8e26c6fe70d891378abcf4ed5538311`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5b15159e3d56ea2358b465cbd5786cf22358d22927743a05a2c82c0f43dc44`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151780c6e0c22eda13464b87aec58a1da0056a3e4d4575a79828a290ff2a999b`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 6.4 MB (6445126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1383da285bc32e22d7b773d24a600eba252ef3aac1e4438675d74ae26e9d617`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a22887ef38763adf8d1ba33b8b649c5da678afffb05ad088693f986e15a67`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cfefb73ba0e8d62b606b4cdd11f73f5f1f9549a58895b03580a5ec1d104c01`  
		Last Modified: Sat, 18 Oct 2025 00:14:18 GMT  
		Size: 48.7 MB (48695226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fe86316f647c4bbcaadfcd474d6be0cd53a261eb105c014f643501eea8ca45`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a78bd86d1a3bd04744b22e806453bf4b04be079824b656b1c25866983b62d1`  
		Last Modified: Sat, 18 Oct 2025 00:14:25 GMT  
		Size: 127.5 MB (127502088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbdcc00c87e2124b3815a0a5db919e0c85f1831410ceb217c82b899396c74b6`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2d3914c8f258885ed8d85f8f40edde1c70703a1c59236f308b8c8bb09ad346`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:a746d03db689c7472853b42bcbdaff220e0d03cccddf7632fe66f2bb79b48d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add9fd30bd111a8ad6de73d2ccef4156e18faa51ef1ddbfd735c52bef083410b`

```dockerfile
```

-	Layers:
	-	`sha256:5a57a9f090c11b3a85e9912d5d7453633e146274295c5905a3a7b3289940b8f5`  
		Last Modified: Sat, 18 Oct 2025 03:02:47 GMT  
		Size: 14.5 MB (14526460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22505a6684def24c9fccd333d484cde678dd4576e578b41dd64b404dbdffbf6f`  
		Last Modified: Sat, 18 Oct 2025 03:02:48 GMT  
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
$ docker pull mysql@sha256:3e646bcda0d9448ffa3d2024eef04e1bca95528ec19b9e8b76749da9d97d4a10
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
$ docker pull mysql@sha256:cc269b0380e0b2e24d5ad0363b6e095b1a73a9175e01de339e8ebafd992aebe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231476460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53ed023c640f3691333cfaab5b10885e657c868d70ef9aaa5986cfa5c5de5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d056aa081a5e7fbec8f34a9ff92fda8e26c6fe70d891378abcf4ed5538311`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5b15159e3d56ea2358b465cbd5786cf22358d22927743a05a2c82c0f43dc44`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151780c6e0c22eda13464b87aec58a1da0056a3e4d4575a79828a290ff2a999b`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 6.4 MB (6445126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1383da285bc32e22d7b773d24a600eba252ef3aac1e4438675d74ae26e9d617`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a22887ef38763adf8d1ba33b8b649c5da678afffb05ad088693f986e15a67`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cfefb73ba0e8d62b606b4cdd11f73f5f1f9549a58895b03580a5ec1d104c01`  
		Last Modified: Sat, 18 Oct 2025 00:14:18 GMT  
		Size: 48.7 MB (48695226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fe86316f647c4bbcaadfcd474d6be0cd53a261eb105c014f643501eea8ca45`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a78bd86d1a3bd04744b22e806453bf4b04be079824b656b1c25866983b62d1`  
		Last Modified: Sat, 18 Oct 2025 00:14:25 GMT  
		Size: 127.5 MB (127502088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbdcc00c87e2124b3815a0a5db919e0c85f1831410ceb217c82b899396c74b6`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2d3914c8f258885ed8d85f8f40edde1c70703a1c59236f308b8c8bb09ad346`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a746d03db689c7472853b42bcbdaff220e0d03cccddf7632fe66f2bb79b48d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add9fd30bd111a8ad6de73d2ccef4156e18faa51ef1ddbfd735c52bef083410b`

```dockerfile
```

-	Layers:
	-	`sha256:5a57a9f090c11b3a85e9912d5d7453633e146274295c5905a3a7b3289940b8f5`  
		Last Modified: Sat, 18 Oct 2025 03:02:47 GMT  
		Size: 14.5 MB (14526460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22505a6684def24c9fccd333d484cde678dd4576e578b41dd64b404dbdffbf6f`  
		Last Modified: Sat, 18 Oct 2025 03:02:48 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:3e646bcda0d9448ffa3d2024eef04e1bca95528ec19b9e8b76749da9d97d4a10
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
$ docker pull mysql@sha256:cc269b0380e0b2e24d5ad0363b6e095b1a73a9175e01de339e8ebafd992aebe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231476460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53ed023c640f3691333cfaab5b10885e657c868d70ef9aaa5986cfa5c5de5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d056aa081a5e7fbec8f34a9ff92fda8e26c6fe70d891378abcf4ed5538311`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5b15159e3d56ea2358b465cbd5786cf22358d22927743a05a2c82c0f43dc44`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151780c6e0c22eda13464b87aec58a1da0056a3e4d4575a79828a290ff2a999b`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 6.4 MB (6445126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1383da285bc32e22d7b773d24a600eba252ef3aac1e4438675d74ae26e9d617`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a22887ef38763adf8d1ba33b8b649c5da678afffb05ad088693f986e15a67`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cfefb73ba0e8d62b606b4cdd11f73f5f1f9549a58895b03580a5ec1d104c01`  
		Last Modified: Sat, 18 Oct 2025 00:14:18 GMT  
		Size: 48.7 MB (48695226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fe86316f647c4bbcaadfcd474d6be0cd53a261eb105c014f643501eea8ca45`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a78bd86d1a3bd04744b22e806453bf4b04be079824b656b1c25866983b62d1`  
		Last Modified: Sat, 18 Oct 2025 00:14:25 GMT  
		Size: 127.5 MB (127502088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbdcc00c87e2124b3815a0a5db919e0c85f1831410ceb217c82b899396c74b6`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2d3914c8f258885ed8d85f8f40edde1c70703a1c59236f308b8c8bb09ad346`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a746d03db689c7472853b42bcbdaff220e0d03cccddf7632fe66f2bb79b48d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add9fd30bd111a8ad6de73d2ccef4156e18faa51ef1ddbfd735c52bef083410b`

```dockerfile
```

-	Layers:
	-	`sha256:5a57a9f090c11b3a85e9912d5d7453633e146274295c5905a3a7b3289940b8f5`  
		Last Modified: Sat, 18 Oct 2025 03:02:47 GMT  
		Size: 14.5 MB (14526460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22505a6684def24c9fccd333d484cde678dd4576e578b41dd64b404dbdffbf6f`  
		Last Modified: Sat, 18 Oct 2025 03:02:48 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43`

```console
$ docker pull mysql@sha256:3e646bcda0d9448ffa3d2024eef04e1bca95528ec19b9e8b76749da9d97d4a10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43` - linux; amd64

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

### `mysql:8.0.43` - unknown; unknown

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

### `mysql:8.0.43` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cc269b0380e0b2e24d5ad0363b6e095b1a73a9175e01de339e8ebafd992aebe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231476460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53ed023c640f3691333cfaab5b10885e657c868d70ef9aaa5986cfa5c5de5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d056aa081a5e7fbec8f34a9ff92fda8e26c6fe70d891378abcf4ed5538311`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5b15159e3d56ea2358b465cbd5786cf22358d22927743a05a2c82c0f43dc44`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151780c6e0c22eda13464b87aec58a1da0056a3e4d4575a79828a290ff2a999b`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 6.4 MB (6445126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1383da285bc32e22d7b773d24a600eba252ef3aac1e4438675d74ae26e9d617`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a22887ef38763adf8d1ba33b8b649c5da678afffb05ad088693f986e15a67`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cfefb73ba0e8d62b606b4cdd11f73f5f1f9549a58895b03580a5ec1d104c01`  
		Last Modified: Sat, 18 Oct 2025 00:14:18 GMT  
		Size: 48.7 MB (48695226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fe86316f647c4bbcaadfcd474d6be0cd53a261eb105c014f643501eea8ca45`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a78bd86d1a3bd04744b22e806453bf4b04be079824b656b1c25866983b62d1`  
		Last Modified: Sat, 18 Oct 2025 00:14:25 GMT  
		Size: 127.5 MB (127502088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbdcc00c87e2124b3815a0a5db919e0c85f1831410ceb217c82b899396c74b6`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2d3914c8f258885ed8d85f8f40edde1c70703a1c59236f308b8c8bb09ad346`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43` - unknown; unknown

```console
$ docker pull mysql@sha256:a746d03db689c7472853b42bcbdaff220e0d03cccddf7632fe66f2bb79b48d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add9fd30bd111a8ad6de73d2ccef4156e18faa51ef1ddbfd735c52bef083410b`

```dockerfile
```

-	Layers:
	-	`sha256:5a57a9f090c11b3a85e9912d5d7453633e146274295c5905a3a7b3289940b8f5`  
		Last Modified: Sat, 18 Oct 2025 03:02:47 GMT  
		Size: 14.5 MB (14526460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22505a6684def24c9fccd333d484cde678dd4576e578b41dd64b404dbdffbf6f`  
		Last Modified: Sat, 18 Oct 2025 03:02:48 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-bookworm`

```console
$ docker pull mysql@sha256:bced38c0ca97bd00c8fbc877a019ff141f014608b0762e6e1978cc76e63f473f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.43-bookworm` - linux; amd64

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

### `mysql:8.0.43-bookworm` - unknown; unknown

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

## `mysql:8.0.43-debian`

```console
$ docker pull mysql@sha256:bced38c0ca97bd00c8fbc877a019ff141f014608b0762e6e1978cc76e63f473f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.43-debian` - linux; amd64

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

### `mysql:8.0.43-debian` - unknown; unknown

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

## `mysql:8.0.43-oracle`

```console
$ docker pull mysql@sha256:3e646bcda0d9448ffa3d2024eef04e1bca95528ec19b9e8b76749da9d97d4a10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43-oracle` - linux; amd64

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

### `mysql:8.0.43-oracle` - unknown; unknown

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

### `mysql:8.0.43-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cc269b0380e0b2e24d5ad0363b6e095b1a73a9175e01de339e8ebafd992aebe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231476460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53ed023c640f3691333cfaab5b10885e657c868d70ef9aaa5986cfa5c5de5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d056aa081a5e7fbec8f34a9ff92fda8e26c6fe70d891378abcf4ed5538311`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5b15159e3d56ea2358b465cbd5786cf22358d22927743a05a2c82c0f43dc44`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151780c6e0c22eda13464b87aec58a1da0056a3e4d4575a79828a290ff2a999b`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 6.4 MB (6445126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1383da285bc32e22d7b773d24a600eba252ef3aac1e4438675d74ae26e9d617`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a22887ef38763adf8d1ba33b8b649c5da678afffb05ad088693f986e15a67`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cfefb73ba0e8d62b606b4cdd11f73f5f1f9549a58895b03580a5ec1d104c01`  
		Last Modified: Sat, 18 Oct 2025 00:14:18 GMT  
		Size: 48.7 MB (48695226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fe86316f647c4bbcaadfcd474d6be0cd53a261eb105c014f643501eea8ca45`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a78bd86d1a3bd04744b22e806453bf4b04be079824b656b1c25866983b62d1`  
		Last Modified: Sat, 18 Oct 2025 00:14:25 GMT  
		Size: 127.5 MB (127502088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbdcc00c87e2124b3815a0a5db919e0c85f1831410ceb217c82b899396c74b6`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2d3914c8f258885ed8d85f8f40edde1c70703a1c59236f308b8c8bb09ad346`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a746d03db689c7472853b42bcbdaff220e0d03cccddf7632fe66f2bb79b48d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add9fd30bd111a8ad6de73d2ccef4156e18faa51ef1ddbfd735c52bef083410b`

```dockerfile
```

-	Layers:
	-	`sha256:5a57a9f090c11b3a85e9912d5d7453633e146274295c5905a3a7b3289940b8f5`  
		Last Modified: Sat, 18 Oct 2025 03:02:47 GMT  
		Size: 14.5 MB (14526460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22505a6684def24c9fccd333d484cde678dd4576e578b41dd64b404dbdffbf6f`  
		Last Modified: Sat, 18 Oct 2025 03:02:48 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-oraclelinux9`

```console
$ docker pull mysql@sha256:3e646bcda0d9448ffa3d2024eef04e1bca95528ec19b9e8b76749da9d97d4a10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43-oraclelinux9` - linux; amd64

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

### `mysql:8.0.43-oraclelinux9` - unknown; unknown

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

### `mysql:8.0.43-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cc269b0380e0b2e24d5ad0363b6e095b1a73a9175e01de339e8ebafd992aebe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231476460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53ed023c640f3691333cfaab5b10885e657c868d70ef9aaa5986cfa5c5de5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d056aa081a5e7fbec8f34a9ff92fda8e26c6fe70d891378abcf4ed5538311`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5b15159e3d56ea2358b465cbd5786cf22358d22927743a05a2c82c0f43dc44`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151780c6e0c22eda13464b87aec58a1da0056a3e4d4575a79828a290ff2a999b`  
		Last Modified: Sat, 18 Oct 2025 00:14:16 GMT  
		Size: 6.4 MB (6445126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1383da285bc32e22d7b773d24a600eba252ef3aac1e4438675d74ae26e9d617`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a22887ef38763adf8d1ba33b8b649c5da678afffb05ad088693f986e15a67`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cfefb73ba0e8d62b606b4cdd11f73f5f1f9549a58895b03580a5ec1d104c01`  
		Last Modified: Sat, 18 Oct 2025 00:14:18 GMT  
		Size: 48.7 MB (48695226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fe86316f647c4bbcaadfcd474d6be0cd53a261eb105c014f643501eea8ca45`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a78bd86d1a3bd04744b22e806453bf4b04be079824b656b1c25866983b62d1`  
		Last Modified: Sat, 18 Oct 2025 00:14:25 GMT  
		Size: 127.5 MB (127502088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbdcc00c87e2124b3815a0a5db919e0c85f1831410ceb217c82b899396c74b6`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2d3914c8f258885ed8d85f8f40edde1c70703a1c59236f308b8c8bb09ad346`  
		Last Modified: Sat, 18 Oct 2025 00:14:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a746d03db689c7472853b42bcbdaff220e0d03cccddf7632fe66f2bb79b48d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add9fd30bd111a8ad6de73d2ccef4156e18faa51ef1ddbfd735c52bef083410b`

```dockerfile
```

-	Layers:
	-	`sha256:5a57a9f090c11b3a85e9912d5d7453633e146274295c5905a3a7b3289940b8f5`  
		Last Modified: Sat, 18 Oct 2025 03:02:47 GMT  
		Size: 14.5 MB (14526460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22505a6684def24c9fccd333d484cde678dd4576e578b41dd64b404dbdffbf6f`  
		Last Modified: Sat, 18 Oct 2025 03:02:48 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
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
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
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
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
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
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6` - linux; amd64

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

### `mysql:8.4.6` - unknown; unknown

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

### `mysql:8.4.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6-oracle`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6-oracle` - linux; amd64

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

### `mysql:8.4.6-oracle` - unknown; unknown

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

### `mysql:8.4.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6-oraclelinux9`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6-oraclelinux9` - linux; amd64

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

### `mysql:8.4.6-oraclelinux9` - unknown; unknown

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

### `mysql:8.4.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
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
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
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
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
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
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4` - linux; amd64

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

### `mysql:9.4` - unknown; unknown

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

### `mysql:9.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4-oracle`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4-oracle` - linux; amd64

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

### `mysql:9.4-oracle` - unknown; unknown

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

### `mysql:9.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4-oraclelinux9`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4-oraclelinux9` - linux; amd64

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

### `mysql:9.4-oraclelinux9` - unknown; unknown

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

### `mysql:9.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0` - linux; amd64

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

### `mysql:9.4.0` - unknown; unknown

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

### `mysql:9.4.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0-oracle`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0-oracle` - linux; amd64

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

### `mysql:9.4.0-oracle` - unknown; unknown

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

### `mysql:9.4.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0-oraclelinux9`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0-oraclelinux9` - linux; amd64

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

### `mysql:9.4.0-oraclelinux9` - unknown; unknown

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

### `mysql:9.4.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
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
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
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
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
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
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
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
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
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
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
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
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:869218921e61d6c3c89820955d63cca42971f0e3e6c1e2792247bbd944ebc6e9
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
$ docker pull mysql@sha256:6752fee1ed70df146fe22d5d1656deee79463f780a24cb7e67c807f2f07d7dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcafc5ba1372cb4ae19439f7dcaeb03a7293b1b3521747774b2ab2129aa9ec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2ec98af8e687a4dbabe5e525c410f76ca6ed40876d19dc481d267a90966b4`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0320ac829fef5e46bbafe4e4580a251ea1043b6325090eff0da710d107f2`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914c5eddb3ed2fcfaf0c8fe528d8bfa4f884a491c001253bb57d9e24f28f9cb`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 6.4 MB (6445166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c055c747e2f4a1a0a8ead699b76e4b0b9495435144f1b04fcae77525168b111`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f31a86323e57f3ffc3e740b92e601ae21a6273899ab4657f93a51da39e835ce`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16704bbc5e9eaf2aa3fef4ae9674c563884e0f35463f58fa4e6c9d35a16a99`  
		Last Modified: Sat, 18 Oct 2025 00:13:35 GMT  
		Size: 46.7 MB (46672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b205b72648c7b6dfead38130f1ef63227320661c23d569079397ef24fc589f8`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25829f8e03ef475defd6ac541a1ca69efb91a301f1b1a51668a19484072e1cb5`  
		Last Modified: Sat, 18 Oct 2025 00:45:24 GMT  
		Size: 130.4 MB (130355793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbca8c581605045b420864f98c4a0f1da324b3a5677c9703546d6cc6d25e7cf`  
		Last Modified: Sat, 18 Oct 2025 00:13:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5721a10e9ef0b0d211fa05e45e76a42b17647797b11a85285303f70894a77a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17593aa73fa5130b15c65de22cef334b0b21102243092c6b8120518e47ad5b3f`

```dockerfile
```

-	Layers:
	-	`sha256:22d0f60a5957510d868dc00a704c09005cb6a8eb600134df7ed6aee436e183b0`  
		Last Modified: Sat, 18 Oct 2025 03:02:32 GMT  
		Size: 14.8 MB (14803353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250dad2075df3979ea274500cf6bd14b534dfc9076f391822f9e91ae74ecfa56`  
		Last Modified: Sat, 18 Oct 2025 03:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
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
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:135bc87cce147c3d28cecb9ad270b814cb52805af7ddeea83bfcaf157d05a6b2
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
$ docker pull mysql@sha256:8c56cb68ef853056f066130282909d051b3f91e57a258ed2e641a2c2baa01152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096cde3528fed6701531858fd067925b0fd6f0a38cbcb777b8341393e317940d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9a25427f289ede710dac02ed01e42c53a7400ce58f0def8b3e558b7741e80`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6cfb14ed63d234a07a76dcbe2379c17328b73c39944bb0b5d2263dee06ab6`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e965880b69ca5a95a41e33e3a2386dfdadd9522eefad8da3c7189e5a25b110`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 6.4 MB (6444984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c065f45644751093347ba04d11bd67c9a3553d2c788e84e6ad0c323ebec8a9b7`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20968b0e0ebf36258f3cfb5dd475191a1be2476784da0854885c047574e5d726`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985602c23e955a58859484f6f06125aea7013b01ac773a8bf4fa94c72efa3a23`  
		Last Modified: Sat, 18 Oct 2025 00:13:42 GMT  
		Size: 48.0 MB (48022590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a2a1e05b8638fd23e253dde21caa0d4c6ea0ebfba2e892bd171963b04b3b6b`  
		Last Modified: Sat, 18 Oct 2025 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058de2285f63e6e924e3a8782ed218052f2dde37edffd6d7d093b4559a2aac5`  
		Last Modified: Sat, 18 Oct 2025 00:27:15 GMT  
		Size: 167.3 MB (167251956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be8d9e1441e9d2678d861bc91e75a1ad48e480ac32f554bb67958c8f22904b2`  
		Last Modified: Sat, 18 Oct 2025 00:13:32 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aa68c2ec7d965dca17d6f515a9960ada4b317f382e8c146cb56fbb89569612fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e499eb0c422c8077925ced4bab94530585a90421366df2b792013356d2dd80`

```dockerfile
```

-	Layers:
	-	`sha256:94a5684982ed77ee5b14f1c51f6121a3307541658c55f8308e51cb0c57fd08c8`  
		Last Modified: Sat, 18 Oct 2025 03:03:21 GMT  
		Size: 17.7 MB (17694443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529a8dff19f2d38be74dce03a0257287ee883dfb61e72664b5cc9b9d06defc4`  
		Last Modified: Sat, 18 Oct 2025 03:03:22 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
