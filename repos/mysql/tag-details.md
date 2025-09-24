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
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:4a8843ef1c30d30937dea3cba5b72665bae17051af7a72b1651f3b7681f76aee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:2ffdae66a52f43285d85feee74d706b625486148f06184b8968962df921f49bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94753e67a0a98bc2720e9f672a30a88872ff08168af0b372747c062bb4708c41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e135f0f080d4ea0fa30a590ea7ab0302f76c4e1a078c1a13df54f3f6287290`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0089c875200546b7a0372da6fd012afef288a1492bd047d86e941c38efeb32`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bdefbbef7865bd1f0c8a7ca34b89887bf4dca2b60bd0e87438083d758f2467`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 6.8 MB (6820271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6145eb6907480e5995a123632da26e4036089a95c7cf8f259f9d88b7664b3667`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c5bb883eca1c109aa837e58e51fa4b6e63ec3f3f5fe0946f170036a5e42ddd`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b25d67bc0be5d4e604909e9e75e336d80bd4629cd779182fd7465bdb28a672f`  
		Last Modified: Tue, 23 Sep 2025 23:20:09 GMT  
		Size: 49.8 MB (49837852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729dd3a03ada06467954d69d3c3389343d8add031a0acd72308236042519d06a`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a66f49d571a1c8eeea70ffff7a99a2e0338d0207de8edd4b822fd9b7451c104`  
		Last Modified: Wed, 24 Sep 2025 00:01:00 GMT  
		Size: 128.9 MB (128927373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faf9da2445bda7c3e9a2727ea554d918d1c0bdbf78d90dc475e5550e149a508`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1a0a82ce7ed84dce37200486482040144a08f2c3f6eac4981d3606df015e1`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3e2ad125a1b68e029e3d1bc394c84470a08538047cdeb7eed22de5e340da0193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df025c06cc55e1e82eec1994e2bf0c3af19377f7896e1927644942e30ef3656`

```dockerfile
```

-	Layers:
	-	`sha256:845d658002a994b87efe465abf04881cef927d35837c904d8ff9ee1eb85daf9c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f661dc42977f1b48f778fe13ea802ec2f4c58b23abe90c1db050d6be067db6f`  
		Last Modified: Wed, 24 Sep 2025 00:02:39 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90c625bf2ca9f11b3044b5d8237f45acb73045f1b9bb4fa89f0640e2756f5eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d5362c2625b5239bd020bb517f6cb35b41337b1e327f20702aee8ccdbc4ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb77c7a6435b5bf1f32a775dd2ef1dd176af6742d8d1cda15020b34edd1724`  
		Last Modified: Tue, 23 Sep 2025 21:31:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc2f5fb29fba813920a1ebe2444832da723027c314b5d9336ea58caac95d3fe`  
		Last Modified: Tue, 23 Sep 2025 21:31:15 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932ae097baf062b3d2a18ada853553642576d6d99bf94d6ee0927d66292d1b32`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 6.4 MB (6445343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105207231f26c8ab2def360aaedea014ad9d7ad21b3b1512f5a8de2599035d`  
		Last Modified: Tue, 23 Sep 2025 21:31:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8b8ceea9d7755115e7f0d62b1e04838d901241d34c82e40a91369c36290eb4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f02261ef9b77fe2642f80a8e2aeca6c7d281d1818d7851f26b1383f5f3c7d0`  
		Last Modified: Tue, 23 Sep 2025 21:31:25 GMT  
		Size: 48.7 MB (48694878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f67d38417a516f5db39fedf88657ba690f0ae72c7a2fec516f6392a9a88b4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f47f504c03540e6f54945e1b550392d0ede6cdc48a416137f8800327a1813e`  
		Last Modified: Tue, 23 Sep 2025 21:31:36 GMT  
		Size: 127.5 MB (127506213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cff585f6c01173ce878df74e3b5f3aaf3cec767656594fd18f541c21d93532`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcf37a9b9eb3eb27c36cea668036d3981bd18d1f8fe6d8679dd28f96df00759`  
		Last Modified: Tue, 23 Sep 2025 21:31:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:56610f4b8716448804a02683fd8157a802f5cbc528d70c883ee63f65c7645862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa19dda708fae5eca361a5b862570dbf1508f1531b711c5496a8ce5c5c64b2`

```dockerfile
```

-	Layers:
	-	`sha256:d9334d025fa4a425b5e14d71c67f8f08b388658429456aad894cc50f35ec83b0`  
		Last Modified: Wed, 24 Sep 2025 00:02:50 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fee2d8045e33bcd84c48f0f6633627b31bd507c0849367b838fac9b699d4234`  
		Last Modified: Wed, 24 Sep 2025 00:02:51 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:0d58619ea4f3eac1239eb28fabea6a3ac63a48f02b7c09432bcd8b9b1072103d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:013929037ffb70560a09cad0d894ca38a9ae39e85fd0a0cb447bb6ab7bbab108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183355349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94e90b3b544aff194e0e3492e2b1a7dd245ddf5e085d6aea160af75071d8cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164ec1d8c652a7023052680e5d26b41192c5ae4ff5e45cfbefad60a3b4f66ad9`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5783293e6dca55031fd024f5decdcb2ac20e0f98ee7e15af96eef975817aab7b`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 4.4 MB (4423019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24cabaf89039de2cdab0fd81449cc0edb63fdd956e957091206ea1df78fa60e`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 1.2 MB (1248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb735fbc5d08b96c7789357010298be1319dfececf3175ffbdb9d77c7d6ff8c`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb1861cbf9571305399f9c21349ad32a44da06087bf9914c2921e4ecf1ddb6f`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 15.3 MB (15294814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b17feb8f203f6015f89083f8a1e1b4e4baae1b0f4a6fc2e194e5262bb473a`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cba180c360db0a2e74e1ae731a625d9ff581d032515422241ab67fb9cd6a58`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24ddf760b0130da70466350a2224d7a6c64af9c5208240a63fb15bc3d107711`  
		Last Modified: Wed, 24 Sep 2025 00:03:14 GMT  
		Size: 134.2 MB (134150247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1671fc54690073c9c1efd0fc918cdf06531096363342fb0318bd22e7e1b1579e`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96481d96cb6f4f1557b01584ba75b01d7c3a7712ea690a40b3aec9f40428ed3b`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a99fddba17740de71034ef653d83fbe42e577d6e5c30137978c5f0108b1cb`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:5151e298e24e5d0c234e964e517b06e10ad3abe9a5dc01c2b9b304a05fe1253e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d58abb1460e6732dd346879d9a9922cd84b62384e293c665bb8899722514c5`

```dockerfile
```

-	Layers:
	-	`sha256:668557f7fec4433d079911b76def280d7a7293774f1825faeb57d155ee492460`  
		Last Modified: Wed, 24 Sep 2025 00:02:44 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f089fb47ec8ef8273681c8a0acba2616e01e62afda4ff694f1e21c96ec870a`  
		Last Modified: Wed, 24 Sep 2025 00:02:45 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:0d58619ea4f3eac1239eb28fabea6a3ac63a48f02b7c09432bcd8b9b1072103d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:013929037ffb70560a09cad0d894ca38a9ae39e85fd0a0cb447bb6ab7bbab108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183355349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94e90b3b544aff194e0e3492e2b1a7dd245ddf5e085d6aea160af75071d8cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164ec1d8c652a7023052680e5d26b41192c5ae4ff5e45cfbefad60a3b4f66ad9`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5783293e6dca55031fd024f5decdcb2ac20e0f98ee7e15af96eef975817aab7b`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 4.4 MB (4423019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24cabaf89039de2cdab0fd81449cc0edb63fdd956e957091206ea1df78fa60e`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 1.2 MB (1248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb735fbc5d08b96c7789357010298be1319dfececf3175ffbdb9d77c7d6ff8c`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb1861cbf9571305399f9c21349ad32a44da06087bf9914c2921e4ecf1ddb6f`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 15.3 MB (15294814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b17feb8f203f6015f89083f8a1e1b4e4baae1b0f4a6fc2e194e5262bb473a`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cba180c360db0a2e74e1ae731a625d9ff581d032515422241ab67fb9cd6a58`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24ddf760b0130da70466350a2224d7a6c64af9c5208240a63fb15bc3d107711`  
		Last Modified: Wed, 24 Sep 2025 00:03:14 GMT  
		Size: 134.2 MB (134150247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1671fc54690073c9c1efd0fc918cdf06531096363342fb0318bd22e7e1b1579e`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96481d96cb6f4f1557b01584ba75b01d7c3a7712ea690a40b3aec9f40428ed3b`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a99fddba17740de71034ef653d83fbe42e577d6e5c30137978c5f0108b1cb`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:5151e298e24e5d0c234e964e517b06e10ad3abe9a5dc01c2b9b304a05fe1253e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d58abb1460e6732dd346879d9a9922cd84b62384e293c665bb8899722514c5`

```dockerfile
```

-	Layers:
	-	`sha256:668557f7fec4433d079911b76def280d7a7293774f1825faeb57d155ee492460`  
		Last Modified: Wed, 24 Sep 2025 00:02:44 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f089fb47ec8ef8273681c8a0acba2616e01e62afda4ff694f1e21c96ec870a`  
		Last Modified: Wed, 24 Sep 2025 00:02:45 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:4a8843ef1c30d30937dea3cba5b72665bae17051af7a72b1651f3b7681f76aee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2ffdae66a52f43285d85feee74d706b625486148f06184b8968962df921f49bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94753e67a0a98bc2720e9f672a30a88872ff08168af0b372747c062bb4708c41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e135f0f080d4ea0fa30a590ea7ab0302f76c4e1a078c1a13df54f3f6287290`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0089c875200546b7a0372da6fd012afef288a1492bd047d86e941c38efeb32`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bdefbbef7865bd1f0c8a7ca34b89887bf4dca2b60bd0e87438083d758f2467`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 6.8 MB (6820271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6145eb6907480e5995a123632da26e4036089a95c7cf8f259f9d88b7664b3667`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c5bb883eca1c109aa837e58e51fa4b6e63ec3f3f5fe0946f170036a5e42ddd`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b25d67bc0be5d4e604909e9e75e336d80bd4629cd779182fd7465bdb28a672f`  
		Last Modified: Tue, 23 Sep 2025 23:20:09 GMT  
		Size: 49.8 MB (49837852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729dd3a03ada06467954d69d3c3389343d8add031a0acd72308236042519d06a`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a66f49d571a1c8eeea70ffff7a99a2e0338d0207de8edd4b822fd9b7451c104`  
		Last Modified: Wed, 24 Sep 2025 00:01:00 GMT  
		Size: 128.9 MB (128927373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faf9da2445bda7c3e9a2727ea554d918d1c0bdbf78d90dc475e5550e149a508`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1a0a82ce7ed84dce37200486482040144a08f2c3f6eac4981d3606df015e1`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3e2ad125a1b68e029e3d1bc394c84470a08538047cdeb7eed22de5e340da0193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df025c06cc55e1e82eec1994e2bf0c3af19377f7896e1927644942e30ef3656`

```dockerfile
```

-	Layers:
	-	`sha256:845d658002a994b87efe465abf04881cef927d35837c904d8ff9ee1eb85daf9c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f661dc42977f1b48f778fe13ea802ec2f4c58b23abe90c1db050d6be067db6f`  
		Last Modified: Wed, 24 Sep 2025 00:02:39 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90c625bf2ca9f11b3044b5d8237f45acb73045f1b9bb4fa89f0640e2756f5eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d5362c2625b5239bd020bb517f6cb35b41337b1e327f20702aee8ccdbc4ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb77c7a6435b5bf1f32a775dd2ef1dd176af6742d8d1cda15020b34edd1724`  
		Last Modified: Tue, 23 Sep 2025 21:31:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc2f5fb29fba813920a1ebe2444832da723027c314b5d9336ea58caac95d3fe`  
		Last Modified: Tue, 23 Sep 2025 21:31:15 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932ae097baf062b3d2a18ada853553642576d6d99bf94d6ee0927d66292d1b32`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 6.4 MB (6445343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105207231f26c8ab2def360aaedea014ad9d7ad21b3b1512f5a8de2599035d`  
		Last Modified: Tue, 23 Sep 2025 21:31:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8b8ceea9d7755115e7f0d62b1e04838d901241d34c82e40a91369c36290eb4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f02261ef9b77fe2642f80a8e2aeca6c7d281d1818d7851f26b1383f5f3c7d0`  
		Last Modified: Tue, 23 Sep 2025 21:31:25 GMT  
		Size: 48.7 MB (48694878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f67d38417a516f5db39fedf88657ba690f0ae72c7a2fec516f6392a9a88b4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f47f504c03540e6f54945e1b550392d0ede6cdc48a416137f8800327a1813e`  
		Last Modified: Tue, 23 Sep 2025 21:31:36 GMT  
		Size: 127.5 MB (127506213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cff585f6c01173ce878df74e3b5f3aaf3cec767656594fd18f541c21d93532`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcf37a9b9eb3eb27c36cea668036d3981bd18d1f8fe6d8679dd28f96df00759`  
		Last Modified: Tue, 23 Sep 2025 21:31:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:56610f4b8716448804a02683fd8157a802f5cbc528d70c883ee63f65c7645862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa19dda708fae5eca361a5b862570dbf1508f1531b711c5496a8ce5c5c64b2`

```dockerfile
```

-	Layers:
	-	`sha256:d9334d025fa4a425b5e14d71c67f8f08b388658429456aad894cc50f35ec83b0`  
		Last Modified: Wed, 24 Sep 2025 00:02:50 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fee2d8045e33bcd84c48f0f6633627b31bd507c0849367b838fac9b699d4234`  
		Last Modified: Wed, 24 Sep 2025 00:02:51 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:4a8843ef1c30d30937dea3cba5b72665bae17051af7a72b1651f3b7681f76aee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2ffdae66a52f43285d85feee74d706b625486148f06184b8968962df921f49bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94753e67a0a98bc2720e9f672a30a88872ff08168af0b372747c062bb4708c41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e135f0f080d4ea0fa30a590ea7ab0302f76c4e1a078c1a13df54f3f6287290`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0089c875200546b7a0372da6fd012afef288a1492bd047d86e941c38efeb32`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bdefbbef7865bd1f0c8a7ca34b89887bf4dca2b60bd0e87438083d758f2467`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 6.8 MB (6820271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6145eb6907480e5995a123632da26e4036089a95c7cf8f259f9d88b7664b3667`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c5bb883eca1c109aa837e58e51fa4b6e63ec3f3f5fe0946f170036a5e42ddd`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b25d67bc0be5d4e604909e9e75e336d80bd4629cd779182fd7465bdb28a672f`  
		Last Modified: Tue, 23 Sep 2025 23:20:09 GMT  
		Size: 49.8 MB (49837852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729dd3a03ada06467954d69d3c3389343d8add031a0acd72308236042519d06a`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a66f49d571a1c8eeea70ffff7a99a2e0338d0207de8edd4b822fd9b7451c104`  
		Last Modified: Wed, 24 Sep 2025 00:01:00 GMT  
		Size: 128.9 MB (128927373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faf9da2445bda7c3e9a2727ea554d918d1c0bdbf78d90dc475e5550e149a508`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1a0a82ce7ed84dce37200486482040144a08f2c3f6eac4981d3606df015e1`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3e2ad125a1b68e029e3d1bc394c84470a08538047cdeb7eed22de5e340da0193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df025c06cc55e1e82eec1994e2bf0c3af19377f7896e1927644942e30ef3656`

```dockerfile
```

-	Layers:
	-	`sha256:845d658002a994b87efe465abf04881cef927d35837c904d8ff9ee1eb85daf9c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f661dc42977f1b48f778fe13ea802ec2f4c58b23abe90c1db050d6be067db6f`  
		Last Modified: Wed, 24 Sep 2025 00:02:39 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90c625bf2ca9f11b3044b5d8237f45acb73045f1b9bb4fa89f0640e2756f5eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d5362c2625b5239bd020bb517f6cb35b41337b1e327f20702aee8ccdbc4ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb77c7a6435b5bf1f32a775dd2ef1dd176af6742d8d1cda15020b34edd1724`  
		Last Modified: Tue, 23 Sep 2025 21:31:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc2f5fb29fba813920a1ebe2444832da723027c314b5d9336ea58caac95d3fe`  
		Last Modified: Tue, 23 Sep 2025 21:31:15 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932ae097baf062b3d2a18ada853553642576d6d99bf94d6ee0927d66292d1b32`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 6.4 MB (6445343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105207231f26c8ab2def360aaedea014ad9d7ad21b3b1512f5a8de2599035d`  
		Last Modified: Tue, 23 Sep 2025 21:31:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8b8ceea9d7755115e7f0d62b1e04838d901241d34c82e40a91369c36290eb4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f02261ef9b77fe2642f80a8e2aeca6c7d281d1818d7851f26b1383f5f3c7d0`  
		Last Modified: Tue, 23 Sep 2025 21:31:25 GMT  
		Size: 48.7 MB (48694878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f67d38417a516f5db39fedf88657ba690f0ae72c7a2fec516f6392a9a88b4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f47f504c03540e6f54945e1b550392d0ede6cdc48a416137f8800327a1813e`  
		Last Modified: Tue, 23 Sep 2025 21:31:36 GMT  
		Size: 127.5 MB (127506213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cff585f6c01173ce878df74e3b5f3aaf3cec767656594fd18f541c21d93532`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcf37a9b9eb3eb27c36cea668036d3981bd18d1f8fe6d8679dd28f96df00759`  
		Last Modified: Tue, 23 Sep 2025 21:31:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:56610f4b8716448804a02683fd8157a802f5cbc528d70c883ee63f65c7645862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa19dda708fae5eca361a5b862570dbf1508f1531b711c5496a8ce5c5c64b2`

```dockerfile
```

-	Layers:
	-	`sha256:d9334d025fa4a425b5e14d71c67f8f08b388658429456aad894cc50f35ec83b0`  
		Last Modified: Wed, 24 Sep 2025 00:02:50 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fee2d8045e33bcd84c48f0f6633627b31bd507c0849367b838fac9b699d4234`  
		Last Modified: Wed, 24 Sep 2025 00:02:51 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43`

```console
$ docker pull mysql@sha256:4a8843ef1c30d30937dea3cba5b72665bae17051af7a72b1651f3b7681f76aee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43` - linux; amd64

```console
$ docker pull mysql@sha256:2ffdae66a52f43285d85feee74d706b625486148f06184b8968962df921f49bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94753e67a0a98bc2720e9f672a30a88872ff08168af0b372747c062bb4708c41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e135f0f080d4ea0fa30a590ea7ab0302f76c4e1a078c1a13df54f3f6287290`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0089c875200546b7a0372da6fd012afef288a1492bd047d86e941c38efeb32`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bdefbbef7865bd1f0c8a7ca34b89887bf4dca2b60bd0e87438083d758f2467`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 6.8 MB (6820271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6145eb6907480e5995a123632da26e4036089a95c7cf8f259f9d88b7664b3667`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c5bb883eca1c109aa837e58e51fa4b6e63ec3f3f5fe0946f170036a5e42ddd`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b25d67bc0be5d4e604909e9e75e336d80bd4629cd779182fd7465bdb28a672f`  
		Last Modified: Tue, 23 Sep 2025 23:20:09 GMT  
		Size: 49.8 MB (49837852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729dd3a03ada06467954d69d3c3389343d8add031a0acd72308236042519d06a`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a66f49d571a1c8eeea70ffff7a99a2e0338d0207de8edd4b822fd9b7451c104`  
		Last Modified: Wed, 24 Sep 2025 00:01:00 GMT  
		Size: 128.9 MB (128927373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faf9da2445bda7c3e9a2727ea554d918d1c0bdbf78d90dc475e5550e149a508`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1a0a82ce7ed84dce37200486482040144a08f2c3f6eac4981d3606df015e1`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43` - unknown; unknown

```console
$ docker pull mysql@sha256:3e2ad125a1b68e029e3d1bc394c84470a08538047cdeb7eed22de5e340da0193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df025c06cc55e1e82eec1994e2bf0c3af19377f7896e1927644942e30ef3656`

```dockerfile
```

-	Layers:
	-	`sha256:845d658002a994b87efe465abf04881cef927d35837c904d8ff9ee1eb85daf9c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f661dc42977f1b48f778fe13ea802ec2f4c58b23abe90c1db050d6be067db6f`  
		Last Modified: Wed, 24 Sep 2025 00:02:39 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90c625bf2ca9f11b3044b5d8237f45acb73045f1b9bb4fa89f0640e2756f5eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d5362c2625b5239bd020bb517f6cb35b41337b1e327f20702aee8ccdbc4ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb77c7a6435b5bf1f32a775dd2ef1dd176af6742d8d1cda15020b34edd1724`  
		Last Modified: Tue, 23 Sep 2025 21:31:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc2f5fb29fba813920a1ebe2444832da723027c314b5d9336ea58caac95d3fe`  
		Last Modified: Tue, 23 Sep 2025 21:31:15 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932ae097baf062b3d2a18ada853553642576d6d99bf94d6ee0927d66292d1b32`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 6.4 MB (6445343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105207231f26c8ab2def360aaedea014ad9d7ad21b3b1512f5a8de2599035d`  
		Last Modified: Tue, 23 Sep 2025 21:31:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8b8ceea9d7755115e7f0d62b1e04838d901241d34c82e40a91369c36290eb4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f02261ef9b77fe2642f80a8e2aeca6c7d281d1818d7851f26b1383f5f3c7d0`  
		Last Modified: Tue, 23 Sep 2025 21:31:25 GMT  
		Size: 48.7 MB (48694878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f67d38417a516f5db39fedf88657ba690f0ae72c7a2fec516f6392a9a88b4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f47f504c03540e6f54945e1b550392d0ede6cdc48a416137f8800327a1813e`  
		Last Modified: Tue, 23 Sep 2025 21:31:36 GMT  
		Size: 127.5 MB (127506213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cff585f6c01173ce878df74e3b5f3aaf3cec767656594fd18f541c21d93532`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcf37a9b9eb3eb27c36cea668036d3981bd18d1f8fe6d8679dd28f96df00759`  
		Last Modified: Tue, 23 Sep 2025 21:31:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43` - unknown; unknown

```console
$ docker pull mysql@sha256:56610f4b8716448804a02683fd8157a802f5cbc528d70c883ee63f65c7645862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa19dda708fae5eca361a5b862570dbf1508f1531b711c5496a8ce5c5c64b2`

```dockerfile
```

-	Layers:
	-	`sha256:d9334d025fa4a425b5e14d71c67f8f08b388658429456aad894cc50f35ec83b0`  
		Last Modified: Wed, 24 Sep 2025 00:02:50 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fee2d8045e33bcd84c48f0f6633627b31bd507c0849367b838fac9b699d4234`  
		Last Modified: Wed, 24 Sep 2025 00:02:51 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-bookworm`

```console
$ docker pull mysql@sha256:0d58619ea4f3eac1239eb28fabea6a3ac63a48f02b7c09432bcd8b9b1072103d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.43-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:013929037ffb70560a09cad0d894ca38a9ae39e85fd0a0cb447bb6ab7bbab108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183355349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94e90b3b544aff194e0e3492e2b1a7dd245ddf5e085d6aea160af75071d8cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164ec1d8c652a7023052680e5d26b41192c5ae4ff5e45cfbefad60a3b4f66ad9`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5783293e6dca55031fd024f5decdcb2ac20e0f98ee7e15af96eef975817aab7b`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 4.4 MB (4423019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24cabaf89039de2cdab0fd81449cc0edb63fdd956e957091206ea1df78fa60e`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 1.2 MB (1248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb735fbc5d08b96c7789357010298be1319dfececf3175ffbdb9d77c7d6ff8c`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb1861cbf9571305399f9c21349ad32a44da06087bf9914c2921e4ecf1ddb6f`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 15.3 MB (15294814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b17feb8f203f6015f89083f8a1e1b4e4baae1b0f4a6fc2e194e5262bb473a`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cba180c360db0a2e74e1ae731a625d9ff581d032515422241ab67fb9cd6a58`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24ddf760b0130da70466350a2224d7a6c64af9c5208240a63fb15bc3d107711`  
		Last Modified: Wed, 24 Sep 2025 00:03:14 GMT  
		Size: 134.2 MB (134150247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1671fc54690073c9c1efd0fc918cdf06531096363342fb0318bd22e7e1b1579e`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96481d96cb6f4f1557b01584ba75b01d7c3a7712ea690a40b3aec9f40428ed3b`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a99fddba17740de71034ef653d83fbe42e577d6e5c30137978c5f0108b1cb`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:5151e298e24e5d0c234e964e517b06e10ad3abe9a5dc01c2b9b304a05fe1253e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d58abb1460e6732dd346879d9a9922cd84b62384e293c665bb8899722514c5`

```dockerfile
```

-	Layers:
	-	`sha256:668557f7fec4433d079911b76def280d7a7293774f1825faeb57d155ee492460`  
		Last Modified: Wed, 24 Sep 2025 00:02:44 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f089fb47ec8ef8273681c8a0acba2616e01e62afda4ff694f1e21c96ec870a`  
		Last Modified: Wed, 24 Sep 2025 00:02:45 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-debian`

```console
$ docker pull mysql@sha256:0d58619ea4f3eac1239eb28fabea6a3ac63a48f02b7c09432bcd8b9b1072103d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.43-debian` - linux; amd64

```console
$ docker pull mysql@sha256:013929037ffb70560a09cad0d894ca38a9ae39e85fd0a0cb447bb6ab7bbab108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183355349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94e90b3b544aff194e0e3492e2b1a7dd245ddf5e085d6aea160af75071d8cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164ec1d8c652a7023052680e5d26b41192c5ae4ff5e45cfbefad60a3b4f66ad9`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5783293e6dca55031fd024f5decdcb2ac20e0f98ee7e15af96eef975817aab7b`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 4.4 MB (4423019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24cabaf89039de2cdab0fd81449cc0edb63fdd956e957091206ea1df78fa60e`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 1.2 MB (1248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb735fbc5d08b96c7789357010298be1319dfececf3175ffbdb9d77c7d6ff8c`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb1861cbf9571305399f9c21349ad32a44da06087bf9914c2921e4ecf1ddb6f`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 15.3 MB (15294814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b17feb8f203f6015f89083f8a1e1b4e4baae1b0f4a6fc2e194e5262bb473a`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cba180c360db0a2e74e1ae731a625d9ff581d032515422241ab67fb9cd6a58`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24ddf760b0130da70466350a2224d7a6c64af9c5208240a63fb15bc3d107711`  
		Last Modified: Wed, 24 Sep 2025 00:03:14 GMT  
		Size: 134.2 MB (134150247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1671fc54690073c9c1efd0fc918cdf06531096363342fb0318bd22e7e1b1579e`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96481d96cb6f4f1557b01584ba75b01d7c3a7712ea690a40b3aec9f40428ed3b`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a99fddba17740de71034ef653d83fbe42e577d6e5c30137978c5f0108b1cb`  
		Last Modified: Tue, 23 Sep 2025 23:19:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:5151e298e24e5d0c234e964e517b06e10ad3abe9a5dc01c2b9b304a05fe1253e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d58abb1460e6732dd346879d9a9922cd84b62384e293c665bb8899722514c5`

```dockerfile
```

-	Layers:
	-	`sha256:668557f7fec4433d079911b76def280d7a7293774f1825faeb57d155ee492460`  
		Last Modified: Wed, 24 Sep 2025 00:02:44 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f089fb47ec8ef8273681c8a0acba2616e01e62afda4ff694f1e21c96ec870a`  
		Last Modified: Wed, 24 Sep 2025 00:02:45 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-oracle`

```console
$ docker pull mysql@sha256:4a8843ef1c30d30937dea3cba5b72665bae17051af7a72b1651f3b7681f76aee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2ffdae66a52f43285d85feee74d706b625486148f06184b8968962df921f49bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94753e67a0a98bc2720e9f672a30a88872ff08168af0b372747c062bb4708c41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e135f0f080d4ea0fa30a590ea7ab0302f76c4e1a078c1a13df54f3f6287290`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0089c875200546b7a0372da6fd012afef288a1492bd047d86e941c38efeb32`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bdefbbef7865bd1f0c8a7ca34b89887bf4dca2b60bd0e87438083d758f2467`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 6.8 MB (6820271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6145eb6907480e5995a123632da26e4036089a95c7cf8f259f9d88b7664b3667`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c5bb883eca1c109aa837e58e51fa4b6e63ec3f3f5fe0946f170036a5e42ddd`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b25d67bc0be5d4e604909e9e75e336d80bd4629cd779182fd7465bdb28a672f`  
		Last Modified: Tue, 23 Sep 2025 23:20:09 GMT  
		Size: 49.8 MB (49837852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729dd3a03ada06467954d69d3c3389343d8add031a0acd72308236042519d06a`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a66f49d571a1c8eeea70ffff7a99a2e0338d0207de8edd4b822fd9b7451c104`  
		Last Modified: Wed, 24 Sep 2025 00:01:00 GMT  
		Size: 128.9 MB (128927373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faf9da2445bda7c3e9a2727ea554d918d1c0bdbf78d90dc475e5550e149a508`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1a0a82ce7ed84dce37200486482040144a08f2c3f6eac4981d3606df015e1`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3e2ad125a1b68e029e3d1bc394c84470a08538047cdeb7eed22de5e340da0193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df025c06cc55e1e82eec1994e2bf0c3af19377f7896e1927644942e30ef3656`

```dockerfile
```

-	Layers:
	-	`sha256:845d658002a994b87efe465abf04881cef927d35837c904d8ff9ee1eb85daf9c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f661dc42977f1b48f778fe13ea802ec2f4c58b23abe90c1db050d6be067db6f`  
		Last Modified: Wed, 24 Sep 2025 00:02:39 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90c625bf2ca9f11b3044b5d8237f45acb73045f1b9bb4fa89f0640e2756f5eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d5362c2625b5239bd020bb517f6cb35b41337b1e327f20702aee8ccdbc4ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb77c7a6435b5bf1f32a775dd2ef1dd176af6742d8d1cda15020b34edd1724`  
		Last Modified: Tue, 23 Sep 2025 21:31:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc2f5fb29fba813920a1ebe2444832da723027c314b5d9336ea58caac95d3fe`  
		Last Modified: Tue, 23 Sep 2025 21:31:15 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932ae097baf062b3d2a18ada853553642576d6d99bf94d6ee0927d66292d1b32`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 6.4 MB (6445343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105207231f26c8ab2def360aaedea014ad9d7ad21b3b1512f5a8de2599035d`  
		Last Modified: Tue, 23 Sep 2025 21:31:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8b8ceea9d7755115e7f0d62b1e04838d901241d34c82e40a91369c36290eb4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f02261ef9b77fe2642f80a8e2aeca6c7d281d1818d7851f26b1383f5f3c7d0`  
		Last Modified: Tue, 23 Sep 2025 21:31:25 GMT  
		Size: 48.7 MB (48694878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f67d38417a516f5db39fedf88657ba690f0ae72c7a2fec516f6392a9a88b4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f47f504c03540e6f54945e1b550392d0ede6cdc48a416137f8800327a1813e`  
		Last Modified: Tue, 23 Sep 2025 21:31:36 GMT  
		Size: 127.5 MB (127506213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cff585f6c01173ce878df74e3b5f3aaf3cec767656594fd18f541c21d93532`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcf37a9b9eb3eb27c36cea668036d3981bd18d1f8fe6d8679dd28f96df00759`  
		Last Modified: Tue, 23 Sep 2025 21:31:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:56610f4b8716448804a02683fd8157a802f5cbc528d70c883ee63f65c7645862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa19dda708fae5eca361a5b862570dbf1508f1531b711c5496a8ce5c5c64b2`

```dockerfile
```

-	Layers:
	-	`sha256:d9334d025fa4a425b5e14d71c67f8f08b388658429456aad894cc50f35ec83b0`  
		Last Modified: Wed, 24 Sep 2025 00:02:50 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fee2d8045e33bcd84c48f0f6633627b31bd507c0849367b838fac9b699d4234`  
		Last Modified: Wed, 24 Sep 2025 00:02:51 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-oraclelinux9`

```console
$ docker pull mysql@sha256:4a8843ef1c30d30937dea3cba5b72665bae17051af7a72b1651f3b7681f76aee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2ffdae66a52f43285d85feee74d706b625486148f06184b8968962df921f49bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94753e67a0a98bc2720e9f672a30a88872ff08168af0b372747c062bb4708c41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e135f0f080d4ea0fa30a590ea7ab0302f76c4e1a078c1a13df54f3f6287290`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0089c875200546b7a0372da6fd012afef288a1492bd047d86e941c38efeb32`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bdefbbef7865bd1f0c8a7ca34b89887bf4dca2b60bd0e87438083d758f2467`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 6.8 MB (6820271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6145eb6907480e5995a123632da26e4036089a95c7cf8f259f9d88b7664b3667`  
		Last Modified: Tue, 23 Sep 2025 23:20:04 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c5bb883eca1c109aa837e58e51fa4b6e63ec3f3f5fe0946f170036a5e42ddd`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b25d67bc0be5d4e604909e9e75e336d80bd4629cd779182fd7465bdb28a672f`  
		Last Modified: Tue, 23 Sep 2025 23:20:09 GMT  
		Size: 49.8 MB (49837852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729dd3a03ada06467954d69d3c3389343d8add031a0acd72308236042519d06a`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a66f49d571a1c8eeea70ffff7a99a2e0338d0207de8edd4b822fd9b7451c104`  
		Last Modified: Wed, 24 Sep 2025 00:01:00 GMT  
		Size: 128.9 MB (128927373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faf9da2445bda7c3e9a2727ea554d918d1c0bdbf78d90dc475e5550e149a508`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1a0a82ce7ed84dce37200486482040144a08f2c3f6eac4981d3606df015e1`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3e2ad125a1b68e029e3d1bc394c84470a08538047cdeb7eed22de5e340da0193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df025c06cc55e1e82eec1994e2bf0c3af19377f7896e1927644942e30ef3656`

```dockerfile
```

-	Layers:
	-	`sha256:845d658002a994b87efe465abf04881cef927d35837c904d8ff9ee1eb85daf9c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f661dc42977f1b48f778fe13ea802ec2f4c58b23abe90c1db050d6be067db6f`  
		Last Modified: Wed, 24 Sep 2025 00:02:39 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90c625bf2ca9f11b3044b5d8237f45acb73045f1b9bb4fa89f0640e2756f5eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d5362c2625b5239bd020bb517f6cb35b41337b1e327f20702aee8ccdbc4ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb77c7a6435b5bf1f32a775dd2ef1dd176af6742d8d1cda15020b34edd1724`  
		Last Modified: Tue, 23 Sep 2025 21:31:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc2f5fb29fba813920a1ebe2444832da723027c314b5d9336ea58caac95d3fe`  
		Last Modified: Tue, 23 Sep 2025 21:31:15 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932ae097baf062b3d2a18ada853553642576d6d99bf94d6ee0927d66292d1b32`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 6.4 MB (6445343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105207231f26c8ab2def360aaedea014ad9d7ad21b3b1512f5a8de2599035d`  
		Last Modified: Tue, 23 Sep 2025 21:31:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8b8ceea9d7755115e7f0d62b1e04838d901241d34c82e40a91369c36290eb4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f02261ef9b77fe2642f80a8e2aeca6c7d281d1818d7851f26b1383f5f3c7d0`  
		Last Modified: Tue, 23 Sep 2025 21:31:25 GMT  
		Size: 48.7 MB (48694878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f67d38417a516f5db39fedf88657ba690f0ae72c7a2fec516f6392a9a88b4`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f47f504c03540e6f54945e1b550392d0ede6cdc48a416137f8800327a1813e`  
		Last Modified: Tue, 23 Sep 2025 21:31:36 GMT  
		Size: 127.5 MB (127506213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cff585f6c01173ce878df74e3b5f3aaf3cec767656594fd18f541c21d93532`  
		Last Modified: Tue, 23 Sep 2025 21:31:17 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcf37a9b9eb3eb27c36cea668036d3981bd18d1f8fe6d8679dd28f96df00759`  
		Last Modified: Tue, 23 Sep 2025 21:31:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:56610f4b8716448804a02683fd8157a802f5cbc528d70c883ee63f65c7645862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa19dda708fae5eca361a5b862570dbf1508f1531b711c5496a8ce5c5c64b2`

```dockerfile
```

-	Layers:
	-	`sha256:d9334d025fa4a425b5e14d71c67f8f08b388658429456aad894cc50f35ec83b0`  
		Last Modified: Wed, 24 Sep 2025 00:02:50 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fee2d8045e33bcd84c48f0f6633627b31bd507c0849367b838fac9b699d4234`  
		Last Modified: Wed, 24 Sep 2025 00:02:51 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6-oracle`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6-oraclelinux9`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4-oracle`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4-oraclelinux9`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0-oracle`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0-oraclelinux9`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:5367102acfefeaa47eb0eb57c8d4f8b96c8c14004859131eac9bbfaa62f81e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:46f74fc1ee06f3fb9713fe30e1cd3eb52d5a85acf5ebf62b05067f74391e0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236859793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf2b3f8428ea11f3ae9e971b7f826356716e6bd71a5e04b52b8f8276ba7a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f697f30e8095d989abe5e1de06d93dcc0021dc7204919727e2eca6701a4d7`  
		Last Modified: Tue, 23 Sep 2025 23:23:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389b884d3d6ce766532122199602201252dadcb7881b5d21b8b463e721f4ba6`  
		Last Modified: Tue, 23 Sep 2025 23:23:28 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69718387e824905d01652b4965aa12e418f5e08d8373cd23836e6454013975e4`  
		Last Modified: Tue, 23 Sep 2025 23:23:25 GMT  
		Size: 6.8 MB (6820300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc946e9b73316ab14cd7c8306a3f28c300d21df9cbd6672a86a3fed3065a0f`  
		Last Modified: Tue, 23 Sep 2025 23:23:27 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b4bec6f690eb2fed680a997b36a10c3a00babf8357aebeb689265fb96b904`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99a8dca35c437bd292b4f556645c0bcbadce6eb56e1b5b89fb13f46e33fcb5`  
		Last Modified: Tue, 23 Sep 2025 23:23:40 GMT  
		Size: 47.8 MB (47786305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a745903ff9c7ef0b5a0ea49337bdfbcab819d9e41c4db29bc665ef605e5a04`  
		Last Modified: Tue, 23 Sep 2025 23:23:21 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ec30544fc8f8e83f68b37b1ddcb7abb8bdf0172eb4a29e7a7aed3db4fa78c`  
		Last Modified: Tue, 23 Sep 2025 23:23:44 GMT  
		Size: 132.0 MB (131963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5b31c795a3486e6347973a20a03cd6d6a7a73be20fa9fac59f1074eca84f9`  
		Last Modified: Tue, 23 Sep 2025 23:23:24 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3d430fb0a49d3264fedbdde170f4a87c1fefdee0ee2d367975f900e075883e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2949ac188bf46189cba97364c241096a28397c92796f3c0bb4de6dafb097a`

```dockerfile
```

-	Layers:
	-	`sha256:643f546e0b639901cc3cb00fef0bad974f3102ac52e54f4f27b4586ba385604c`  
		Last Modified: Wed, 24 Sep 2025 00:02:38 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1100367841f6dffcf617bcdce9ee19c2587e78417f41c183e4f687d6df9eb998`  
		Last Modified: Wed, 24 Sep 2025 00:02:40 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:52f1bba14ac67b5035078d20454cd0aa8657558869326c41938ff04c9c69eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5996048b834723a19fdee049c5dd822cfea85350b3aa4e78e00e93e5bd8ab65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb75117faeac1db3f481c1ecb2e9d5ad9610a09fb959e032db69ea4ee90ee426`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e418c8c213d1a739d87cd095e323f33ebf4c3e44019e494ec827522382d61b`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60be0006e7e454f9e2067f9d65dc10f14e4aa5f616b507f449b581e4b4c9652`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 6.4 MB (6445395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32c03c01ca3a4867d0577e501aad0614031b44b8cd9dc5fc785ac8304a22c2`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6099902d32d769bcecf7dc2e7693a87c09c8b34d91f089ef64cc0ce8184161`  
		Last Modified: Tue, 23 Sep 2025 21:31:26 GMT  
		Size: 46.7 MB (46672610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a6458371b085ae6cc30b374a57aa3fd57210c9870b15f632976ab25649325`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07d2d743d5b723e02b06d571cda40f1e51ef74d1282021f3399e6c3ead77ad`  
		Last Modified: Tue, 23 Sep 2025 22:15:03 GMT  
		Size: 130.4 MB (130356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad65e9d77b8d690fc78dbc74292789a3975502212153a6fd7d9c809068c0a5d`  
		Last Modified: Tue, 23 Sep 2025 21:31:23 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:75da0f31cdabaf33399903da298ec2e61aacee813fa6a2a205dff2b4b3d8c1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b7e888d4f2573a9e97af1582908e4b572a0ae4e873a27b79f3bfca3075cf9`

```dockerfile
```

-	Layers:
	-	`sha256:a6adea65e9008c9401ecf01b6aaa7a3a8d18033cd498d7196db41d5cc12f2e8e`  
		Last Modified: Wed, 24 Sep 2025 00:03:00 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cd19a20ffbb30918a27daf1c7a060db03ac358c7eec4eccea032a915d65d0d`  
		Last Modified: Wed, 24 Sep 2025 00:03:01 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:91447968e66961302339ec4dc4d385f5e1a957d98e63c7d52ecf8b1de0907346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a0d541011ee1758f9b568b0d7bb0920b0c0138ace1fb4fac2af852397fa264ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275367999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bdb7e77f7f793d767affc4bf4651e3b4a73b6ac28b17fa14f0e01eefc3ac47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c71b4bef6542def6c82567e8b9464aadbe0e5ec8eb318dc440d2882259f34`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9dafee77b549014e01bf4ac60f29fdaa2bf39c66e239598474804bf0e1d6`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9301ae294fee10b94d28be97e27c5cf2ab0e3c2671e5f66e2f41c79fe3ab911`  
		Last Modified: Tue, 23 Sep 2025 23:20:00 GMT  
		Size: 6.8 MB (6820256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620875f220d5e81ec99e0c02cf7d1c066ff9a5bbc976a36ad8d1ca8106e8c27`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457b1401253c19509121419424807eaf132e395834504c1173e747ec2cd17e2`  
		Last Modified: Tue, 23 Sep 2025 23:19:59 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8e7ce47d4070e01abfede0bf1c2e11edeaaba65fc54a678c408e448463aaac`  
		Last Modified: Tue, 23 Sep 2025 23:20:03 GMT  
		Size: 49.3 MB (49286557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522a8b4b86fe11f678d8ffcd97bac47e3df1893ab5bbdf7d5692e0d03acfb07`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ddb8dbdb41cd106c3e47ff9d987670afc04c221bc794e34aab26bb50402ab`  
		Last Modified: Wed, 24 Sep 2025 00:01:36 GMT  
		Size: 169.0 MB (168971139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619a14803e8266bf12b8ad8554c1e9685420b6b72403ed5b2a59b9eeb26c1581`  
		Last Modified: Tue, 23 Sep 2025 23:19:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:98c58afcc90eacdccd0e80ff087396f8857c665c123ac5c75cca68c1479225df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1cd2fec448086e987cf8590f0e22c898bc729171a0b6d1791f92a2bbdaebf`

```dockerfile
```

-	Layers:
	-	`sha256:e75895ba9d0f31d72a844609b41f39c283729d8f5b017dfd650424fbb092ccb0`  
		Last Modified: Wed, 24 Sep 2025 00:03:23 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45555cb8659dc1de9424b4ef325733733e69366689a2190dd5b682c20c07a7`  
		Last Modified: Wed, 24 Sep 2025 00:03:24 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7bd9e7258ef1ffaf9c1a9817fe76f6b5949ec21550f030d463b476bab56c2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270563073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec22e21be27435c6991930424ae28428cd09c82d7928e2c4e5810de8849ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beec75ea9523131575d2d8d76466c00b67506f064d31e723df56b608d1dbe0`  
		Last Modified: Tue, 23 Sep 2025 22:19:17 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f24e83af6dc9378bdbe4eb1d35e026bd15543a6384b789496a435187fd99e`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e973ad942c23c4c9805148016bffc0fd9b25381654f88ac37c4b81d299ba06`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 6.4 MB (6445336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbd3f4ed8c70a921eba2b06229071ca7782917995a90cc9df37a22743647d4`  
		Last Modified: Tue, 23 Sep 2025 21:31:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd21296720fa1fac7e42ea0dcaea55053952d26a39f7f8aebe1439dcbd253bc`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda0e12a0b66ff487863eebd14754d63df9d7c935f3e8ffcd1ab3a906fa6744`  
		Last Modified: Tue, 23 Sep 2025 22:19:34 GMT  
		Size: 48.0 MB (48019878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a31c1f092cf53edce59010ae59b74289ae2cde853473882906fb71d8f3d50d`  
		Last Modified: Tue, 23 Sep 2025 22:19:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716452459d78473c39f52d956a45ce2f89cb6d96caa7c084c954370724be4485`  
		Last Modified: Tue, 23 Sep 2025 22:19:49 GMT  
		Size: 167.3 MB (167262545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25a9a46a8f728e0a336c6f34bb0121df84598ee6a4973bff78756a0effccb8`  
		Last Modified: Tue, 23 Sep 2025 22:19:19 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:65a66c9d1047a361115a96fc01c08f003ad0e5095f2ee420a63be8a3df9ff19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c35067666bd311c0f596650066a9bdccd3f97edda4b34156c60f67559a7b45`

```dockerfile
```

-	Layers:
	-	`sha256:a88d43015128436c140fc0623a066fdd22d2395589717315c2b9ade3c074a6c6`  
		Last Modified: Wed, 24 Sep 2025 00:03:39 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f5c265a0fd6179f5d239be1d4639ff910e36181020a1e7314de6d939aced05`  
		Last Modified: Wed, 24 Sep 2025 00:03:40 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
