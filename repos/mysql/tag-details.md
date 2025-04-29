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
-	[`mysql:8.0.42`](#mysql8042)
-	[`mysql:8.0.42-bookworm`](#mysql8042-bookworm)
-	[`mysql:8.0.42-debian`](#mysql8042-debian)
-	[`mysql:8.0.42-oracle`](#mysql8042-oracle)
-	[`mysql:8.0.42-oraclelinux9`](#mysql8042-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.5`](#mysql845)
-	[`mysql:8.4.5-oracle`](#mysql845-oracle)
-	[`mysql:8.4.5-oraclelinux9`](#mysql845-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.3`](#mysql93)
-	[`mysql:9.3-oracle`](#mysql93-oracle)
-	[`mysql:9.3-oraclelinux9`](#mysql93-oraclelinux9)
-	[`mysql:9.3.0`](#mysql930)
-	[`mysql:9.3.0-oracle`](#mysql930-oracle)
-	[`mysql:9.3.0-oraclelinux9`](#mysql930-oraclelinux9)
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
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:968e12b1fde035655c7a940db808b47372b70128293a38a3914e0b291c306e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:5f1d0b66d7541424a795888135ac1c37c0cd7731ddcacc1b2db9fd77507d6a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234747981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f7ec307380fca5322d5a1c706aff3370997ebb7a8fcf4b53ad249a34ccb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd9ff0e16bf6fc1664154c1fe6bc7294d9fdbfff5d707f4f27a282f5f47452`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb1d882a76a5186dcaebe72d56e111496b4543e0ba92a56952ef4210ad9354`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c08134121bfd6cef62bfdc03bfdefb209bc86993528539ada88e14a968fc7c`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 6.9 MB (6896357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc2e96984e16e824231233ec862dbbf5dc9a38bdc2ca9eba4190c1e16f499c0`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5636d7314013d6e7ae46ce039caca0fccf3d81268bb9e7854db59cbe3fbf3f6`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0ff87df77d8b47c27b9686897345e18a3b7da8de7cfd95090c26d2a5c7c39a`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 49.7 MB (49664894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9c2ecc3352b597933b9f486236340abe35150be67c59e73514322a4bb52a7d`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbde96d8818e29892eaa60aa73db1443399a33b673f1dc5d1dd0b1cb61259813`  
		Last Modified: Tue, 15 Apr 2025 00:07:39 GMT  
		Size: 128.1 MB (128102925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcb3921fdb80398e043954b6544b2fbd3107cde705a9f43977ec406f021e3e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069dfe57230c446b682c1ee824b8ebd2ae35dfdd5ffcc262077c506e2182b78e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:531e4caee0fd521a08ae745c64c46b832f3ae62fa8ab092d3d1f5ce71ad979f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14063285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60bcde09d6079d51c19f9c42e3e7d9c2032234f092cce9e0d3b66c9f1f72827`

```dockerfile
```

-	Layers:
	-	`sha256:7b2444b15625fd6b2ff8ecc03b989fc61461d4b56682ec8d00a312e81ab20ff5`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 14.0 MB (14028331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f6211596b9b912a110ec74912f79d80cc681908688afa85321f89a881ad187`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:49d3c535e60bd5bf4cd8d3692ce1b17eb4ba91ef2714ea01927c68757da1e2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230265780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf1cb2d88553a5928148ae685652ff9fc187eb5fee7ce584b659284f173c552`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c1fdca8b92e6e0713e01cb9c57ac871482d3e8ac856860293c1e5f1e38f3f4`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bc4ae690f4d47974ed149e3b5dcdeb7f796a987ca7bf42daa70f119446513c`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 48.5 MB (48530561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c7ef039dde6a40af5210a55d24bb12532df65af90c7ce7b5ec4e38cd101541`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c150de948b39b78a5944e29dfd1b911fef5473570ff06201d3fb362d0714c1`  
		Last Modified: Tue, 15 Apr 2025 00:13:42 GMT  
		Size: 126.6 MB (126647083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba120b1d9fa4b532f1cccf3b891d12a9576bec9b3ea20c2ce6c59adbb1f14c60`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242af28a3a08f127c76bc012f0e3bf0dddcd0da7b323adcd15a297f67b725543`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:6e429671e55dfdb45405242bf6ede1bd0a43f0cf1040b53a543af2b151800feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14061878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0aedccec319258c15d76d9cfaf52d89b9cc8380aa0c0f1ebaf279a1886f87b`

```dockerfile
```

-	Layers:
	-	`sha256:f91b2408cff9281945b6b8bba3b922d52ce979dbbcd49ad724f0e14b740d5ebd`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 14.0 MB (14026678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258564f928f1e3a4cd838d83d5a86cdbf71867ccd5a9475a499e403a1ecaa4eb`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 35.2 KB (35200 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:97e4193aec5aa9552d536f3e4f55de068eec4a72b96fb81639dcc97f7fd6c686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:7a711473cf6af640874c09a4cafcec6734c2e1e05a3ceb2f3b4c059b00444c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183353478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7460cf9b955b02bd45337cfc4dc0f8e9066a334a610c1f776d17540f504573d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4026058410b19c58a78234aee0fa85ff74b72e92e0fd287c695df6423628a04b`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efc9f60b4ca020edb8cf35f05b377a8ec393ec64c875c48fc6147a97a1dec9e`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 4.4 MB (4422776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb29612c8a0ce06d6f9603bc4d2ab1051c9391f5dd11ef1f56169d8bed9c10`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 1.4 MB (1446003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec5c53ca482ecea7235890fca83772f782f0de899c55a7ecfde71fe110c3a1b`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0582621e23e039b2908f283b85108456d966dabce4daa623e8074c3cf8343`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 15.3 MB (15294049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81935a6b23b28ac7789f011d290ee875f81810927161cb71f0410f0f9df20a43`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d824cb76f2bb4ec911096a81b20907186ea87c036997a9eb4c4decfe489535`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2f0cfc83f71d80f0338a792c90d6b381460f1375155c9bcf38d570c231591`  
		Last Modified: Mon, 28 Apr 2025 21:57:00 GMT  
		Size: 134.0 MB (133952739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c16287de63fc88d238e86a78b6100526631bdc91cf31502017b3edc5d1ab07`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6516d466daad6410006cd555a605ecd736ae17b99938cbf1a0e3ac9de009e`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f475918de7f3d19d670ce9c1de533b253205fc2d1b219439e15be47086e46ba3`  
		Last Modified: Mon, 28 Apr 2025 21:56:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:b4932b3569e1d3bcfa3c7a345b48262e3bd097331271ca9b2d3bc8b0b02184f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219c2b2f8a080209bae00a66c3da0292cf3935bb46bc1947f72d83d5f0c06dd6`

```dockerfile
```

-	Layers:
	-	`sha256:262d8e27bb435b8cc4562aac346258145391df420d3c67e83bad3734dafd2cb8`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 4.0 MB (3994376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae91e3461498d565c3be493b697d6a06cb02664d8554b83de7bbd35478f0c63c`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 34.3 KB (34295 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:97e4193aec5aa9552d536f3e4f55de068eec4a72b96fb81639dcc97f7fd6c686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:7a711473cf6af640874c09a4cafcec6734c2e1e05a3ceb2f3b4c059b00444c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183353478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7460cf9b955b02bd45337cfc4dc0f8e9066a334a610c1f776d17540f504573d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4026058410b19c58a78234aee0fa85ff74b72e92e0fd287c695df6423628a04b`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efc9f60b4ca020edb8cf35f05b377a8ec393ec64c875c48fc6147a97a1dec9e`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 4.4 MB (4422776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb29612c8a0ce06d6f9603bc4d2ab1051c9391f5dd11ef1f56169d8bed9c10`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 1.4 MB (1446003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec5c53ca482ecea7235890fca83772f782f0de899c55a7ecfde71fe110c3a1b`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0582621e23e039b2908f283b85108456d966dabce4daa623e8074c3cf8343`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 15.3 MB (15294049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81935a6b23b28ac7789f011d290ee875f81810927161cb71f0410f0f9df20a43`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d824cb76f2bb4ec911096a81b20907186ea87c036997a9eb4c4decfe489535`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2f0cfc83f71d80f0338a792c90d6b381460f1375155c9bcf38d570c231591`  
		Last Modified: Mon, 28 Apr 2025 21:57:00 GMT  
		Size: 134.0 MB (133952739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c16287de63fc88d238e86a78b6100526631bdc91cf31502017b3edc5d1ab07`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6516d466daad6410006cd555a605ecd736ae17b99938cbf1a0e3ac9de009e`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f475918de7f3d19d670ce9c1de533b253205fc2d1b219439e15be47086e46ba3`  
		Last Modified: Mon, 28 Apr 2025 21:56:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:b4932b3569e1d3bcfa3c7a345b48262e3bd097331271ca9b2d3bc8b0b02184f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219c2b2f8a080209bae00a66c3da0292cf3935bb46bc1947f72d83d5f0c06dd6`

```dockerfile
```

-	Layers:
	-	`sha256:262d8e27bb435b8cc4562aac346258145391df420d3c67e83bad3734dafd2cb8`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 4.0 MB (3994376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae91e3461498d565c3be493b697d6a06cb02664d8554b83de7bbd35478f0c63c`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 34.3 KB (34295 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:968e12b1fde035655c7a940db808b47372b70128293a38a3914e0b291c306e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5f1d0b66d7541424a795888135ac1c37c0cd7731ddcacc1b2db9fd77507d6a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234747981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f7ec307380fca5322d5a1c706aff3370997ebb7a8fcf4b53ad249a34ccb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd9ff0e16bf6fc1664154c1fe6bc7294d9fdbfff5d707f4f27a282f5f47452`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb1d882a76a5186dcaebe72d56e111496b4543e0ba92a56952ef4210ad9354`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c08134121bfd6cef62bfdc03bfdefb209bc86993528539ada88e14a968fc7c`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 6.9 MB (6896357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc2e96984e16e824231233ec862dbbf5dc9a38bdc2ca9eba4190c1e16f499c0`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5636d7314013d6e7ae46ce039caca0fccf3d81268bb9e7854db59cbe3fbf3f6`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0ff87df77d8b47c27b9686897345e18a3b7da8de7cfd95090c26d2a5c7c39a`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 49.7 MB (49664894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9c2ecc3352b597933b9f486236340abe35150be67c59e73514322a4bb52a7d`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbde96d8818e29892eaa60aa73db1443399a33b673f1dc5d1dd0b1cb61259813`  
		Last Modified: Tue, 15 Apr 2025 00:07:39 GMT  
		Size: 128.1 MB (128102925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcb3921fdb80398e043954b6544b2fbd3107cde705a9f43977ec406f021e3e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069dfe57230c446b682c1ee824b8ebd2ae35dfdd5ffcc262077c506e2182b78e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:531e4caee0fd521a08ae745c64c46b832f3ae62fa8ab092d3d1f5ce71ad979f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14063285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60bcde09d6079d51c19f9c42e3e7d9c2032234f092cce9e0d3b66c9f1f72827`

```dockerfile
```

-	Layers:
	-	`sha256:7b2444b15625fd6b2ff8ecc03b989fc61461d4b56682ec8d00a312e81ab20ff5`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 14.0 MB (14028331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f6211596b9b912a110ec74912f79d80cc681908688afa85321f89a881ad187`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:49d3c535e60bd5bf4cd8d3692ce1b17eb4ba91ef2714ea01927c68757da1e2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230265780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf1cb2d88553a5928148ae685652ff9fc187eb5fee7ce584b659284f173c552`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c1fdca8b92e6e0713e01cb9c57ac871482d3e8ac856860293c1e5f1e38f3f4`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bc4ae690f4d47974ed149e3b5dcdeb7f796a987ca7bf42daa70f119446513c`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 48.5 MB (48530561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c7ef039dde6a40af5210a55d24bb12532df65af90c7ce7b5ec4e38cd101541`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c150de948b39b78a5944e29dfd1b911fef5473570ff06201d3fb362d0714c1`  
		Last Modified: Tue, 15 Apr 2025 00:13:42 GMT  
		Size: 126.6 MB (126647083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba120b1d9fa4b532f1cccf3b891d12a9576bec9b3ea20c2ce6c59adbb1f14c60`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242af28a3a08f127c76bc012f0e3bf0dddcd0da7b323adcd15a297f67b725543`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6e429671e55dfdb45405242bf6ede1bd0a43f0cf1040b53a543af2b151800feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14061878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0aedccec319258c15d76d9cfaf52d89b9cc8380aa0c0f1ebaf279a1886f87b`

```dockerfile
```

-	Layers:
	-	`sha256:f91b2408cff9281945b6b8bba3b922d52ce979dbbcd49ad724f0e14b740d5ebd`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 14.0 MB (14026678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258564f928f1e3a4cd838d83d5a86cdbf71867ccd5a9475a499e403a1ecaa4eb`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 35.2 KB (35200 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:968e12b1fde035655c7a940db808b47372b70128293a38a3914e0b291c306e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5f1d0b66d7541424a795888135ac1c37c0cd7731ddcacc1b2db9fd77507d6a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234747981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f7ec307380fca5322d5a1c706aff3370997ebb7a8fcf4b53ad249a34ccb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd9ff0e16bf6fc1664154c1fe6bc7294d9fdbfff5d707f4f27a282f5f47452`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb1d882a76a5186dcaebe72d56e111496b4543e0ba92a56952ef4210ad9354`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c08134121bfd6cef62bfdc03bfdefb209bc86993528539ada88e14a968fc7c`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 6.9 MB (6896357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc2e96984e16e824231233ec862dbbf5dc9a38bdc2ca9eba4190c1e16f499c0`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5636d7314013d6e7ae46ce039caca0fccf3d81268bb9e7854db59cbe3fbf3f6`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0ff87df77d8b47c27b9686897345e18a3b7da8de7cfd95090c26d2a5c7c39a`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 49.7 MB (49664894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9c2ecc3352b597933b9f486236340abe35150be67c59e73514322a4bb52a7d`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbde96d8818e29892eaa60aa73db1443399a33b673f1dc5d1dd0b1cb61259813`  
		Last Modified: Tue, 15 Apr 2025 00:07:39 GMT  
		Size: 128.1 MB (128102925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcb3921fdb80398e043954b6544b2fbd3107cde705a9f43977ec406f021e3e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069dfe57230c446b682c1ee824b8ebd2ae35dfdd5ffcc262077c506e2182b78e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:531e4caee0fd521a08ae745c64c46b832f3ae62fa8ab092d3d1f5ce71ad979f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14063285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60bcde09d6079d51c19f9c42e3e7d9c2032234f092cce9e0d3b66c9f1f72827`

```dockerfile
```

-	Layers:
	-	`sha256:7b2444b15625fd6b2ff8ecc03b989fc61461d4b56682ec8d00a312e81ab20ff5`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 14.0 MB (14028331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f6211596b9b912a110ec74912f79d80cc681908688afa85321f89a881ad187`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:49d3c535e60bd5bf4cd8d3692ce1b17eb4ba91ef2714ea01927c68757da1e2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230265780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf1cb2d88553a5928148ae685652ff9fc187eb5fee7ce584b659284f173c552`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c1fdca8b92e6e0713e01cb9c57ac871482d3e8ac856860293c1e5f1e38f3f4`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bc4ae690f4d47974ed149e3b5dcdeb7f796a987ca7bf42daa70f119446513c`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 48.5 MB (48530561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c7ef039dde6a40af5210a55d24bb12532df65af90c7ce7b5ec4e38cd101541`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c150de948b39b78a5944e29dfd1b911fef5473570ff06201d3fb362d0714c1`  
		Last Modified: Tue, 15 Apr 2025 00:13:42 GMT  
		Size: 126.6 MB (126647083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba120b1d9fa4b532f1cccf3b891d12a9576bec9b3ea20c2ce6c59adbb1f14c60`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242af28a3a08f127c76bc012f0e3bf0dddcd0da7b323adcd15a297f67b725543`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6e429671e55dfdb45405242bf6ede1bd0a43f0cf1040b53a543af2b151800feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14061878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0aedccec319258c15d76d9cfaf52d89b9cc8380aa0c0f1ebaf279a1886f87b`

```dockerfile
```

-	Layers:
	-	`sha256:f91b2408cff9281945b6b8bba3b922d52ce979dbbcd49ad724f0e14b740d5ebd`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 14.0 MB (14026678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258564f928f1e3a4cd838d83d5a86cdbf71867ccd5a9475a499e403a1ecaa4eb`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 35.2 KB (35200 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42`

```console
$ docker pull mysql@sha256:968e12b1fde035655c7a940db808b47372b70128293a38a3914e0b291c306e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42` - linux; amd64

```console
$ docker pull mysql@sha256:5f1d0b66d7541424a795888135ac1c37c0cd7731ddcacc1b2db9fd77507d6a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234747981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f7ec307380fca5322d5a1c706aff3370997ebb7a8fcf4b53ad249a34ccb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd9ff0e16bf6fc1664154c1fe6bc7294d9fdbfff5d707f4f27a282f5f47452`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb1d882a76a5186dcaebe72d56e111496b4543e0ba92a56952ef4210ad9354`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c08134121bfd6cef62bfdc03bfdefb209bc86993528539ada88e14a968fc7c`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 6.9 MB (6896357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc2e96984e16e824231233ec862dbbf5dc9a38bdc2ca9eba4190c1e16f499c0`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5636d7314013d6e7ae46ce039caca0fccf3d81268bb9e7854db59cbe3fbf3f6`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0ff87df77d8b47c27b9686897345e18a3b7da8de7cfd95090c26d2a5c7c39a`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 49.7 MB (49664894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9c2ecc3352b597933b9f486236340abe35150be67c59e73514322a4bb52a7d`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbde96d8818e29892eaa60aa73db1443399a33b673f1dc5d1dd0b1cb61259813`  
		Last Modified: Tue, 15 Apr 2025 00:07:39 GMT  
		Size: 128.1 MB (128102925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcb3921fdb80398e043954b6544b2fbd3107cde705a9f43977ec406f021e3e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069dfe57230c446b682c1ee824b8ebd2ae35dfdd5ffcc262077c506e2182b78e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42` - unknown; unknown

```console
$ docker pull mysql@sha256:531e4caee0fd521a08ae745c64c46b832f3ae62fa8ab092d3d1f5ce71ad979f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14063285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60bcde09d6079d51c19f9c42e3e7d9c2032234f092cce9e0d3b66c9f1f72827`

```dockerfile
```

-	Layers:
	-	`sha256:7b2444b15625fd6b2ff8ecc03b989fc61461d4b56682ec8d00a312e81ab20ff5`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 14.0 MB (14028331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f6211596b9b912a110ec74912f79d80cc681908688afa85321f89a881ad187`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.42` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:49d3c535e60bd5bf4cd8d3692ce1b17eb4ba91ef2714ea01927c68757da1e2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230265780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf1cb2d88553a5928148ae685652ff9fc187eb5fee7ce584b659284f173c552`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c1fdca8b92e6e0713e01cb9c57ac871482d3e8ac856860293c1e5f1e38f3f4`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bc4ae690f4d47974ed149e3b5dcdeb7f796a987ca7bf42daa70f119446513c`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 48.5 MB (48530561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c7ef039dde6a40af5210a55d24bb12532df65af90c7ce7b5ec4e38cd101541`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c150de948b39b78a5944e29dfd1b911fef5473570ff06201d3fb362d0714c1`  
		Last Modified: Tue, 15 Apr 2025 00:13:42 GMT  
		Size: 126.6 MB (126647083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba120b1d9fa4b532f1cccf3b891d12a9576bec9b3ea20c2ce6c59adbb1f14c60`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242af28a3a08f127c76bc012f0e3bf0dddcd0da7b323adcd15a297f67b725543`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42` - unknown; unknown

```console
$ docker pull mysql@sha256:6e429671e55dfdb45405242bf6ede1bd0a43f0cf1040b53a543af2b151800feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14061878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0aedccec319258c15d76d9cfaf52d89b9cc8380aa0c0f1ebaf279a1886f87b`

```dockerfile
```

-	Layers:
	-	`sha256:f91b2408cff9281945b6b8bba3b922d52ce979dbbcd49ad724f0e14b740d5ebd`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 14.0 MB (14026678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258564f928f1e3a4cd838d83d5a86cdbf71867ccd5a9475a499e403a1ecaa4eb`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 35.2 KB (35200 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-bookworm`

```console
$ docker pull mysql@sha256:97e4193aec5aa9552d536f3e4f55de068eec4a72b96fb81639dcc97f7fd6c686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.42-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:7a711473cf6af640874c09a4cafcec6734c2e1e05a3ceb2f3b4c059b00444c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183353478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7460cf9b955b02bd45337cfc4dc0f8e9066a334a610c1f776d17540f504573d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4026058410b19c58a78234aee0fa85ff74b72e92e0fd287c695df6423628a04b`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efc9f60b4ca020edb8cf35f05b377a8ec393ec64c875c48fc6147a97a1dec9e`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 4.4 MB (4422776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb29612c8a0ce06d6f9603bc4d2ab1051c9391f5dd11ef1f56169d8bed9c10`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 1.4 MB (1446003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec5c53ca482ecea7235890fca83772f782f0de899c55a7ecfde71fe110c3a1b`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0582621e23e039b2908f283b85108456d966dabce4daa623e8074c3cf8343`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 15.3 MB (15294049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81935a6b23b28ac7789f011d290ee875f81810927161cb71f0410f0f9df20a43`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d824cb76f2bb4ec911096a81b20907186ea87c036997a9eb4c4decfe489535`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2f0cfc83f71d80f0338a792c90d6b381460f1375155c9bcf38d570c231591`  
		Last Modified: Mon, 28 Apr 2025 21:57:00 GMT  
		Size: 134.0 MB (133952739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c16287de63fc88d238e86a78b6100526631bdc91cf31502017b3edc5d1ab07`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6516d466daad6410006cd555a605ecd736ae17b99938cbf1a0e3ac9de009e`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f475918de7f3d19d670ce9c1de533b253205fc2d1b219439e15be47086e46ba3`  
		Last Modified: Mon, 28 Apr 2025 21:56:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:b4932b3569e1d3bcfa3c7a345b48262e3bd097331271ca9b2d3bc8b0b02184f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219c2b2f8a080209bae00a66c3da0292cf3935bb46bc1947f72d83d5f0c06dd6`

```dockerfile
```

-	Layers:
	-	`sha256:262d8e27bb435b8cc4562aac346258145391df420d3c67e83bad3734dafd2cb8`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 4.0 MB (3994376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae91e3461498d565c3be493b697d6a06cb02664d8554b83de7bbd35478f0c63c`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 34.3 KB (34295 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-debian`

```console
$ docker pull mysql@sha256:97e4193aec5aa9552d536f3e4f55de068eec4a72b96fb81639dcc97f7fd6c686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.42-debian` - linux; amd64

```console
$ docker pull mysql@sha256:7a711473cf6af640874c09a4cafcec6734c2e1e05a3ceb2f3b4c059b00444c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183353478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7460cf9b955b02bd45337cfc4dc0f8e9066a334a610c1f776d17540f504573d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4026058410b19c58a78234aee0fa85ff74b72e92e0fd287c695df6423628a04b`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efc9f60b4ca020edb8cf35f05b377a8ec393ec64c875c48fc6147a97a1dec9e`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 4.4 MB (4422776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb29612c8a0ce06d6f9603bc4d2ab1051c9391f5dd11ef1f56169d8bed9c10`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 1.4 MB (1446003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec5c53ca482ecea7235890fca83772f782f0de899c55a7ecfde71fe110c3a1b`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0582621e23e039b2908f283b85108456d966dabce4daa623e8074c3cf8343`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 15.3 MB (15294049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81935a6b23b28ac7789f011d290ee875f81810927161cb71f0410f0f9df20a43`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d824cb76f2bb4ec911096a81b20907186ea87c036997a9eb4c4decfe489535`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2f0cfc83f71d80f0338a792c90d6b381460f1375155c9bcf38d570c231591`  
		Last Modified: Mon, 28 Apr 2025 21:57:00 GMT  
		Size: 134.0 MB (133952739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c16287de63fc88d238e86a78b6100526631bdc91cf31502017b3edc5d1ab07`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6516d466daad6410006cd555a605ecd736ae17b99938cbf1a0e3ac9de009e`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f475918de7f3d19d670ce9c1de533b253205fc2d1b219439e15be47086e46ba3`  
		Last Modified: Mon, 28 Apr 2025 21:56:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:b4932b3569e1d3bcfa3c7a345b48262e3bd097331271ca9b2d3bc8b0b02184f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219c2b2f8a080209bae00a66c3da0292cf3935bb46bc1947f72d83d5f0c06dd6`

```dockerfile
```

-	Layers:
	-	`sha256:262d8e27bb435b8cc4562aac346258145391df420d3c67e83bad3734dafd2cb8`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 4.0 MB (3994376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae91e3461498d565c3be493b697d6a06cb02664d8554b83de7bbd35478f0c63c`  
		Last Modified: Mon, 28 Apr 2025 21:56:57 GMT  
		Size: 34.3 KB (34295 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-oracle`

```console
$ docker pull mysql@sha256:968e12b1fde035655c7a940db808b47372b70128293a38a3914e0b291c306e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5f1d0b66d7541424a795888135ac1c37c0cd7731ddcacc1b2db9fd77507d6a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234747981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f7ec307380fca5322d5a1c706aff3370997ebb7a8fcf4b53ad249a34ccb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd9ff0e16bf6fc1664154c1fe6bc7294d9fdbfff5d707f4f27a282f5f47452`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb1d882a76a5186dcaebe72d56e111496b4543e0ba92a56952ef4210ad9354`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c08134121bfd6cef62bfdc03bfdefb209bc86993528539ada88e14a968fc7c`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 6.9 MB (6896357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc2e96984e16e824231233ec862dbbf5dc9a38bdc2ca9eba4190c1e16f499c0`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5636d7314013d6e7ae46ce039caca0fccf3d81268bb9e7854db59cbe3fbf3f6`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0ff87df77d8b47c27b9686897345e18a3b7da8de7cfd95090c26d2a5c7c39a`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 49.7 MB (49664894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9c2ecc3352b597933b9f486236340abe35150be67c59e73514322a4bb52a7d`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbde96d8818e29892eaa60aa73db1443399a33b673f1dc5d1dd0b1cb61259813`  
		Last Modified: Tue, 15 Apr 2025 00:07:39 GMT  
		Size: 128.1 MB (128102925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcb3921fdb80398e043954b6544b2fbd3107cde705a9f43977ec406f021e3e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069dfe57230c446b682c1ee824b8ebd2ae35dfdd5ffcc262077c506e2182b78e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:531e4caee0fd521a08ae745c64c46b832f3ae62fa8ab092d3d1f5ce71ad979f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14063285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60bcde09d6079d51c19f9c42e3e7d9c2032234f092cce9e0d3b66c9f1f72827`

```dockerfile
```

-	Layers:
	-	`sha256:7b2444b15625fd6b2ff8ecc03b989fc61461d4b56682ec8d00a312e81ab20ff5`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 14.0 MB (14028331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f6211596b9b912a110ec74912f79d80cc681908688afa85321f89a881ad187`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.42-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:49d3c535e60bd5bf4cd8d3692ce1b17eb4ba91ef2714ea01927c68757da1e2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230265780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf1cb2d88553a5928148ae685652ff9fc187eb5fee7ce584b659284f173c552`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c1fdca8b92e6e0713e01cb9c57ac871482d3e8ac856860293c1e5f1e38f3f4`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bc4ae690f4d47974ed149e3b5dcdeb7f796a987ca7bf42daa70f119446513c`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 48.5 MB (48530561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c7ef039dde6a40af5210a55d24bb12532df65af90c7ce7b5ec4e38cd101541`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c150de948b39b78a5944e29dfd1b911fef5473570ff06201d3fb362d0714c1`  
		Last Modified: Tue, 15 Apr 2025 00:13:42 GMT  
		Size: 126.6 MB (126647083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba120b1d9fa4b532f1cccf3b891d12a9576bec9b3ea20c2ce6c59adbb1f14c60`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242af28a3a08f127c76bc012f0e3bf0dddcd0da7b323adcd15a297f67b725543`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6e429671e55dfdb45405242bf6ede1bd0a43f0cf1040b53a543af2b151800feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14061878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0aedccec319258c15d76d9cfaf52d89b9cc8380aa0c0f1ebaf279a1886f87b`

```dockerfile
```

-	Layers:
	-	`sha256:f91b2408cff9281945b6b8bba3b922d52ce979dbbcd49ad724f0e14b740d5ebd`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 14.0 MB (14026678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258564f928f1e3a4cd838d83d5a86cdbf71867ccd5a9475a499e403a1ecaa4eb`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 35.2 KB (35200 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-oraclelinux9`

```console
$ docker pull mysql@sha256:968e12b1fde035655c7a940db808b47372b70128293a38a3914e0b291c306e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5f1d0b66d7541424a795888135ac1c37c0cd7731ddcacc1b2db9fd77507d6a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234747981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f7ec307380fca5322d5a1c706aff3370997ebb7a8fcf4b53ad249a34ccb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd9ff0e16bf6fc1664154c1fe6bc7294d9fdbfff5d707f4f27a282f5f47452`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb1d882a76a5186dcaebe72d56e111496b4543e0ba92a56952ef4210ad9354`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c08134121bfd6cef62bfdc03bfdefb209bc86993528539ada88e14a968fc7c`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 6.9 MB (6896357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc2e96984e16e824231233ec862dbbf5dc9a38bdc2ca9eba4190c1e16f499c0`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5636d7314013d6e7ae46ce039caca0fccf3d81268bb9e7854db59cbe3fbf3f6`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0ff87df77d8b47c27b9686897345e18a3b7da8de7cfd95090c26d2a5c7c39a`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 49.7 MB (49664894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9c2ecc3352b597933b9f486236340abe35150be67c59e73514322a4bb52a7d`  
		Last Modified: Tue, 15 Apr 2025 00:07:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbde96d8818e29892eaa60aa73db1443399a33b673f1dc5d1dd0b1cb61259813`  
		Last Modified: Tue, 15 Apr 2025 00:07:39 GMT  
		Size: 128.1 MB (128102925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcb3921fdb80398e043954b6544b2fbd3107cde705a9f43977ec406f021e3e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069dfe57230c446b682c1ee824b8ebd2ae35dfdd5ffcc262077c506e2182b78e`  
		Last Modified: Tue, 15 Apr 2025 00:07:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:531e4caee0fd521a08ae745c64c46b832f3ae62fa8ab092d3d1f5ce71ad979f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14063285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60bcde09d6079d51c19f9c42e3e7d9c2032234f092cce9e0d3b66c9f1f72827`

```dockerfile
```

-	Layers:
	-	`sha256:7b2444b15625fd6b2ff8ecc03b989fc61461d4b56682ec8d00a312e81ab20ff5`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 14.0 MB (14028331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f6211596b9b912a110ec74912f79d80cc681908688afa85321f89a881ad187`  
		Last Modified: Tue, 15 Apr 2025 00:07:35 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.42-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:49d3c535e60bd5bf4cd8d3692ce1b17eb4ba91ef2714ea01927c68757da1e2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230265780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf1cb2d88553a5928148ae685652ff9fc187eb5fee7ce584b659284f173c552`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c1fdca8b92e6e0713e01cb9c57ac871482d3e8ac856860293c1e5f1e38f3f4`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bc4ae690f4d47974ed149e3b5dcdeb7f796a987ca7bf42daa70f119446513c`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 48.5 MB (48530561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c7ef039dde6a40af5210a55d24bb12532df65af90c7ce7b5ec4e38cd101541`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c150de948b39b78a5944e29dfd1b911fef5473570ff06201d3fb362d0714c1`  
		Last Modified: Tue, 15 Apr 2025 00:13:42 GMT  
		Size: 126.6 MB (126647083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba120b1d9fa4b532f1cccf3b891d12a9576bec9b3ea20c2ce6c59adbb1f14c60`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242af28a3a08f127c76bc012f0e3bf0dddcd0da7b323adcd15a297f67b725543`  
		Last Modified: Tue, 15 Apr 2025 00:13:39 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6e429671e55dfdb45405242bf6ede1bd0a43f0cf1040b53a543af2b151800feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14061878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0aedccec319258c15d76d9cfaf52d89b9cc8380aa0c0f1ebaf279a1886f87b`

```dockerfile
```

-	Layers:
	-	`sha256:f91b2408cff9281945b6b8bba3b922d52ce979dbbcd49ad724f0e14b740d5ebd`  
		Last Modified: Tue, 15 Apr 2025 00:13:40 GMT  
		Size: 14.0 MB (14026678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258564f928f1e3a4cd838d83d5a86cdbf71867ccd5a9475a499e403a1ecaa4eb`  
		Last Modified: Tue, 15 Apr 2025 00:13:38 GMT  
		Size: 35.2 KB (35200 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.5` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5-oracle`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.5-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5-oraclelinux9`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3-oracle`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3-oraclelinux9`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0-oracle`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0-oraclelinux9`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:3a89257a3a979e46e3650628bea227a6bc318a2bdc95f954489ec89573a4c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dc6acfdfcf111858d8ec72daa23308a54377dc458d10ba4dd9484de2ea3cbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235751516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6ba656d1061d948799c1a4d0f0aee0968a62ee7cd7932ad6c46e9c72b045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c228f7bea3b0f60b2fef520cceb4d6cc3082f095766bae892bbb95804228de7`  
		Last Modified: Tue, 15 Apr 2025 21:53:28 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ec4c227a41b57d7ad471d769e8cd848ad2e69a4415dce858e0436e31f9b4d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb416885cc1f01116904c5a0e7d267ee22d41a2c9d2166a0f095fc8eedd6fa6a`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 6.9 MB (6896518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eaa68c59217c97f8d11b210b92e23124269d73e316c5c3a262efd855bfd0a1`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8f079852f5cb68875c54ae4d9b521381b609465d247ad19dbaf2d82aa4c0c`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5287da18a2fc9f6a2a5856d4188102e040f72d12c71f9880e7e78a50f0821`  
		Last Modified: Tue, 15 Apr 2025 21:53:32 GMT  
		Size: 47.6 MB (47625516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4571eacc074121c001f7143dece938291bf425cf33ae637f84bc483468324`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182039f5bee38952c2c37bc505eca3814ef8d5922694532053c92f98ce15a63d`  
		Last Modified: Tue, 15 Apr 2025 21:53:34 GMT  
		Size: 131.1 MB (131145791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd4e5cd318c864fec53c5d777e72af443ce7e7b288bcdc24058022f7f25399`  
		Last Modified: Tue, 15 Apr 2025 21:53:30 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:73338c7d36ea557c94c0502c2d80fa303abc189617aad2ab1ada47471b34fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14339403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c947425ac788f9a07334ca598628c2f7040deaa0ba9764e283432fcc18d8e`

```dockerfile
```

-	Layers:
	-	`sha256:9e15e5c014a4f8103026d7f9ecc75d337d800dc0ff5a56e2e4bf45131609b20d`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 14.3 MB (14305152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759bc56263efb19ae8177eb6dcad586b6389630b1f343fd3ac262c453e28b459`  
		Last Modified: Tue, 15 Apr 2025 21:53:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:802f7fb60513501fd3e5a07519818c8be6ec16830138c04d2c9dce8e30c24a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231108026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9cb03db0b387579c9ddaef8817931a4d2d0a702034db46a88efa79497da2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ac94b602fdd92102ce95ee2abf51b9be9b639a618ea8aa16dae164570cd03`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec450c6393c6866a42e1550475788f427dde80bda6b023c490937b8bb5e17d5`  
		Last Modified: Tue, 15 Apr 2025 00:12:04 GMT  
		Size: 46.5 MB (46510681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d6647a9d0a22e8f03f0a5f3105c86b3e95d0b4f5e348c1101a7f8e1e8c224`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a62484e6b2beac2945d3f742285d0a004954f6a9213ac17116b79145c95927`  
		Last Modified: Tue, 15 Apr 2025 21:57:15 GMT  
		Size: 129.5 MB (129509321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87885fb56d1dd1f868479f45b4aea2bae742a30553c60738c47541d8b1acf67`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6852ae60bf9a796d87675cfb818e0182d68b22a6de541086c0fadc7ef74bd12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14338126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dcde8f740114c1a1d316610267296ac517288e6636dd0bdb6ac4a2ad35c46b`

```dockerfile
```

-	Layers:
	-	`sha256:7e80f92e80d293557dd2627a8d70b4c73531376c9df5cef77b8eaf58885f8827`  
		Last Modified: Tue, 15 Apr 2025 21:57:12 GMT  
		Size: 14.3 MB (14303571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae2c7a64800dff774ddaf23b9a6b2a1853c560deb9bf86822e3f60b2cad657`  
		Last Modified: Tue, 15 Apr 2025 21:57:11 GMT  
		Size: 34.6 KB (34555 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:7839322bd6c3174a699586c3ea36314c59b61b4ce01b4146951818b94aef5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:91460a1990e5fff3279efe635630ac6edd391926ca80a985e0ed658274c53e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257754401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d796bebc27d70aca324403b4f16bca96eba549b39633c9ba55f2bc37bf85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa811e9a869e4d562b9f03ec9af6fb8661a4df178c56e76c2be8a938a46d29c6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2982daa21747c731aa9754c9e979ffa0bc28924addb46bf9f66e7348743d6`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d7076afe36a3c2481787eec09ba6b5d569729e567902b56f63b6a2f2af122`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 6.9 MB (6896500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4e5ea3754615d23911db0da95f2bc3cb49a562a713c1f49f085536e5b927e`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275c0ff11a061a9a702d709e3f42dca0130eca89c6cddd26c2c4bbd45da3abe`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 48.4 MB (48420583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792ea2d4e0e612ec07b8cb60179d2632e2f5171c5d89eaeca6710cebc117446`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b2cd84940c04b8d9e00143eecfd1ce186ed5c7ded71f0acd84ee5a80fedd`  
		Last Modified: Tue, 15 Apr 2025 00:08:09 GMT  
		Size: 152.4 MB (152353623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9451290759dff497c8dad61699344564a00ba8627d603c69e46189ee2f1a2c51`  
		Last Modified: Tue, 15 Apr 2025 00:08:07 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d58009a64dd3b1364967d2ac14424ac06785d45eb0d8d43972c4a1e3000fe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dc241c091a345be2f3b6c85bda4f05ad93d9e6e1b6cf17a5f54d1b774178d`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2c8feddf5ce80b2a868b521d0741fb2fc2a849ddd48154beb48b34f84ea20`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 15.1 MB (15071650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870661ac452a0c62d6dea4782bc2e19c12c92b0b7ad22dab2f30f2b13a852a22`  
		Last Modified: Tue, 15 Apr 2025 00:08:06 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:90742fac43d76b6358ff0d8fd3d0a6928407002c29c2a741633cc787c906af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067aec32d6b2fe3b4c861333ee0d1b366aa0eef7b7c6de6d4a619c4d12724040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f39a1086c35732fd8f86179dd9656590f282d24bc27b7582f494a3e7eee02`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7d8b9ec0f73de292059601f40e8050d075f382ae3b91d42784424b365f06b`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 913.4 KB (913440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0ce28ec2e3770d6e448cceb3d626db84b7b4854d70d2b344ab301f02c57c0`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 6.5 MB (6490285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638509fc8b3badea0ef2ff69eff0bbe0a14aa36bcb0d39fc5c61ce8dc9f48f36`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5c634f2aa51d39049c212ffa44155bdc7b08cd1a2d5354157ff9a47c7e7f5`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c3cfdb54647cd242c5fc7c0de94d46989fc0d25954b4d959c52348d04173c`  
		Last Modified: Tue, 15 Apr 2025 00:10:27 GMT  
		Size: 47.3 MB (47272827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c1fe576aaf34d0f47a4b298c277931645f329e66393cc603f5e854b9de149`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee65fddcb97d5da098eb0ac689555677b50c90f46f2ad5f24d76cd5d5348e7`  
		Last Modified: Tue, 15 Apr 2025 00:10:31 GMT  
		Size: 150.6 MB (150632468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ebc7729381763f04d5db20c87a6ab7d053a2fa7c38db1ea449f61a263cbd9`  
		Last Modified: Tue, 15 Apr 2025 00:10:26 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b55bb973c422c6c7d296eb3a5e313b507d5e1e8e920512b03192cb7dfd5fa637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15105764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd174b018e83f88d53f30c2bf1360b9339c8da16a1986f782c23d6261c8c3c80`

```dockerfile
```

-	Layers:
	-	`sha256:4acd32603b899cee60639d1bcef72e2a7b5f8f7a5a9ff625606d1bc4a207447d`  
		Last Modified: Tue, 15 Apr 2025 00:10:25 GMT  
		Size: 15.1 MB (15070105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aa829395f0e547d5c3f5c20b989bbbf582c9f69dfaa4678daeb495c699b703`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
