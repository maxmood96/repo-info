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
