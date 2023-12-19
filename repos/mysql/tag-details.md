<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux8`](#mysql8-oraclelinux8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-bullseye`](#mysql80-bullseye)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0-oraclelinux8`](#mysql80-oraclelinux8)
-	[`mysql:8.0.35`](#mysql8035)
-	[`mysql:8.0.35-bullseye`](#mysql8035-bullseye)
-	[`mysql:8.0.35-debian`](#mysql8035-debian)
-	[`mysql:8.0.35-oracle`](#mysql8035-oracle)
-	[`mysql:8.0.35-oraclelinux8`](#mysql8035-oraclelinux8)
-	[`mysql:8.2`](#mysql82)
-	[`mysql:8.2-oracle`](#mysql82-oracle)
-	[`mysql:8.2-oraclelinux8`](#mysql82-oraclelinux8)
-	[`mysql:8.2.0`](#mysql820)
-	[`mysql:8.2.0-oracle`](#mysql820-oracle)
-	[`mysql:8.2.0-oraclelinux8`](#mysql820-oraclelinux8)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux8`](#mysqlinnovation-oraclelinux8)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux8`](#mysqloraclelinux8)

## `mysql:8`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux8`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:e8aded859189ea25dfc4371c7079941be835eb91a54334dd3fa82a9259c26dab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:124709177dfe53732029653081cf52378215bd8e3f10f14e94d490969f680b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173759219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300df64d4be784f8992d62b87a2a3f32f28ffa54fd4448f720e8e55ef33270f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e33690e46ba8482569a79e2bf66c8c7a53cbc22f7bebea8cc5bca7e9051f65`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 4.6 MB (4606817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ea003555d1dd0c7a9a5ceaa18bd7208d17f375fe8412b2c9a83451cda6782`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79abd900d0600d9d60fbb972222bd116a7882155ea82c8e8efa97edf023d3fb`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d721b014e95566c0fc5ce36065d6a8b11eed348ab158fbcc9ac4b585e8650c`  
		Last Modified: Thu, 14 Dec 2023 18:52:22 GMT  
		Size: 58.5 MB (58514574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba9f26e807f4e3dcd030bdcf103f5d5079de6f86d66406e91cfbe8e9fc56c02`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7be8506e77574efc8fc9fa164fa7d87e16506aefe111afff11aefe5ef9502c3`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 58.3 MB (58325400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef9735ba310beee320a5fec6fe2f305feae49cfaf30b88db33097efc3a53638`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768daf85511c86ca05c1f6238566fbce6f83fcc8274a39dca20bc30c448d3131`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:9129d84df03f3c36711914ec48d54695fa051279e48f785a6ea0d4fb9f32eeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350f69bfd3fc16abdaad5604ede6ff6751376b89cdfa23975d22ffad66aba41a`

```dockerfile
```

-	Layers:
	-	`sha256:88fbb3798072a16d864f697c5d90fe255e121b9f271cfefaa7f2c9a24283b377`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 11.6 MB (11567393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd56e84fd5575b533c7fb113319b86551f2a9379cd98bf1039e8fcff82c9f6c`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 33.9 KB (33910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8ee2fe7eaf935ed89b47d6010f6df90259b3609d8df5d87d232a6bc36f0bc075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f81235988528166fd0ad151cf78258b4ecf4565383c9e95ee6557470dde3ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2d4a8cba602b5e3cd65d5e0557988bcbd78b091afb3f6ae0d15864790987f`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba09d9fb3dfd35ff7ebbb6eb20bd59a35b737aec5e0e2f2c42eb50dda9d1e1`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 57.6 MB (57573677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3039dd1391bc16761b31a730472044ed80f3817b431f9de14e0b2b9e5949a66e`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4d0901f4a72dd35f6f7f609dbcc9e9d4cc321ed55cad8b778a73cd0e8b4132`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 64.6 MB (64575659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ffadc976d782ad9beaafd96646c04a37a91ab42bec7c3340d312ebe6d30bfe`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce24b8ac6b4928227fc12ef8569db0eb81194b07b97b2b25a7ac3f59ffaf9232`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:93dd96ed5c4dfaad500931c8bd5fef986d4713062b42d2c18bbf132b9ef88922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11599722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa4b66addb7ddb598bbf216c63487583739eb6b75a905df678be0462f6852c1`

```dockerfile
```

-	Layers:
	-	`sha256:fa10120f60379e910b2c802d1f14daf9abc49c54d75d693ff079cc9df930f814`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 11.6 MB (11565969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd9a910678b2ec061d21467e0bfad540d513b009275b0c7d4805f0ee1b19b16d`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 33.8 KB (33753 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bullseye`

```console
$ docker pull mysql@sha256:033a00e6355f3348487933cd9572984d4574b8cac59a71434a4a4b74504d4282
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bullseye` - linux; amd64

```console
$ docker pull mysql@sha256:bda410b1ba9fa28233d34669438e1ee3cd40d08efe7db27a754fc6ef30834cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179126201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c5e28586043f1155dcf5769a62ce3fbc0031a0a3d90eb64d465120cb56ce0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 21:28:23 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENV GOSU_VERSION=1.16
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 Dec 2023 21:28:23 GMT
ENV MYSQL_VERSION=8.0.35-1debian11
# Fri, 15 Dec 2023 21:28:23 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 Dec 2023 21:28:23 GMT
COPY config/ /etc/mysql/ # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Dec 2023 21:28:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 15 Dec 2023 21:28:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b01c838fc79b37e322ae5a16f84a6ccc27ca133bee2874090751536789ef073`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8500e12244dd81352ba29546b575a15e83614aa7d752b6fd4f3a367e57c17e`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 4.2 MB (4207540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae228aa190a86352dce1c5573ae6e257a0e5af720c7012fe220e59b09504308`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 1.5 MB (1472510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fcd497cdbd53c1e265f6ff528cdd3a53c74500fe4404f197f4364ceed88c20`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65598fbce0667e0315c4481d43dd19851f4668c09f985ff32d13f2050f38c4df`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 12.5 MB (12454934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1e8cdfe04bbe14fd7099571a0cb611c1c63dfa2989da39eb7a75b8e9df5b08`  
		Last Modified: Sat, 16 Dec 2023 00:52:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acc0935e72ada43cb191dea71e8be359acc5ad5f5040056e973068fd48cf52a`  
		Last Modified: Sat, 16 Dec 2023 00:52:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76ed920e910d82447965f5c1f55efe5bb069af159fe23772d9c688b64be115`  
		Last Modified: Sat, 16 Dec 2023 00:52:33 GMT  
		Size: 129.6 MB (129562531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1e5b45feffe9aa474e2e16f123cd5129e69a69245c24d51ffb2706e25131a3`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb4abbe78619511c97edfd8c05a351ded6df0f6764674db5d0d99e5012566de`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8c260c8c6fb419f092f52c57457e6bee54a428e14114955b0ee14906059134`  
		Last Modified: Sat, 16 Dec 2023 00:52:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bullseye` - unknown; unknown

```console
$ docker pull mysql@sha256:506434d0f05be405f0ae304078aea321176a73146c1ca6e2f1291264a3205747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffae5bcb9a98272dee4569d90f895bb91c0c313739ecc60f96a5e6ef22d5ab62`

```dockerfile
```

-	Layers:
	-	`sha256:82ca863aced305acc9c7efb65b0ae5ce36432aab7c270ed94849cc193e5c2d9c`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 3.6 MB (3552993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae41c906f9a76411585e2785f349f1e57a5afc61a11ebf6e13c341872370466b`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:033a00e6355f3348487933cd9572984d4574b8cac59a71434a4a4b74504d4282
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:bda410b1ba9fa28233d34669438e1ee3cd40d08efe7db27a754fc6ef30834cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179126201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c5e28586043f1155dcf5769a62ce3fbc0031a0a3d90eb64d465120cb56ce0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 21:28:23 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENV GOSU_VERSION=1.16
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 Dec 2023 21:28:23 GMT
ENV MYSQL_VERSION=8.0.35-1debian11
# Fri, 15 Dec 2023 21:28:23 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 Dec 2023 21:28:23 GMT
COPY config/ /etc/mysql/ # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Dec 2023 21:28:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 15 Dec 2023 21:28:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b01c838fc79b37e322ae5a16f84a6ccc27ca133bee2874090751536789ef073`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8500e12244dd81352ba29546b575a15e83614aa7d752b6fd4f3a367e57c17e`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 4.2 MB (4207540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae228aa190a86352dce1c5573ae6e257a0e5af720c7012fe220e59b09504308`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 1.5 MB (1472510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fcd497cdbd53c1e265f6ff528cdd3a53c74500fe4404f197f4364ceed88c20`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65598fbce0667e0315c4481d43dd19851f4668c09f985ff32d13f2050f38c4df`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 12.5 MB (12454934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1e8cdfe04bbe14fd7099571a0cb611c1c63dfa2989da39eb7a75b8e9df5b08`  
		Last Modified: Sat, 16 Dec 2023 00:52:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acc0935e72ada43cb191dea71e8be359acc5ad5f5040056e973068fd48cf52a`  
		Last Modified: Sat, 16 Dec 2023 00:52:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76ed920e910d82447965f5c1f55efe5bb069af159fe23772d9c688b64be115`  
		Last Modified: Sat, 16 Dec 2023 00:52:33 GMT  
		Size: 129.6 MB (129562531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1e5b45feffe9aa474e2e16f123cd5129e69a69245c24d51ffb2706e25131a3`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb4abbe78619511c97edfd8c05a351ded6df0f6764674db5d0d99e5012566de`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8c260c8c6fb419f092f52c57457e6bee54a428e14114955b0ee14906059134`  
		Last Modified: Sat, 16 Dec 2023 00:52:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:506434d0f05be405f0ae304078aea321176a73146c1ca6e2f1291264a3205747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffae5bcb9a98272dee4569d90f895bb91c0c313739ecc60f96a5e6ef22d5ab62`

```dockerfile
```

-	Layers:
	-	`sha256:82ca863aced305acc9c7efb65b0ae5ce36432aab7c270ed94849cc193e5c2d9c`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 3.6 MB (3552993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae41c906f9a76411585e2785f349f1e57a5afc61a11ebf6e13c341872370466b`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:e8aded859189ea25dfc4371c7079941be835eb91a54334dd3fa82a9259c26dab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:124709177dfe53732029653081cf52378215bd8e3f10f14e94d490969f680b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173759219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300df64d4be784f8992d62b87a2a3f32f28ffa54fd4448f720e8e55ef33270f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e33690e46ba8482569a79e2bf66c8c7a53cbc22f7bebea8cc5bca7e9051f65`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 4.6 MB (4606817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ea003555d1dd0c7a9a5ceaa18bd7208d17f375fe8412b2c9a83451cda6782`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79abd900d0600d9d60fbb972222bd116a7882155ea82c8e8efa97edf023d3fb`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d721b014e95566c0fc5ce36065d6a8b11eed348ab158fbcc9ac4b585e8650c`  
		Last Modified: Thu, 14 Dec 2023 18:52:22 GMT  
		Size: 58.5 MB (58514574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba9f26e807f4e3dcd030bdcf103f5d5079de6f86d66406e91cfbe8e9fc56c02`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7be8506e77574efc8fc9fa164fa7d87e16506aefe111afff11aefe5ef9502c3`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 58.3 MB (58325400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef9735ba310beee320a5fec6fe2f305feae49cfaf30b88db33097efc3a53638`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768daf85511c86ca05c1f6238566fbce6f83fcc8274a39dca20bc30c448d3131`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9129d84df03f3c36711914ec48d54695fa051279e48f785a6ea0d4fb9f32eeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350f69bfd3fc16abdaad5604ede6ff6751376b89cdfa23975d22ffad66aba41a`

```dockerfile
```

-	Layers:
	-	`sha256:88fbb3798072a16d864f697c5d90fe255e121b9f271cfefaa7f2c9a24283b377`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 11.6 MB (11567393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd56e84fd5575b533c7fb113319b86551f2a9379cd98bf1039e8fcff82c9f6c`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 33.9 KB (33910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8ee2fe7eaf935ed89b47d6010f6df90259b3609d8df5d87d232a6bc36f0bc075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f81235988528166fd0ad151cf78258b4ecf4565383c9e95ee6557470dde3ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2d4a8cba602b5e3cd65d5e0557988bcbd78b091afb3f6ae0d15864790987f`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba09d9fb3dfd35ff7ebbb6eb20bd59a35b737aec5e0e2f2c42eb50dda9d1e1`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 57.6 MB (57573677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3039dd1391bc16761b31a730472044ed80f3817b431f9de14e0b2b9e5949a66e`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4d0901f4a72dd35f6f7f609dbcc9e9d4cc321ed55cad8b778a73cd0e8b4132`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 64.6 MB (64575659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ffadc976d782ad9beaafd96646c04a37a91ab42bec7c3340d312ebe6d30bfe`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce24b8ac6b4928227fc12ef8569db0eb81194b07b97b2b25a7ac3f59ffaf9232`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:93dd96ed5c4dfaad500931c8bd5fef986d4713062b42d2c18bbf132b9ef88922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11599722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa4b66addb7ddb598bbf216c63487583739eb6b75a905df678be0462f6852c1`

```dockerfile
```

-	Layers:
	-	`sha256:fa10120f60379e910b2c802d1f14daf9abc49c54d75d693ff079cc9df930f814`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 11.6 MB (11565969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd9a910678b2ec061d21467e0bfad540d513b009275b0c7d4805f0ee1b19b16d`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 33.8 KB (33753 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux8`

```console
$ docker pull mysql@sha256:e8aded859189ea25dfc4371c7079941be835eb91a54334dd3fa82a9259c26dab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:124709177dfe53732029653081cf52378215bd8e3f10f14e94d490969f680b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173759219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300df64d4be784f8992d62b87a2a3f32f28ffa54fd4448f720e8e55ef33270f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e33690e46ba8482569a79e2bf66c8c7a53cbc22f7bebea8cc5bca7e9051f65`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 4.6 MB (4606817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ea003555d1dd0c7a9a5ceaa18bd7208d17f375fe8412b2c9a83451cda6782`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79abd900d0600d9d60fbb972222bd116a7882155ea82c8e8efa97edf023d3fb`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d721b014e95566c0fc5ce36065d6a8b11eed348ab158fbcc9ac4b585e8650c`  
		Last Modified: Thu, 14 Dec 2023 18:52:22 GMT  
		Size: 58.5 MB (58514574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba9f26e807f4e3dcd030bdcf103f5d5079de6f86d66406e91cfbe8e9fc56c02`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7be8506e77574efc8fc9fa164fa7d87e16506aefe111afff11aefe5ef9502c3`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 58.3 MB (58325400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef9735ba310beee320a5fec6fe2f305feae49cfaf30b88db33097efc3a53638`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768daf85511c86ca05c1f6238566fbce6f83fcc8274a39dca20bc30c448d3131`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:9129d84df03f3c36711914ec48d54695fa051279e48f785a6ea0d4fb9f32eeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350f69bfd3fc16abdaad5604ede6ff6751376b89cdfa23975d22ffad66aba41a`

```dockerfile
```

-	Layers:
	-	`sha256:88fbb3798072a16d864f697c5d90fe255e121b9f271cfefaa7f2c9a24283b377`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 11.6 MB (11567393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd56e84fd5575b533c7fb113319b86551f2a9379cd98bf1039e8fcff82c9f6c`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 33.9 KB (33910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8ee2fe7eaf935ed89b47d6010f6df90259b3609d8df5d87d232a6bc36f0bc075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f81235988528166fd0ad151cf78258b4ecf4565383c9e95ee6557470dde3ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2d4a8cba602b5e3cd65d5e0557988bcbd78b091afb3f6ae0d15864790987f`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba09d9fb3dfd35ff7ebbb6eb20bd59a35b737aec5e0e2f2c42eb50dda9d1e1`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 57.6 MB (57573677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3039dd1391bc16761b31a730472044ed80f3817b431f9de14e0b2b9e5949a66e`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4d0901f4a72dd35f6f7f609dbcc9e9d4cc321ed55cad8b778a73cd0e8b4132`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 64.6 MB (64575659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ffadc976d782ad9beaafd96646c04a37a91ab42bec7c3340d312ebe6d30bfe`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce24b8ac6b4928227fc12ef8569db0eb81194b07b97b2b25a7ac3f59ffaf9232`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:93dd96ed5c4dfaad500931c8bd5fef986d4713062b42d2c18bbf132b9ef88922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11599722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa4b66addb7ddb598bbf216c63487583739eb6b75a905df678be0462f6852c1`

```dockerfile
```

-	Layers:
	-	`sha256:fa10120f60379e910b2c802d1f14daf9abc49c54d75d693ff079cc9df930f814`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 11.6 MB (11565969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd9a910678b2ec061d21467e0bfad540d513b009275b0c7d4805f0ee1b19b16d`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 33.8 KB (33753 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35`

```console
$ docker pull mysql@sha256:e8aded859189ea25dfc4371c7079941be835eb91a54334dd3fa82a9259c26dab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.35` - linux; amd64

```console
$ docker pull mysql@sha256:124709177dfe53732029653081cf52378215bd8e3f10f14e94d490969f680b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173759219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300df64d4be784f8992d62b87a2a3f32f28ffa54fd4448f720e8e55ef33270f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e33690e46ba8482569a79e2bf66c8c7a53cbc22f7bebea8cc5bca7e9051f65`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 4.6 MB (4606817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ea003555d1dd0c7a9a5ceaa18bd7208d17f375fe8412b2c9a83451cda6782`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79abd900d0600d9d60fbb972222bd116a7882155ea82c8e8efa97edf023d3fb`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d721b014e95566c0fc5ce36065d6a8b11eed348ab158fbcc9ac4b585e8650c`  
		Last Modified: Thu, 14 Dec 2023 18:52:22 GMT  
		Size: 58.5 MB (58514574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba9f26e807f4e3dcd030bdcf103f5d5079de6f86d66406e91cfbe8e9fc56c02`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7be8506e77574efc8fc9fa164fa7d87e16506aefe111afff11aefe5ef9502c3`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 58.3 MB (58325400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef9735ba310beee320a5fec6fe2f305feae49cfaf30b88db33097efc3a53638`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768daf85511c86ca05c1f6238566fbce6f83fcc8274a39dca20bc30c448d3131`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35` - unknown; unknown

```console
$ docker pull mysql@sha256:9129d84df03f3c36711914ec48d54695fa051279e48f785a6ea0d4fb9f32eeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350f69bfd3fc16abdaad5604ede6ff6751376b89cdfa23975d22ffad66aba41a`

```dockerfile
```

-	Layers:
	-	`sha256:88fbb3798072a16d864f697c5d90fe255e121b9f271cfefaa7f2c9a24283b377`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 11.6 MB (11567393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd56e84fd5575b533c7fb113319b86551f2a9379cd98bf1039e8fcff82c9f6c`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 33.9 KB (33910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.35` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8ee2fe7eaf935ed89b47d6010f6df90259b3609d8df5d87d232a6bc36f0bc075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f81235988528166fd0ad151cf78258b4ecf4565383c9e95ee6557470dde3ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2d4a8cba602b5e3cd65d5e0557988bcbd78b091afb3f6ae0d15864790987f`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba09d9fb3dfd35ff7ebbb6eb20bd59a35b737aec5e0e2f2c42eb50dda9d1e1`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 57.6 MB (57573677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3039dd1391bc16761b31a730472044ed80f3817b431f9de14e0b2b9e5949a66e`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4d0901f4a72dd35f6f7f609dbcc9e9d4cc321ed55cad8b778a73cd0e8b4132`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 64.6 MB (64575659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ffadc976d782ad9beaafd96646c04a37a91ab42bec7c3340d312ebe6d30bfe`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce24b8ac6b4928227fc12ef8569db0eb81194b07b97b2b25a7ac3f59ffaf9232`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35` - unknown; unknown

```console
$ docker pull mysql@sha256:93dd96ed5c4dfaad500931c8bd5fef986d4713062b42d2c18bbf132b9ef88922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11599722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa4b66addb7ddb598bbf216c63487583739eb6b75a905df678be0462f6852c1`

```dockerfile
```

-	Layers:
	-	`sha256:fa10120f60379e910b2c802d1f14daf9abc49c54d75d693ff079cc9df930f814`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 11.6 MB (11565969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd9a910678b2ec061d21467e0bfad540d513b009275b0c7d4805f0ee1b19b16d`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 33.8 KB (33753 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35-bullseye`

```console
$ docker pull mysql@sha256:033a00e6355f3348487933cd9572984d4574b8cac59a71434a4a4b74504d4282
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.35-bullseye` - linux; amd64

```console
$ docker pull mysql@sha256:bda410b1ba9fa28233d34669438e1ee3cd40d08efe7db27a754fc6ef30834cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179126201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c5e28586043f1155dcf5769a62ce3fbc0031a0a3d90eb64d465120cb56ce0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 21:28:23 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENV GOSU_VERSION=1.16
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 Dec 2023 21:28:23 GMT
ENV MYSQL_VERSION=8.0.35-1debian11
# Fri, 15 Dec 2023 21:28:23 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 Dec 2023 21:28:23 GMT
COPY config/ /etc/mysql/ # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Dec 2023 21:28:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 15 Dec 2023 21:28:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b01c838fc79b37e322ae5a16f84a6ccc27ca133bee2874090751536789ef073`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8500e12244dd81352ba29546b575a15e83614aa7d752b6fd4f3a367e57c17e`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 4.2 MB (4207540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae228aa190a86352dce1c5573ae6e257a0e5af720c7012fe220e59b09504308`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 1.5 MB (1472510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fcd497cdbd53c1e265f6ff528cdd3a53c74500fe4404f197f4364ceed88c20`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65598fbce0667e0315c4481d43dd19851f4668c09f985ff32d13f2050f38c4df`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 12.5 MB (12454934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1e8cdfe04bbe14fd7099571a0cb611c1c63dfa2989da39eb7a75b8e9df5b08`  
		Last Modified: Sat, 16 Dec 2023 00:52:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acc0935e72ada43cb191dea71e8be359acc5ad5f5040056e973068fd48cf52a`  
		Last Modified: Sat, 16 Dec 2023 00:52:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76ed920e910d82447965f5c1f55efe5bb069af159fe23772d9c688b64be115`  
		Last Modified: Sat, 16 Dec 2023 00:52:33 GMT  
		Size: 129.6 MB (129562531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1e5b45feffe9aa474e2e16f123cd5129e69a69245c24d51ffb2706e25131a3`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb4abbe78619511c97edfd8c05a351ded6df0f6764674db5d0d99e5012566de`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8c260c8c6fb419f092f52c57457e6bee54a428e14114955b0ee14906059134`  
		Last Modified: Sat, 16 Dec 2023 00:52:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-bullseye` - unknown; unknown

```console
$ docker pull mysql@sha256:506434d0f05be405f0ae304078aea321176a73146c1ca6e2f1291264a3205747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffae5bcb9a98272dee4569d90f895bb91c0c313739ecc60f96a5e6ef22d5ab62`

```dockerfile
```

-	Layers:
	-	`sha256:82ca863aced305acc9c7efb65b0ae5ce36432aab7c270ed94849cc193e5c2d9c`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 3.6 MB (3552993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae41c906f9a76411585e2785f349f1e57a5afc61a11ebf6e13c341872370466b`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35-debian`

```console
$ docker pull mysql@sha256:033a00e6355f3348487933cd9572984d4574b8cac59a71434a4a4b74504d4282
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.35-debian` - linux; amd64

```console
$ docker pull mysql@sha256:bda410b1ba9fa28233d34669438e1ee3cd40d08efe7db27a754fc6ef30834cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179126201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c5e28586043f1155dcf5769a62ce3fbc0031a0a3d90eb64d465120cb56ce0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 21:28:23 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENV GOSU_VERSION=1.16
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 Dec 2023 21:28:23 GMT
ENV MYSQL_VERSION=8.0.35-1debian11
# Fri, 15 Dec 2023 21:28:23 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 Dec 2023 21:28:23 GMT
COPY config/ /etc/mysql/ # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 15 Dec 2023 21:28:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Dec 2023 21:28:23 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 15 Dec 2023 21:28:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b01c838fc79b37e322ae5a16f84a6ccc27ca133bee2874090751536789ef073`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8500e12244dd81352ba29546b575a15e83614aa7d752b6fd4f3a367e57c17e`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 4.2 MB (4207540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae228aa190a86352dce1c5573ae6e257a0e5af720c7012fe220e59b09504308`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 1.5 MB (1472510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fcd497cdbd53c1e265f6ff528cdd3a53c74500fe4404f197f4364ceed88c20`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65598fbce0667e0315c4481d43dd19851f4668c09f985ff32d13f2050f38c4df`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 12.5 MB (12454934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1e8cdfe04bbe14fd7099571a0cb611c1c63dfa2989da39eb7a75b8e9df5b08`  
		Last Modified: Sat, 16 Dec 2023 00:52:30 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acc0935e72ada43cb191dea71e8be359acc5ad5f5040056e973068fd48cf52a`  
		Last Modified: Sat, 16 Dec 2023 00:52:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76ed920e910d82447965f5c1f55efe5bb069af159fe23772d9c688b64be115`  
		Last Modified: Sat, 16 Dec 2023 00:52:33 GMT  
		Size: 129.6 MB (129562531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1e5b45feffe9aa474e2e16f123cd5129e69a69245c24d51ffb2706e25131a3`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb4abbe78619511c97edfd8c05a351ded6df0f6764674db5d0d99e5012566de`  
		Last Modified: Sat, 16 Dec 2023 00:52:31 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8c260c8c6fb419f092f52c57457e6bee54a428e14114955b0ee14906059134`  
		Last Modified: Sat, 16 Dec 2023 00:52:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:506434d0f05be405f0ae304078aea321176a73146c1ca6e2f1291264a3205747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffae5bcb9a98272dee4569d90f895bb91c0c313739ecc60f96a5e6ef22d5ab62`

```dockerfile
```

-	Layers:
	-	`sha256:82ca863aced305acc9c7efb65b0ae5ce36432aab7c270ed94849cc193e5c2d9c`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 3.6 MB (3552993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae41c906f9a76411585e2785f349f1e57a5afc61a11ebf6e13c341872370466b`  
		Last Modified: Sat, 16 Dec 2023 00:52:29 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35-oracle`

```console
$ docker pull mysql@sha256:e8aded859189ea25dfc4371c7079941be835eb91a54334dd3fa82a9259c26dab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.35-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:124709177dfe53732029653081cf52378215bd8e3f10f14e94d490969f680b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173759219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300df64d4be784f8992d62b87a2a3f32f28ffa54fd4448f720e8e55ef33270f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e33690e46ba8482569a79e2bf66c8c7a53cbc22f7bebea8cc5bca7e9051f65`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 4.6 MB (4606817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ea003555d1dd0c7a9a5ceaa18bd7208d17f375fe8412b2c9a83451cda6782`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79abd900d0600d9d60fbb972222bd116a7882155ea82c8e8efa97edf023d3fb`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d721b014e95566c0fc5ce36065d6a8b11eed348ab158fbcc9ac4b585e8650c`  
		Last Modified: Thu, 14 Dec 2023 18:52:22 GMT  
		Size: 58.5 MB (58514574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba9f26e807f4e3dcd030bdcf103f5d5079de6f86d66406e91cfbe8e9fc56c02`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7be8506e77574efc8fc9fa164fa7d87e16506aefe111afff11aefe5ef9502c3`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 58.3 MB (58325400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef9735ba310beee320a5fec6fe2f305feae49cfaf30b88db33097efc3a53638`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768daf85511c86ca05c1f6238566fbce6f83fcc8274a39dca20bc30c448d3131`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9129d84df03f3c36711914ec48d54695fa051279e48f785a6ea0d4fb9f32eeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350f69bfd3fc16abdaad5604ede6ff6751376b89cdfa23975d22ffad66aba41a`

```dockerfile
```

-	Layers:
	-	`sha256:88fbb3798072a16d864f697c5d90fe255e121b9f271cfefaa7f2c9a24283b377`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 11.6 MB (11567393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd56e84fd5575b533c7fb113319b86551f2a9379cd98bf1039e8fcff82c9f6c`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 33.9 KB (33910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.35-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8ee2fe7eaf935ed89b47d6010f6df90259b3609d8df5d87d232a6bc36f0bc075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f81235988528166fd0ad151cf78258b4ecf4565383c9e95ee6557470dde3ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2d4a8cba602b5e3cd65d5e0557988bcbd78b091afb3f6ae0d15864790987f`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba09d9fb3dfd35ff7ebbb6eb20bd59a35b737aec5e0e2f2c42eb50dda9d1e1`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 57.6 MB (57573677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3039dd1391bc16761b31a730472044ed80f3817b431f9de14e0b2b9e5949a66e`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4d0901f4a72dd35f6f7f609dbcc9e9d4cc321ed55cad8b778a73cd0e8b4132`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 64.6 MB (64575659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ffadc976d782ad9beaafd96646c04a37a91ab42bec7c3340d312ebe6d30bfe`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce24b8ac6b4928227fc12ef8569db0eb81194b07b97b2b25a7ac3f59ffaf9232`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:93dd96ed5c4dfaad500931c8bd5fef986d4713062b42d2c18bbf132b9ef88922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11599722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa4b66addb7ddb598bbf216c63487583739eb6b75a905df678be0462f6852c1`

```dockerfile
```

-	Layers:
	-	`sha256:fa10120f60379e910b2c802d1f14daf9abc49c54d75d693ff079cc9df930f814`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 11.6 MB (11565969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd9a910678b2ec061d21467e0bfad540d513b009275b0c7d4805f0ee1b19b16d`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 33.8 KB (33753 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.35-oraclelinux8`

```console
$ docker pull mysql@sha256:e8aded859189ea25dfc4371c7079941be835eb91a54334dd3fa82a9259c26dab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.35-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:124709177dfe53732029653081cf52378215bd8e3f10f14e94d490969f680b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173759219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300df64d4be784f8992d62b87a2a3f32f28ffa54fd4448f720e8e55ef33270f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e33690e46ba8482569a79e2bf66c8c7a53cbc22f7bebea8cc5bca7e9051f65`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 4.6 MB (4606817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ea003555d1dd0c7a9a5ceaa18bd7208d17f375fe8412b2c9a83451cda6782`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79abd900d0600d9d60fbb972222bd116a7882155ea82c8e8efa97edf023d3fb`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d721b014e95566c0fc5ce36065d6a8b11eed348ab158fbcc9ac4b585e8650c`  
		Last Modified: Thu, 14 Dec 2023 18:52:22 GMT  
		Size: 58.5 MB (58514574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba9f26e807f4e3dcd030bdcf103f5d5079de6f86d66406e91cfbe8e9fc56c02`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7be8506e77574efc8fc9fa164fa7d87e16506aefe111afff11aefe5ef9502c3`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 58.3 MB (58325400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef9735ba310beee320a5fec6fe2f305feae49cfaf30b88db33097efc3a53638`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768daf85511c86ca05c1f6238566fbce6f83fcc8274a39dca20bc30c448d3131`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:9129d84df03f3c36711914ec48d54695fa051279e48f785a6ea0d4fb9f32eeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11601303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350f69bfd3fc16abdaad5604ede6ff6751376b89cdfa23975d22ffad66aba41a`

```dockerfile
```

-	Layers:
	-	`sha256:88fbb3798072a16d864f697c5d90fe255e121b9f271cfefaa7f2c9a24283b377`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 11.6 MB (11567393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd56e84fd5575b533c7fb113319b86551f2a9379cd98bf1039e8fcff82c9f6c`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 33.9 KB (33910 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.35-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8ee2fe7eaf935ed89b47d6010f6df90259b3609d8df5d87d232a6bc36f0bc075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177445288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f81235988528166fd0ad151cf78258b4ecf4565383c9e95ee6557470dde3ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2d4a8cba602b5e3cd65d5e0557988bcbd78b091afb3f6ae0d15864790987f`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba09d9fb3dfd35ff7ebbb6eb20bd59a35b737aec5e0e2f2c42eb50dda9d1e1`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 57.6 MB (57573677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3039dd1391bc16761b31a730472044ed80f3817b431f9de14e0b2b9e5949a66e`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4d0901f4a72dd35f6f7f609dbcc9e9d4cc321ed55cad8b778a73cd0e8b4132`  
		Last Modified: Thu, 14 Dec 2023 20:16:56 GMT  
		Size: 64.6 MB (64575659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ffadc976d782ad9beaafd96646c04a37a91ab42bec7c3340d312ebe6d30bfe`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 5.4 KB (5384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce24b8ac6b4928227fc12ef8569db0eb81194b07b97b2b25a7ac3f59ffaf9232`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.35-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:93dd96ed5c4dfaad500931c8bd5fef986d4713062b42d2c18bbf132b9ef88922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11599722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa4b66addb7ddb598bbf216c63487583739eb6b75a905df678be0462f6852c1`

```dockerfile
```

-	Layers:
	-	`sha256:fa10120f60379e910b2c802d1f14daf9abc49c54d75d693ff079cc9df930f814`  
		Last Modified: Thu, 14 Dec 2023 20:16:55 GMT  
		Size: 11.6 MB (11565969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd9a910678b2ec061d21467e0bfad540d513b009275b0c7d4805f0ee1b19b16d`  
		Last Modified: Thu, 14 Dec 2023 20:16:54 GMT  
		Size: 33.8 KB (33753 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2-oracle`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2-oraclelinux8`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2.0`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2.0` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2.0-oracle`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.2.0-oraclelinux8`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.2.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.2.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.2.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux8`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux8`

```console
$ docker pull mysql@sha256:ceb98918916bd5261b3e9866ac8271d75d276b8a4db56f1dc190770342a77a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:e528b69c8a8bc92868b995881c9d1ef91d10020ed73b3c25bc6f73017df928d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181604379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f0456d1c1a96b92db74cef42e955e69982e1489937e53b060ef30d4ef9896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6055edb33b7367ea875ee0e3bcd184220a633c615238176892266857d4380`  
		Last Modified: Thu, 14 Dec 2023 18:52:18 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646ab461d8bc00e32894b6ade7648cde75ee4e20d0b4ce4823ee62233fe32d6`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012006c6a591f2e524d580140da5f9947abdf1fe12151210747a2f98b140981f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 4.6 MB (4606811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d5fa34b95d8dbdda0ef2cddd0ceb4b6c142580b17518edfcb34449bc328fa`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0243877faf394bc8507e1aabd7bba793e0732adb4207eefba3648dfe4afb8`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b459cd2f5a2d75fde5db59a84fc0620b64ef15d4656b50a9f0d5e4b92599`  
		Last Modified: Thu, 14 Dec 2023 18:52:23 GMT  
		Size: 62.6 MB (62585301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dceaed53baf8d8056f27e99315c65f841c72b767ac001168e6ea315afbb5fcf`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b834ea1cdcf292186edbc0e5a15ade8ef96e674a4843c31bd1ffea92472ab`  
		Last Modified: Thu, 14 Dec 2023 18:52:24 GMT  
		Size: 62.1 MB (62099950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df78c25b2278d01b98ceaedf0340cfddd0219bac0eef850583595b9809a9765`  
		Last Modified: Thu, 14 Dec 2023 18:52:21 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:043600b559d350271ffb7434f6e847dd7d9603e3a5a2906c37423b850b9276d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75579766d6398b05df6ac1b50e10ea99e1e1dd37b851131163c8b19987e69232`

```dockerfile
```

-	Layers:
	-	`sha256:86702c762adb9cb5578dd80015a75928e4f84e0fd1f3445f95e05702e55ae15f`  
		Last Modified: Thu, 14 Dec 2023 18:52:20 GMT  
		Size: 11.6 MB (11571508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619d430dd2ff812d558fa834e8040376d50cd7c3b28ea70ed08495ea7526b6c7`  
		Last Modified: Thu, 14 Dec 2023 18:52:19 GMT  
		Size: 33.3 KB (33321 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:60c18e162f94d30142402e64f78e4817bb12a0695238fb06b35107a80a2ac080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185276124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1402b5eee239d06c8f1a01c16cd0b773e85e808e5c9185a6b36e9b232e776275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_VERSION=8.2.0-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENV MYSQL_SHELL_VERSION=8.2.1-1.el8
# Tue, 12 Dec 2023 19:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Dec 2023 19:11:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 19:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 19:11:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 Dec 2023 19:11:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c686b91aca61da8058a44e9f6aa06cbb27aa65cf2db0768377bcc6899dc0c2`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39062282e36f6169d219352cb19810ac7506e408e89b4ef33c400903a6ecc1`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73452dd561ff872804f5a63faab7552647c80c8a399e834fe154707a48613b20`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 4.3 MB (4300794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba54e261f50c32496de78ff38c42eb03cb97850ddbeb3c96f4fe34ea1cb23bc`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c0fd6cce4772b17fe2500d6ce97e3a35076112226cc23269afa1542f7b51d`  
		Last Modified: Thu, 14 Dec 2023 20:15:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaffd91cbb1278d374c5b91f8a3e87239e73b0113a1fa5835faf13bcb05948dc`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 61.6 MB (61602995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec60922d8e9eefbce5167faf6f2296ddec22dcafc9a84f5db6f94e92e032089`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942dbd5bb0a98d45556f650aa3174e3e4a5fcf822e5e7a67529ae622bb02b14a`  
		Last Modified: Thu, 14 Dec 2023 20:15:09 GMT  
		Size: 68.4 MB (68377279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2f0c1cf4862f32a2b059096a2ce24dcd67dc9c8990ed79e0cc9400629298a`  
		Last Modified: Thu, 14 Dec 2023 20:15:07 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:c98f729aaaf45c1bd27de95baa1548e137b2f7bed0fd54d4d3c6194dd81b8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11603439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84502ed27d7ab974d0375cbf1a37a7774e64d8ed985d7fb7c4cd6dc4db6761e`

```dockerfile
```

-	Layers:
	-	`sha256:3a1ac52e1cef0e5254b4b06bffc3c8b9db2d3eaef00f14f4bc3468fb58943047`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 11.6 MB (11570096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667252c2b8bab629219c4a08e4af26e643ea265631335d200b0b4eb347c99175`  
		Last Modified: Thu, 14 Dec 2023 20:15:05 GMT  
		Size: 33.3 KB (33343 bytes)  
		MIME: application/vnd.in-toto+json
