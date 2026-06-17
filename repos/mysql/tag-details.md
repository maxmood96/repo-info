<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux9`](#mysql8-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.10`](#mysql8410)
-	[`mysql:8.4.10-oracle`](#mysql8410-oracle)
-	[`mysql:8.4.10-oraclelinux9`](#mysql8410-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.7`](#mysql97)
-	[`mysql:9.7-oracle`](#mysql97-oracle)
-	[`mysql:9.7-oraclelinux9`](#mysql97-oraclelinux9)
-	[`mysql:9.7.1`](#mysql971)
-	[`mysql:9.7.1-oracle`](#mysql971-oracle)
-	[`mysql:9.7.1-oraclelinux9`](#mysql971-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:8`

```console
$ docker pull mysql@sha256:563602a18ffd5be220968e8508d84c9dcd80fbffe69e28af51572db29e3285b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:94d1a3602540127d4979699ff8f6b6ae3d276a95305b3822c17abf3258995575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddce01ed435e81eb1b75674a3f4159f306c21346f1318895ba9f4a0f6b809af7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc907e0cfd46eb20ea747da4d9a86f0e8f96a953c14e3182774f625f93354dd`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12180891808e5e8256c07a556f076759cf37f255a8ae0cfdb6a61738a8f5c25d`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 783.6 KB (783564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4241c623e8f1e37f7b056644394947302b67b17618197d8be25bf4d93fa7c65`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 6.2 MB (6170658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db21c8e01a142d95c4a7584c672e2a0f8dabdd89ceb31df2a2c3028d6325317a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e36e20f9d536b5f96f6df935a882190ee1d09942923e3cd9dba79be88dbf5f`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95fdeb9c2aa23da45c3dfd3401c8b505ac84c5f0876f21a7902d45100e4acea`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 51.6 MB (51589512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa46846430985f241db4d18e3830ba388ac7c5267b5bd86ce11af900e7b54a`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8c406363298e5df397af8165786c44aab78e964ec31876849c4191a7609bd`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 132.4 MB (132405230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787990c783ee403069657aea217bfb7bf4f46548bcb5cba2c1993bd92aebc1a`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:dbc5978b2b10918ee75ca6a5752fb5a96230485de0ed31411200f33f20e554d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b55f62e960e1f97c7da3864167a46e37c84977c35c42462ef9c2d7794f2c68`

```dockerfile
```

-	Layers:
	-	`sha256:08b2091fe7bb7b63fd0b815570ed90a3befcaa7dfd32ab853bcacba5105caa8f`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 15.7 MB (15710018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b725d551ffbfb1d4329077220e4670cab57fb51b0d0116e4dbbba981543b306a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b6838bca58d96cdcfb36999bb90c3558a684ef2302430dad1694070cc984312c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233032958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fc05616f8ea53e509c0a3831c4a6ec1e624ae24a2aa93d8d8f08f8c5ff848e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd556d890493166361f818f8fa4eb84d5e2ef98788953bc4370286e029637c6`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dfd8bd20a7c949c819b2cb9e5bcd91ecbc3eddd269b7db9e3e7abfce6576f`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830aab8d1de40547b6a5e705b20c2636b2787454a884683eae65bc4e186a8811`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 5.8 MB (5792156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0dab97404c19b331e945f00b6ef8acd36596f21c7d89c742b5343131172e71`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54be1b41b223fe1593c6211b39ff4bd467cc574b317284456196c366b1ed11`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451acb96e10ed59d4dfecf37f20992ff87ef06ff549fcc39ae02fec5fd468d2d`  
		Last Modified: Tue, 16 Jun 2026 23:47:01 GMT  
		Size: 49.8 MB (49826313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c4efac8f2d02a5bc435374491d4b5b4ed847b87809fdb34b1ef56dd1d2026`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ce6adf874692a6a9c8d3359d8f3fe0d1d9ac20f1c4fa54f677ea7669f8825`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 130.8 MB (130768498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5c816d9b8d58339a3b5d674c37cd9df4e9a96093bb02c34ea76b014a993c2`  
		Last Modified: Tue, 16 Jun 2026 23:47:00 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:848253f86b47452052a4295916b461eae71d988ca20c0c7e74c1b63e444f8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f8d999c7f9ae4ef26b26e71280b5e009b7140a8e2034ad214c75c42b38646`

```dockerfile
```

-	Layers:
	-	`sha256:c02e4ef7e85cfb3451d007dc047fc29136d3003ed9ce0be9e8230fbccc73ea33`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 15.7 MB (15708402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8d3f2c4c66c8690705483f9eac7b4d25fbad2cb2ba5589abd173e1d35b80cf`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:563602a18ffd5be220968e8508d84c9dcd80fbffe69e28af51572db29e3285b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:94d1a3602540127d4979699ff8f6b6ae3d276a95305b3822c17abf3258995575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddce01ed435e81eb1b75674a3f4159f306c21346f1318895ba9f4a0f6b809af7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc907e0cfd46eb20ea747da4d9a86f0e8f96a953c14e3182774f625f93354dd`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12180891808e5e8256c07a556f076759cf37f255a8ae0cfdb6a61738a8f5c25d`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 783.6 KB (783564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4241c623e8f1e37f7b056644394947302b67b17618197d8be25bf4d93fa7c65`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 6.2 MB (6170658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db21c8e01a142d95c4a7584c672e2a0f8dabdd89ceb31df2a2c3028d6325317a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e36e20f9d536b5f96f6df935a882190ee1d09942923e3cd9dba79be88dbf5f`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95fdeb9c2aa23da45c3dfd3401c8b505ac84c5f0876f21a7902d45100e4acea`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 51.6 MB (51589512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa46846430985f241db4d18e3830ba388ac7c5267b5bd86ce11af900e7b54a`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8c406363298e5df397af8165786c44aab78e964ec31876849c4191a7609bd`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 132.4 MB (132405230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787990c783ee403069657aea217bfb7bf4f46548bcb5cba2c1993bd92aebc1a`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:dbc5978b2b10918ee75ca6a5752fb5a96230485de0ed31411200f33f20e554d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b55f62e960e1f97c7da3864167a46e37c84977c35c42462ef9c2d7794f2c68`

```dockerfile
```

-	Layers:
	-	`sha256:08b2091fe7bb7b63fd0b815570ed90a3befcaa7dfd32ab853bcacba5105caa8f`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 15.7 MB (15710018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b725d551ffbfb1d4329077220e4670cab57fb51b0d0116e4dbbba981543b306a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b6838bca58d96cdcfb36999bb90c3558a684ef2302430dad1694070cc984312c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233032958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fc05616f8ea53e509c0a3831c4a6ec1e624ae24a2aa93d8d8f08f8c5ff848e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd556d890493166361f818f8fa4eb84d5e2ef98788953bc4370286e029637c6`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dfd8bd20a7c949c819b2cb9e5bcd91ecbc3eddd269b7db9e3e7abfce6576f`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830aab8d1de40547b6a5e705b20c2636b2787454a884683eae65bc4e186a8811`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 5.8 MB (5792156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0dab97404c19b331e945f00b6ef8acd36596f21c7d89c742b5343131172e71`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54be1b41b223fe1593c6211b39ff4bd467cc574b317284456196c366b1ed11`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451acb96e10ed59d4dfecf37f20992ff87ef06ff549fcc39ae02fec5fd468d2d`  
		Last Modified: Tue, 16 Jun 2026 23:47:01 GMT  
		Size: 49.8 MB (49826313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c4efac8f2d02a5bc435374491d4b5b4ed847b87809fdb34b1ef56dd1d2026`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ce6adf874692a6a9c8d3359d8f3fe0d1d9ac20f1c4fa54f677ea7669f8825`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 130.8 MB (130768498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5c816d9b8d58339a3b5d674c37cd9df4e9a96093bb02c34ea76b014a993c2`  
		Last Modified: Tue, 16 Jun 2026 23:47:00 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:848253f86b47452052a4295916b461eae71d988ca20c0c7e74c1b63e444f8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f8d999c7f9ae4ef26b26e71280b5e009b7140a8e2034ad214c75c42b38646`

```dockerfile
```

-	Layers:
	-	`sha256:c02e4ef7e85cfb3451d007dc047fc29136d3003ed9ce0be9e8230fbccc73ea33`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 15.7 MB (15708402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8d3f2c4c66c8690705483f9eac7b4d25fbad2cb2ba5589abd173e1d35b80cf`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:563602a18ffd5be220968e8508d84c9dcd80fbffe69e28af51572db29e3285b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:94d1a3602540127d4979699ff8f6b6ae3d276a95305b3822c17abf3258995575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddce01ed435e81eb1b75674a3f4159f306c21346f1318895ba9f4a0f6b809af7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc907e0cfd46eb20ea747da4d9a86f0e8f96a953c14e3182774f625f93354dd`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12180891808e5e8256c07a556f076759cf37f255a8ae0cfdb6a61738a8f5c25d`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 783.6 KB (783564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4241c623e8f1e37f7b056644394947302b67b17618197d8be25bf4d93fa7c65`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 6.2 MB (6170658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db21c8e01a142d95c4a7584c672e2a0f8dabdd89ceb31df2a2c3028d6325317a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e36e20f9d536b5f96f6df935a882190ee1d09942923e3cd9dba79be88dbf5f`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95fdeb9c2aa23da45c3dfd3401c8b505ac84c5f0876f21a7902d45100e4acea`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 51.6 MB (51589512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa46846430985f241db4d18e3830ba388ac7c5267b5bd86ce11af900e7b54a`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8c406363298e5df397af8165786c44aab78e964ec31876849c4191a7609bd`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 132.4 MB (132405230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787990c783ee403069657aea217bfb7bf4f46548bcb5cba2c1993bd92aebc1a`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:dbc5978b2b10918ee75ca6a5752fb5a96230485de0ed31411200f33f20e554d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b55f62e960e1f97c7da3864167a46e37c84977c35c42462ef9c2d7794f2c68`

```dockerfile
```

-	Layers:
	-	`sha256:08b2091fe7bb7b63fd0b815570ed90a3befcaa7dfd32ab853bcacba5105caa8f`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 15.7 MB (15710018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b725d551ffbfb1d4329077220e4670cab57fb51b0d0116e4dbbba981543b306a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b6838bca58d96cdcfb36999bb90c3558a684ef2302430dad1694070cc984312c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233032958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fc05616f8ea53e509c0a3831c4a6ec1e624ae24a2aa93d8d8f08f8c5ff848e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd556d890493166361f818f8fa4eb84d5e2ef98788953bc4370286e029637c6`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dfd8bd20a7c949c819b2cb9e5bcd91ecbc3eddd269b7db9e3e7abfce6576f`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830aab8d1de40547b6a5e705b20c2636b2787454a884683eae65bc4e186a8811`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 5.8 MB (5792156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0dab97404c19b331e945f00b6ef8acd36596f21c7d89c742b5343131172e71`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54be1b41b223fe1593c6211b39ff4bd467cc574b317284456196c366b1ed11`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451acb96e10ed59d4dfecf37f20992ff87ef06ff549fcc39ae02fec5fd468d2d`  
		Last Modified: Tue, 16 Jun 2026 23:47:01 GMT  
		Size: 49.8 MB (49826313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c4efac8f2d02a5bc435374491d4b5b4ed847b87809fdb34b1ef56dd1d2026`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ce6adf874692a6a9c8d3359d8f3fe0d1d9ac20f1c4fa54f677ea7669f8825`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 130.8 MB (130768498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5c816d9b8d58339a3b5d674c37cd9df4e9a96093bb02c34ea76b014a993c2`  
		Last Modified: Tue, 16 Jun 2026 23:47:00 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:848253f86b47452052a4295916b461eae71d988ca20c0c7e74c1b63e444f8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f8d999c7f9ae4ef26b26e71280b5e009b7140a8e2034ad214c75c42b38646`

```dockerfile
```

-	Layers:
	-	`sha256:c02e4ef7e85cfb3451d007dc047fc29136d3003ed9ce0be9e8230fbccc73ea33`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 15.7 MB (15708402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8d3f2c4c66c8690705483f9eac7b4d25fbad2cb2ba5589abd173e1d35b80cf`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:563602a18ffd5be220968e8508d84c9dcd80fbffe69e28af51572db29e3285b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:94d1a3602540127d4979699ff8f6b6ae3d276a95305b3822c17abf3258995575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddce01ed435e81eb1b75674a3f4159f306c21346f1318895ba9f4a0f6b809af7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc907e0cfd46eb20ea747da4d9a86f0e8f96a953c14e3182774f625f93354dd`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12180891808e5e8256c07a556f076759cf37f255a8ae0cfdb6a61738a8f5c25d`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 783.6 KB (783564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4241c623e8f1e37f7b056644394947302b67b17618197d8be25bf4d93fa7c65`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 6.2 MB (6170658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db21c8e01a142d95c4a7584c672e2a0f8dabdd89ceb31df2a2c3028d6325317a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e36e20f9d536b5f96f6df935a882190ee1d09942923e3cd9dba79be88dbf5f`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95fdeb9c2aa23da45c3dfd3401c8b505ac84c5f0876f21a7902d45100e4acea`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 51.6 MB (51589512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa46846430985f241db4d18e3830ba388ac7c5267b5bd86ce11af900e7b54a`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8c406363298e5df397af8165786c44aab78e964ec31876849c4191a7609bd`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 132.4 MB (132405230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787990c783ee403069657aea217bfb7bf4f46548bcb5cba2c1993bd92aebc1a`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:dbc5978b2b10918ee75ca6a5752fb5a96230485de0ed31411200f33f20e554d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b55f62e960e1f97c7da3864167a46e37c84977c35c42462ef9c2d7794f2c68`

```dockerfile
```

-	Layers:
	-	`sha256:08b2091fe7bb7b63fd0b815570ed90a3befcaa7dfd32ab853bcacba5105caa8f`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 15.7 MB (15710018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b725d551ffbfb1d4329077220e4670cab57fb51b0d0116e4dbbba981543b306a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b6838bca58d96cdcfb36999bb90c3558a684ef2302430dad1694070cc984312c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233032958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fc05616f8ea53e509c0a3831c4a6ec1e624ae24a2aa93d8d8f08f8c5ff848e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd556d890493166361f818f8fa4eb84d5e2ef98788953bc4370286e029637c6`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dfd8bd20a7c949c819b2cb9e5bcd91ecbc3eddd269b7db9e3e7abfce6576f`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830aab8d1de40547b6a5e705b20c2636b2787454a884683eae65bc4e186a8811`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 5.8 MB (5792156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0dab97404c19b331e945f00b6ef8acd36596f21c7d89c742b5343131172e71`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54be1b41b223fe1593c6211b39ff4bd467cc574b317284456196c366b1ed11`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451acb96e10ed59d4dfecf37f20992ff87ef06ff549fcc39ae02fec5fd468d2d`  
		Last Modified: Tue, 16 Jun 2026 23:47:01 GMT  
		Size: 49.8 MB (49826313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c4efac8f2d02a5bc435374491d4b5b4ed847b87809fdb34b1ef56dd1d2026`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ce6adf874692a6a9c8d3359d8f3fe0d1d9ac20f1c4fa54f677ea7669f8825`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 130.8 MB (130768498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5c816d9b8d58339a3b5d674c37cd9df4e9a96093bb02c34ea76b014a993c2`  
		Last Modified: Tue, 16 Jun 2026 23:47:00 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:848253f86b47452052a4295916b461eae71d988ca20c0c7e74c1b63e444f8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f8d999c7f9ae4ef26b26e71280b5e009b7140a8e2034ad214c75c42b38646`

```dockerfile
```

-	Layers:
	-	`sha256:c02e4ef7e85cfb3451d007dc047fc29136d3003ed9ce0be9e8230fbccc73ea33`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 15.7 MB (15708402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8d3f2c4c66c8690705483f9eac7b4d25fbad2cb2ba5589abd173e1d35b80cf`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:563602a18ffd5be220968e8508d84c9dcd80fbffe69e28af51572db29e3285b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:94d1a3602540127d4979699ff8f6b6ae3d276a95305b3822c17abf3258995575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddce01ed435e81eb1b75674a3f4159f306c21346f1318895ba9f4a0f6b809af7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc907e0cfd46eb20ea747da4d9a86f0e8f96a953c14e3182774f625f93354dd`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12180891808e5e8256c07a556f076759cf37f255a8ae0cfdb6a61738a8f5c25d`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 783.6 KB (783564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4241c623e8f1e37f7b056644394947302b67b17618197d8be25bf4d93fa7c65`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 6.2 MB (6170658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db21c8e01a142d95c4a7584c672e2a0f8dabdd89ceb31df2a2c3028d6325317a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e36e20f9d536b5f96f6df935a882190ee1d09942923e3cd9dba79be88dbf5f`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95fdeb9c2aa23da45c3dfd3401c8b505ac84c5f0876f21a7902d45100e4acea`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 51.6 MB (51589512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa46846430985f241db4d18e3830ba388ac7c5267b5bd86ce11af900e7b54a`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8c406363298e5df397af8165786c44aab78e964ec31876849c4191a7609bd`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 132.4 MB (132405230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787990c783ee403069657aea217bfb7bf4f46548bcb5cba2c1993bd92aebc1a`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:dbc5978b2b10918ee75ca6a5752fb5a96230485de0ed31411200f33f20e554d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b55f62e960e1f97c7da3864167a46e37c84977c35c42462ef9c2d7794f2c68`

```dockerfile
```

-	Layers:
	-	`sha256:08b2091fe7bb7b63fd0b815570ed90a3befcaa7dfd32ab853bcacba5105caa8f`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 15.7 MB (15710018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b725d551ffbfb1d4329077220e4670cab57fb51b0d0116e4dbbba981543b306a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b6838bca58d96cdcfb36999bb90c3558a684ef2302430dad1694070cc984312c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233032958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fc05616f8ea53e509c0a3831c4a6ec1e624ae24a2aa93d8d8f08f8c5ff848e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd556d890493166361f818f8fa4eb84d5e2ef98788953bc4370286e029637c6`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dfd8bd20a7c949c819b2cb9e5bcd91ecbc3eddd269b7db9e3e7abfce6576f`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830aab8d1de40547b6a5e705b20c2636b2787454a884683eae65bc4e186a8811`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 5.8 MB (5792156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0dab97404c19b331e945f00b6ef8acd36596f21c7d89c742b5343131172e71`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54be1b41b223fe1593c6211b39ff4bd467cc574b317284456196c366b1ed11`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451acb96e10ed59d4dfecf37f20992ff87ef06ff549fcc39ae02fec5fd468d2d`  
		Last Modified: Tue, 16 Jun 2026 23:47:01 GMT  
		Size: 49.8 MB (49826313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c4efac8f2d02a5bc435374491d4b5b4ed847b87809fdb34b1ef56dd1d2026`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ce6adf874692a6a9c8d3359d8f3fe0d1d9ac20f1c4fa54f677ea7669f8825`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 130.8 MB (130768498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5c816d9b8d58339a3b5d674c37cd9df4e9a96093bb02c34ea76b014a993c2`  
		Last Modified: Tue, 16 Jun 2026 23:47:00 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:848253f86b47452052a4295916b461eae71d988ca20c0c7e74c1b63e444f8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f8d999c7f9ae4ef26b26e71280b5e009b7140a8e2034ad214c75c42b38646`

```dockerfile
```

-	Layers:
	-	`sha256:c02e4ef7e85cfb3451d007dc047fc29136d3003ed9ce0be9e8230fbccc73ea33`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 15.7 MB (15708402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8d3f2c4c66c8690705483f9eac7b4d25fbad2cb2ba5589abd173e1d35b80cf`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:563602a18ffd5be220968e8508d84c9dcd80fbffe69e28af51572db29e3285b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:94d1a3602540127d4979699ff8f6b6ae3d276a95305b3822c17abf3258995575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddce01ed435e81eb1b75674a3f4159f306c21346f1318895ba9f4a0f6b809af7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc907e0cfd46eb20ea747da4d9a86f0e8f96a953c14e3182774f625f93354dd`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12180891808e5e8256c07a556f076759cf37f255a8ae0cfdb6a61738a8f5c25d`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 783.6 KB (783564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4241c623e8f1e37f7b056644394947302b67b17618197d8be25bf4d93fa7c65`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 6.2 MB (6170658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db21c8e01a142d95c4a7584c672e2a0f8dabdd89ceb31df2a2c3028d6325317a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e36e20f9d536b5f96f6df935a882190ee1d09942923e3cd9dba79be88dbf5f`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95fdeb9c2aa23da45c3dfd3401c8b505ac84c5f0876f21a7902d45100e4acea`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 51.6 MB (51589512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa46846430985f241db4d18e3830ba388ac7c5267b5bd86ce11af900e7b54a`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8c406363298e5df397af8165786c44aab78e964ec31876849c4191a7609bd`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 132.4 MB (132405230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787990c783ee403069657aea217bfb7bf4f46548bcb5cba2c1993bd92aebc1a`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:dbc5978b2b10918ee75ca6a5752fb5a96230485de0ed31411200f33f20e554d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b55f62e960e1f97c7da3864167a46e37c84977c35c42462ef9c2d7794f2c68`

```dockerfile
```

-	Layers:
	-	`sha256:08b2091fe7bb7b63fd0b815570ed90a3befcaa7dfd32ab853bcacba5105caa8f`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 15.7 MB (15710018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b725d551ffbfb1d4329077220e4670cab57fb51b0d0116e4dbbba981543b306a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b6838bca58d96cdcfb36999bb90c3558a684ef2302430dad1694070cc984312c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233032958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fc05616f8ea53e509c0a3831c4a6ec1e624ae24a2aa93d8d8f08f8c5ff848e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd556d890493166361f818f8fa4eb84d5e2ef98788953bc4370286e029637c6`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dfd8bd20a7c949c819b2cb9e5bcd91ecbc3eddd269b7db9e3e7abfce6576f`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830aab8d1de40547b6a5e705b20c2636b2787454a884683eae65bc4e186a8811`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 5.8 MB (5792156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0dab97404c19b331e945f00b6ef8acd36596f21c7d89c742b5343131172e71`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54be1b41b223fe1593c6211b39ff4bd467cc574b317284456196c366b1ed11`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451acb96e10ed59d4dfecf37f20992ff87ef06ff549fcc39ae02fec5fd468d2d`  
		Last Modified: Tue, 16 Jun 2026 23:47:01 GMT  
		Size: 49.8 MB (49826313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c4efac8f2d02a5bc435374491d4b5b4ed847b87809fdb34b1ef56dd1d2026`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ce6adf874692a6a9c8d3359d8f3fe0d1d9ac20f1c4fa54f677ea7669f8825`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 130.8 MB (130768498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5c816d9b8d58339a3b5d674c37cd9df4e9a96093bb02c34ea76b014a993c2`  
		Last Modified: Tue, 16 Jun 2026 23:47:00 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:848253f86b47452052a4295916b461eae71d988ca20c0c7e74c1b63e444f8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f8d999c7f9ae4ef26b26e71280b5e009b7140a8e2034ad214c75c42b38646`

```dockerfile
```

-	Layers:
	-	`sha256:c02e4ef7e85cfb3451d007dc047fc29136d3003ed9ce0be9e8230fbccc73ea33`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 15.7 MB (15708402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8d3f2c4c66c8690705483f9eac7b4d25fbad2cb2ba5589abd173e1d35b80cf`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.10`

```console
$ docker pull mysql@sha256:563602a18ffd5be220968e8508d84c9dcd80fbffe69e28af51572db29e3285b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.10` - linux; amd64

```console
$ docker pull mysql@sha256:94d1a3602540127d4979699ff8f6b6ae3d276a95305b3822c17abf3258995575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddce01ed435e81eb1b75674a3f4159f306c21346f1318895ba9f4a0f6b809af7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc907e0cfd46eb20ea747da4d9a86f0e8f96a953c14e3182774f625f93354dd`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12180891808e5e8256c07a556f076759cf37f255a8ae0cfdb6a61738a8f5c25d`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 783.6 KB (783564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4241c623e8f1e37f7b056644394947302b67b17618197d8be25bf4d93fa7c65`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 6.2 MB (6170658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db21c8e01a142d95c4a7584c672e2a0f8dabdd89ceb31df2a2c3028d6325317a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e36e20f9d536b5f96f6df935a882190ee1d09942923e3cd9dba79be88dbf5f`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95fdeb9c2aa23da45c3dfd3401c8b505ac84c5f0876f21a7902d45100e4acea`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 51.6 MB (51589512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa46846430985f241db4d18e3830ba388ac7c5267b5bd86ce11af900e7b54a`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8c406363298e5df397af8165786c44aab78e964ec31876849c4191a7609bd`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 132.4 MB (132405230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787990c783ee403069657aea217bfb7bf4f46548bcb5cba2c1993bd92aebc1a`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.10` - unknown; unknown

```console
$ docker pull mysql@sha256:dbc5978b2b10918ee75ca6a5752fb5a96230485de0ed31411200f33f20e554d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b55f62e960e1f97c7da3864167a46e37c84977c35c42462ef9c2d7794f2c68`

```dockerfile
```

-	Layers:
	-	`sha256:08b2091fe7bb7b63fd0b815570ed90a3befcaa7dfd32ab853bcacba5105caa8f`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 15.7 MB (15710018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b725d551ffbfb1d4329077220e4670cab57fb51b0d0116e4dbbba981543b306a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.10` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b6838bca58d96cdcfb36999bb90c3558a684ef2302430dad1694070cc984312c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233032958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fc05616f8ea53e509c0a3831c4a6ec1e624ae24a2aa93d8d8f08f8c5ff848e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd556d890493166361f818f8fa4eb84d5e2ef98788953bc4370286e029637c6`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dfd8bd20a7c949c819b2cb9e5bcd91ecbc3eddd269b7db9e3e7abfce6576f`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830aab8d1de40547b6a5e705b20c2636b2787454a884683eae65bc4e186a8811`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 5.8 MB (5792156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0dab97404c19b331e945f00b6ef8acd36596f21c7d89c742b5343131172e71`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54be1b41b223fe1593c6211b39ff4bd467cc574b317284456196c366b1ed11`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451acb96e10ed59d4dfecf37f20992ff87ef06ff549fcc39ae02fec5fd468d2d`  
		Last Modified: Tue, 16 Jun 2026 23:47:01 GMT  
		Size: 49.8 MB (49826313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c4efac8f2d02a5bc435374491d4b5b4ed847b87809fdb34b1ef56dd1d2026`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ce6adf874692a6a9c8d3359d8f3fe0d1d9ac20f1c4fa54f677ea7669f8825`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 130.8 MB (130768498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5c816d9b8d58339a3b5d674c37cd9df4e9a96093bb02c34ea76b014a993c2`  
		Last Modified: Tue, 16 Jun 2026 23:47:00 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.10` - unknown; unknown

```console
$ docker pull mysql@sha256:848253f86b47452052a4295916b461eae71d988ca20c0c7e74c1b63e444f8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f8d999c7f9ae4ef26b26e71280b5e009b7140a8e2034ad214c75c42b38646`

```dockerfile
```

-	Layers:
	-	`sha256:c02e4ef7e85cfb3451d007dc047fc29136d3003ed9ce0be9e8230fbccc73ea33`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 15.7 MB (15708402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8d3f2c4c66c8690705483f9eac7b4d25fbad2cb2ba5589abd173e1d35b80cf`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.10-oracle`

```console
$ docker pull mysql@sha256:563602a18ffd5be220968e8508d84c9dcd80fbffe69e28af51572db29e3285b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.10-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:94d1a3602540127d4979699ff8f6b6ae3d276a95305b3822c17abf3258995575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddce01ed435e81eb1b75674a3f4159f306c21346f1318895ba9f4a0f6b809af7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc907e0cfd46eb20ea747da4d9a86f0e8f96a953c14e3182774f625f93354dd`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12180891808e5e8256c07a556f076759cf37f255a8ae0cfdb6a61738a8f5c25d`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 783.6 KB (783564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4241c623e8f1e37f7b056644394947302b67b17618197d8be25bf4d93fa7c65`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 6.2 MB (6170658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db21c8e01a142d95c4a7584c672e2a0f8dabdd89ceb31df2a2c3028d6325317a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e36e20f9d536b5f96f6df935a882190ee1d09942923e3cd9dba79be88dbf5f`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95fdeb9c2aa23da45c3dfd3401c8b505ac84c5f0876f21a7902d45100e4acea`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 51.6 MB (51589512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa46846430985f241db4d18e3830ba388ac7c5267b5bd86ce11af900e7b54a`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8c406363298e5df397af8165786c44aab78e964ec31876849c4191a7609bd`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 132.4 MB (132405230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787990c783ee403069657aea217bfb7bf4f46548bcb5cba2c1993bd92aebc1a`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.10-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:dbc5978b2b10918ee75ca6a5752fb5a96230485de0ed31411200f33f20e554d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b55f62e960e1f97c7da3864167a46e37c84977c35c42462ef9c2d7794f2c68`

```dockerfile
```

-	Layers:
	-	`sha256:08b2091fe7bb7b63fd0b815570ed90a3befcaa7dfd32ab853bcacba5105caa8f`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 15.7 MB (15710018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b725d551ffbfb1d4329077220e4670cab57fb51b0d0116e4dbbba981543b306a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.10-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b6838bca58d96cdcfb36999bb90c3558a684ef2302430dad1694070cc984312c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233032958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fc05616f8ea53e509c0a3831c4a6ec1e624ae24a2aa93d8d8f08f8c5ff848e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd556d890493166361f818f8fa4eb84d5e2ef98788953bc4370286e029637c6`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dfd8bd20a7c949c819b2cb9e5bcd91ecbc3eddd269b7db9e3e7abfce6576f`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830aab8d1de40547b6a5e705b20c2636b2787454a884683eae65bc4e186a8811`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 5.8 MB (5792156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0dab97404c19b331e945f00b6ef8acd36596f21c7d89c742b5343131172e71`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54be1b41b223fe1593c6211b39ff4bd467cc574b317284456196c366b1ed11`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451acb96e10ed59d4dfecf37f20992ff87ef06ff549fcc39ae02fec5fd468d2d`  
		Last Modified: Tue, 16 Jun 2026 23:47:01 GMT  
		Size: 49.8 MB (49826313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c4efac8f2d02a5bc435374491d4b5b4ed847b87809fdb34b1ef56dd1d2026`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ce6adf874692a6a9c8d3359d8f3fe0d1d9ac20f1c4fa54f677ea7669f8825`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 130.8 MB (130768498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5c816d9b8d58339a3b5d674c37cd9df4e9a96093bb02c34ea76b014a993c2`  
		Last Modified: Tue, 16 Jun 2026 23:47:00 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.10-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:848253f86b47452052a4295916b461eae71d988ca20c0c7e74c1b63e444f8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f8d999c7f9ae4ef26b26e71280b5e009b7140a8e2034ad214c75c42b38646`

```dockerfile
```

-	Layers:
	-	`sha256:c02e4ef7e85cfb3451d007dc047fc29136d3003ed9ce0be9e8230fbccc73ea33`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 15.7 MB (15708402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8d3f2c4c66c8690705483f9eac7b4d25fbad2cb2ba5589abd173e1d35b80cf`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.10-oraclelinux9`

```console
$ docker pull mysql@sha256:563602a18ffd5be220968e8508d84c9dcd80fbffe69e28af51572db29e3285b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.10-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:94d1a3602540127d4979699ff8f6b6ae3d276a95305b3822c17abf3258995575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddce01ed435e81eb1b75674a3f4159f306c21346f1318895ba9f4a0f6b809af7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:16 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc907e0cfd46eb20ea747da4d9a86f0e8f96a953c14e3182774f625f93354dd`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12180891808e5e8256c07a556f076759cf37f255a8ae0cfdb6a61738a8f5c25d`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 783.6 KB (783564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4241c623e8f1e37f7b056644394947302b67b17618197d8be25bf4d93fa7c65`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 6.2 MB (6170658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db21c8e01a142d95c4a7584c672e2a0f8dabdd89ceb31df2a2c3028d6325317a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e36e20f9d536b5f96f6df935a882190ee1d09942923e3cd9dba79be88dbf5f`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95fdeb9c2aa23da45c3dfd3401c8b505ac84c5f0876f21a7902d45100e4acea`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 51.6 MB (51589512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa46846430985f241db4d18e3830ba388ac7c5267b5bd86ce11af900e7b54a`  
		Last Modified: Tue, 16 Jun 2026 23:46:54 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8c406363298e5df397af8165786c44aab78e964ec31876849c4191a7609bd`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 132.4 MB (132405230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787990c783ee403069657aea217bfb7bf4f46548bcb5cba2c1993bd92aebc1a`  
		Last Modified: Tue, 16 Jun 2026 23:46:55 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.10-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:dbc5978b2b10918ee75ca6a5752fb5a96230485de0ed31411200f33f20e554d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b55f62e960e1f97c7da3864167a46e37c84977c35c42462ef9c2d7794f2c68`

```dockerfile
```

-	Layers:
	-	`sha256:08b2091fe7bb7b63fd0b815570ed90a3befcaa7dfd32ab853bcacba5105caa8f`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 15.7 MB (15710018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b725d551ffbfb1d4329077220e4670cab57fb51b0d0116e4dbbba981543b306a`  
		Last Modified: Tue, 16 Jun 2026 23:46:53 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.10-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b6838bca58d96cdcfb36999bb90c3558a684ef2302430dad1694070cc984312c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233032958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fc05616f8ea53e509c0a3831c4a6ec1e624ae24a2aa93d8d8f08f8c5ff848e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 16 Jun 2026 23:45:11 GMT
ENV MYSQL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:45:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
ENV MYSQL_SHELL_VERSION=8.4.10-1.el9
# Tue, 16 Jun 2026 23:46:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd556d890493166361f818f8fa4eb84d5e2ef98788953bc4370286e029637c6`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dfd8bd20a7c949c819b2cb9e5bcd91ecbc3eddd269b7db9e3e7abfce6576f`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830aab8d1de40547b6a5e705b20c2636b2787454a884683eae65bc4e186a8811`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 5.8 MB (5792156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0dab97404c19b331e945f00b6ef8acd36596f21c7d89c742b5343131172e71`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54be1b41b223fe1593c6211b39ff4bd467cc574b317284456196c366b1ed11`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451acb96e10ed59d4dfecf37f20992ff87ef06ff549fcc39ae02fec5fd468d2d`  
		Last Modified: Tue, 16 Jun 2026 23:47:01 GMT  
		Size: 49.8 MB (49826313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c4efac8f2d02a5bc435374491d4b5b4ed847b87809fdb34b1ef56dd1d2026`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ce6adf874692a6a9c8d3359d8f3fe0d1d9ac20f1c4fa54f677ea7669f8825`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 130.8 MB (130768498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5c816d9b8d58339a3b5d674c37cd9df4e9a96093bb02c34ea76b014a993c2`  
		Last Modified: Tue, 16 Jun 2026 23:47:00 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.10-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:848253f86b47452052a4295916b461eae71d988ca20c0c7e74c1b63e444f8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f8d999c7f9ae4ef26b26e71280b5e009b7140a8e2034ad214c75c42b38646`

```dockerfile
```

-	Layers:
	-	`sha256:c02e4ef7e85cfb3451d007dc047fc29136d3003ed9ce0be9e8230fbccc73ea33`  
		Last Modified: Tue, 16 Jun 2026 23:46:59 GMT  
		Size: 15.7 MB (15708402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8d3f2c4c66c8690705483f9eac7b4d25fbad2cb2ba5589abd173e1d35b80cf`  
		Last Modified: Tue, 16 Jun 2026 23:46:58 GMT  
		Size: 33.6 KB (33582 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7-oracle`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7-oraclelinux9`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7.1`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.1` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.1` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.1` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7.1-oracle`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7.1-oraclelinux9`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.1-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7.1-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:e370cd5f64599d46985b7729b452f2153825246f88d82753ec595c5dfc6fef6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:08775e50f9fd40eeb98408e651dd779892fb44c15fea3cf13f9ae42e77dde97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270174254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b58dcd4de9b3cb8a9725cc802824f2e70e2c78de8017767643e6fe7e9a7bc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:17 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:17 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:47 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1b5ce44a5a7b749518148ddb5d5956aea0166fa379ec700755424bf6a8409`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9269a5b770b91f0603818458d371fe3fc3b504cbcd470bab2c1355996aa44`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 783.6 KB (783565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa254cf17fa915510278da6038744dbdf1dece4165477487f0d33a75a178ab6`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 6.2 MB (6170697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f87a59c152e17b6b90ad34586f2d4b9f8778bf5c3712775404b1a41b81d11`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3938a6b74fb4415afd02f5928c56940547fd56983cac578db805866e0c879a`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017322df62589d373dc6cd2f979750d1e3b192ff840779f83752e1b3ddfb28b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 57.0 MB (56976705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687e41f2f920a3d30d7da112f313dd3ac95dc031659a7173456bdd850790989`  
		Last Modified: Tue, 16 Jun 2026 23:47:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aae638e49064ceb6685229ba0fa8a84b6c1be28c8c6075f11f9288005068c8`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 158.9 MB (158924337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b43c748cbb8457877647ca0b0e2832f9087966acac830da794e7b81ea221c6`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1ede67bc74f8a575da3f926592086626a3b6f03f9873d678b0ab1f9c582c698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a60085d86bbf25d6b24aa397b1598aa0654e6c1f68a163112f5beb9920283d`

```dockerfile
```

-	Layers:
	-	`sha256:fabbed2360d0b57ef961f27f5733a6e39e9637bdbc01d0c964e3fb551752344d`  
		Last Modified: Tue, 16 Jun 2026 23:47:04 GMT  
		Size: 16.8 MB (16797392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e87462711bcb47d10c6e7bac03a86d527f27b50850c119d5e02409d75cfeb`  
		Last Modified: Tue, 16 Jun 2026 23:47:03 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0f641848a76aa16684ae8ffb5a8288845ab43c57087e7f1e5df952159867e204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266617386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35b38be979cb0b2278404f341860d6e20ff922609dd631176b31ce68aa009f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:44:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 16 Jun 2026 23:44:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:44:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:45:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 16 Jun 2026 23:45:10 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:45:10 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 16 Jun 2026 23:45:45 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 16 Jun 2026 23:45:46 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 16 Jun 2026 23:46:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 16 Jun 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:46:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:46:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 16 Jun 2026 23:46:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e25be2cad1b1f185e9af3462d41af92ac71c043744987025a775df0c1718f`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b4c49fd88e5fa16078a170b6321eb513e5c776d098fa94f5322488c2afc68`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fd96a935071d8ea38217a6065dd2beb308e232fd05c59937c6f2f713af6d2`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 5.8 MB (5792138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957707d11955dabb819f3c0635744179d7675d7e6ef9021006d13bc792b883e8`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b2963c03302646ce0e504be215796ee88e3b98520252de9c3b3f6baba604b`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf169078a81ee6975a2ee5c84a6c26d18f2616f0bc08805de61549106d1685`  
		Last Modified: Tue, 16 Jun 2026 23:47:09 GMT  
		Size: 57.0 MB (56985363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77a972f0a3bffb111546c9434947cf6d25eb909d56f7bea51f1ff4222c1df88`  
		Last Modified: Tue, 16 Jun 2026 23:47:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aea34ff95188ad490fd80a35ad59b618d0df4ff0472c66b1f6c96bd3cf407`  
		Last Modified: Tue, 16 Jun 2026 23:47:11 GMT  
		Size: 157.2 MB (157193902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f052bf658e3bed9bfbdd7e52ad659f9223438a5a739d1ac90b5446e3b1b958e`  
		Last Modified: Tue, 16 Jun 2026 23:47:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f076b233f75389af108341c00d0547660406aa0ee17520422bc910862acc89bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ce68c4205c26eded12a664e1f05f5eada1bd4492ad60268df3a1d769981130`

```dockerfile
```

-	Layers:
	-	`sha256:e12af0afb9eee6400cbb9de91df2e19e6f99b6a139c1c6d0ca02b18210199bba`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 16.8 MB (16795848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe272e4ef60057e4a8723415462a9fe2b525eaecc62931257ab8e94388d83384`  
		Last Modified: Tue, 16 Jun 2026 23:47:06 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json
