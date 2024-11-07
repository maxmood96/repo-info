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
-	[`mysql:8.0.40`](#mysql8040)
-	[`mysql:8.0.40-bookworm`](#mysql8040-bookworm)
-	[`mysql:8.0.40-debian`](#mysql8040-debian)
-	[`mysql:8.0.40-oracle`](#mysql8040-oracle)
-	[`mysql:8.0.40-oraclelinux9`](#mysql8040-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.3`](#mysql843)
-	[`mysql:8.4.3-oracle`](#mysql843-oracle)
-	[`mysql:8.4.3-oraclelinux9`](#mysql843-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.1`](#mysql91)
-	[`mysql:9.1-oracle`](#mysql91-oracle)
-	[`mysql:9.1-oraclelinux9`](#mysql91-oraclelinux9)
-	[`mysql:9.1.0`](#mysql910)
-	[`mysql:9.1.0-oracle`](#mysql910-oracle)
-	[`mysql:9.1.0-oraclelinux9`](#mysql910-oraclelinux9)
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
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:f3a00e618edc1f7ea047d86527b3f3c4654b5e9e3d10d59e879f84a6c6cb110c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:df0757d9bccdc23e6aefd784ac96903b8f4adf8b4b8ad77a6261435f64e9e0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170545091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4b39935f208286727fa100cc733bc2681da4df62d5354fc360a29a0f26d85a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7354d28ef157443d1e66e12099f882609bc688851e6408721caad44f8502f884`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7478c7c1cef6f2fac1a94602ee8f3da82c837046ff59373a7e4b0ff7c80792d4`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2c12e6ea0ce001ca93471951ca8dcc0495298302278d73494e484b8e2bc98a`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 6.7 MB (6738241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f9f9dbb9a785db7e4c991aa8a9be7748175670a26fec8149a5bf4cc395873`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6ec9901d5a7d6cb2b0128a7e57e88b0f6bea89ab38dde9c18579c1af3c16cd`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 49.6 MB (49594613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd808bff6af22e0e64530d2b3abc32eb78bd8295d185b85df18876e825afa34`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397a7aefe9e4dcf1ebfaa749a6beffa0cf59a2bf27ffaae8d4a1ce00dbbd7fde`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 64.0 MB (64001589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2300358455cf76e69f66ef31dae56b5e160d5690405ceada69f06d876550c2fb`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300abd503ad1c22215580e076391ab7d5c46383f27914ed1af277ce52f712909`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:ca31e4f6a3ddc374cc289c760f4ae089e4455f624f93e5022e4942008217e6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e7d3871c186cb2431f5bb9c3decfa5a96aba3f2adc60a7fdd787af0b1d2ca3`

```dockerfile
```

-	Layers:
	-	`sha256:eb7e2205b6f99d2ff6d6d48ff4e8b355eff5547c80270491a507850d517890b8`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 14.7 MB (14749237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ee9d5d40c1d9b67dcf303e854953c9895e888daff2464cfb6a1c0cad4097fa`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:fd8e39c02230421a5ebff8154c31be78acaba6fc4692c8227bcdcc8374d0f7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175113066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c77f0f5954315c86ee82a02ae9dce316062bef810f0d4b30e8dca5a26c2a2a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccb4fbac12748ba7203bc1ad266e78f707250ed92c2358e1bce83b0e3a3030a`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac9411b2f7baca26a5b47dd55a901e4353f58ae981f42dbbf850d8e4c9c66f`  
		Last Modified: Wed, 06 Nov 2024 20:55:32 GMT  
		Size: 48.5 MB (48457495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b19b98e136403fc82a6ab22146666507fa09169be5639cf03ac516ab45af8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b744ce874ce6daa8b31d3782f2b35026e6b9181b6217b44e1db81dab3f83696`  
		Last Modified: Wed, 06 Nov 2024 20:55:33 GMT  
		Size: 71.5 MB (71514041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5f8bfef83403a0086d9bc9ce0dd873d0502c2ead882ada635a3252c72a0563`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd3a178e40bdf54a9c7412184a386176e391c4925b478e4f1a30a8ec6d9dc1e`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8400f1e807842d38d88c228b06a2f0d0344417270ffcc9228ee8532ee5db9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f7784ba52101501cec8017ceed1fab564a54d98324ccf709e9ccf874c7ac2a`

```dockerfile
```

-	Layers:
	-	`sha256:efd841bff3c6a93cb222bb497f575766fc1e2b393953d61a7c297521f99a8760`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 14.7 MB (14744315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae0d990eda5903edcc1a638027337372e2bdb71ef479a035d09a4e8bab0ced8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:49b84fc5916192e766f6879127d4d871e7101e73bd15ca63df4c1d5ba6d08946
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:3e02ef51dfc79b03db86b7c0062d3bad3fd9f0387e2fa840842e7ef9d88d8e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184176649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1a2fa05087a2bce3781e5a57e32d535725a128a9aaf69b011d956b6face15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1debian12
# Mon, 14 Oct 2024 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2811da9b019eed58703a8ada1caa82533276039c52ab3a74636da84859bb40`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2baf8dba5bbe9c68e00b53d352e48e4318bcc4a3c0ea7fe20dec9e8e87ff76d`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.4 MB (4422704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614d15f9c06d6e6a1a248d99e306b85add43031f83f974b2c2022d053e71d9c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.4 MB (1445878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b0c5e04163f0547e7229170628d079ee2f838019b64fefc9340f72fe61981`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f22d133288ad4b83b330050601bd2eb187e6768ea330fc18eb963a1304fa8d`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 15.3 MB (15294765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620060781f1e82b4ac6bad00e2e313caaab1042776b930c56738c1a226f76e67`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69095101e4f64ba06332cc8edb2fff22d36813c27f809a8bd66d4825cf3a8316`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47961d443cea8428d3cd3f6ccbf24fd7a9e48b723b8618f8f18f6206623dc2a6`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 133.9 MB (133876747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15871d93458f7e05360fc45c0b2a69b059a68f66b3cbc5aeca7e17d7707fa3ee`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82da9494c1cfa82f7466d409529f09d1c38c9e30724b1afce7f1d6060a10f88f`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ceddd40e6b584c3483837f8f5963dfefe3a13ee11afc33b4bb749f8ab92ae5`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca39339c819cf8ea1fdb2d6531b8993ebfa93cf849801e2cf0f3737571ccefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9790f7c41dfb8ef68d613e084aa436d073d249302dc3722d4b519ee8eca4fff`

```dockerfile
```

-	Layers:
	-	`sha256:cfc62b48f0159d49308ec5353528a4853d89d4807bdf056f3148e66ffc9fe38c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.0 MB (3981572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3239c31101b2d7721588207b13bda72001e4f00ffd0cdac796931dacca981f98`  
		Last Modified: Thu, 17 Oct 2024 01:31:08 GMT  
		Size: 34.2 KB (34176 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:49b84fc5916192e766f6879127d4d871e7101e73bd15ca63df4c1d5ba6d08946
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3e02ef51dfc79b03db86b7c0062d3bad3fd9f0387e2fa840842e7ef9d88d8e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184176649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1a2fa05087a2bce3781e5a57e32d535725a128a9aaf69b011d956b6face15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1debian12
# Mon, 14 Oct 2024 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2811da9b019eed58703a8ada1caa82533276039c52ab3a74636da84859bb40`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2baf8dba5bbe9c68e00b53d352e48e4318bcc4a3c0ea7fe20dec9e8e87ff76d`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.4 MB (4422704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614d15f9c06d6e6a1a248d99e306b85add43031f83f974b2c2022d053e71d9c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.4 MB (1445878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b0c5e04163f0547e7229170628d079ee2f838019b64fefc9340f72fe61981`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f22d133288ad4b83b330050601bd2eb187e6768ea330fc18eb963a1304fa8d`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 15.3 MB (15294765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620060781f1e82b4ac6bad00e2e313caaab1042776b930c56738c1a226f76e67`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69095101e4f64ba06332cc8edb2fff22d36813c27f809a8bd66d4825cf3a8316`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47961d443cea8428d3cd3f6ccbf24fd7a9e48b723b8618f8f18f6206623dc2a6`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 133.9 MB (133876747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15871d93458f7e05360fc45c0b2a69b059a68f66b3cbc5aeca7e17d7707fa3ee`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82da9494c1cfa82f7466d409529f09d1c38c9e30724b1afce7f1d6060a10f88f`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ceddd40e6b584c3483837f8f5963dfefe3a13ee11afc33b4bb749f8ab92ae5`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca39339c819cf8ea1fdb2d6531b8993ebfa93cf849801e2cf0f3737571ccefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9790f7c41dfb8ef68d613e084aa436d073d249302dc3722d4b519ee8eca4fff`

```dockerfile
```

-	Layers:
	-	`sha256:cfc62b48f0159d49308ec5353528a4853d89d4807bdf056f3148e66ffc9fe38c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.0 MB (3981572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3239c31101b2d7721588207b13bda72001e4f00ffd0cdac796931dacca981f98`  
		Last Modified: Thu, 17 Oct 2024 01:31:08 GMT  
		Size: 34.2 KB (34176 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:f3a00e618edc1f7ea047d86527b3f3c4654b5e9e3d10d59e879f84a6c6cb110c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:df0757d9bccdc23e6aefd784ac96903b8f4adf8b4b8ad77a6261435f64e9e0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170545091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4b39935f208286727fa100cc733bc2681da4df62d5354fc360a29a0f26d85a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7354d28ef157443d1e66e12099f882609bc688851e6408721caad44f8502f884`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7478c7c1cef6f2fac1a94602ee8f3da82c837046ff59373a7e4b0ff7c80792d4`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2c12e6ea0ce001ca93471951ca8dcc0495298302278d73494e484b8e2bc98a`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 6.7 MB (6738241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f9f9dbb9a785db7e4c991aa8a9be7748175670a26fec8149a5bf4cc395873`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6ec9901d5a7d6cb2b0128a7e57e88b0f6bea89ab38dde9c18579c1af3c16cd`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 49.6 MB (49594613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd808bff6af22e0e64530d2b3abc32eb78bd8295d185b85df18876e825afa34`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397a7aefe9e4dcf1ebfaa749a6beffa0cf59a2bf27ffaae8d4a1ce00dbbd7fde`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 64.0 MB (64001589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2300358455cf76e69f66ef31dae56b5e160d5690405ceada69f06d876550c2fb`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300abd503ad1c22215580e076391ab7d5c46383f27914ed1af277ce52f712909`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ca31e4f6a3ddc374cc289c760f4ae089e4455f624f93e5022e4942008217e6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e7d3871c186cb2431f5bb9c3decfa5a96aba3f2adc60a7fdd787af0b1d2ca3`

```dockerfile
```

-	Layers:
	-	`sha256:eb7e2205b6f99d2ff6d6d48ff4e8b355eff5547c80270491a507850d517890b8`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 14.7 MB (14749237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ee9d5d40c1d9b67dcf303e854953c9895e888daff2464cfb6a1c0cad4097fa`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:fd8e39c02230421a5ebff8154c31be78acaba6fc4692c8227bcdcc8374d0f7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175113066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c77f0f5954315c86ee82a02ae9dce316062bef810f0d4b30e8dca5a26c2a2a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccb4fbac12748ba7203bc1ad266e78f707250ed92c2358e1bce83b0e3a3030a`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac9411b2f7baca26a5b47dd55a901e4353f58ae981f42dbbf850d8e4c9c66f`  
		Last Modified: Wed, 06 Nov 2024 20:55:32 GMT  
		Size: 48.5 MB (48457495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b19b98e136403fc82a6ab22146666507fa09169be5639cf03ac516ab45af8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b744ce874ce6daa8b31d3782f2b35026e6b9181b6217b44e1db81dab3f83696`  
		Last Modified: Wed, 06 Nov 2024 20:55:33 GMT  
		Size: 71.5 MB (71514041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5f8bfef83403a0086d9bc9ce0dd873d0502c2ead882ada635a3252c72a0563`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd3a178e40bdf54a9c7412184a386176e391c4925b478e4f1a30a8ec6d9dc1e`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8400f1e807842d38d88c228b06a2f0d0344417270ffcc9228ee8532ee5db9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f7784ba52101501cec8017ceed1fab564a54d98324ccf709e9ccf874c7ac2a`

```dockerfile
```

-	Layers:
	-	`sha256:efd841bff3c6a93cb222bb497f575766fc1e2b393953d61a7c297521f99a8760`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 14.7 MB (14744315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae0d990eda5903edcc1a638027337372e2bdb71ef479a035d09a4e8bab0ced8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:f3a00e618edc1f7ea047d86527b3f3c4654b5e9e3d10d59e879f84a6c6cb110c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:df0757d9bccdc23e6aefd784ac96903b8f4adf8b4b8ad77a6261435f64e9e0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170545091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4b39935f208286727fa100cc733bc2681da4df62d5354fc360a29a0f26d85a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7354d28ef157443d1e66e12099f882609bc688851e6408721caad44f8502f884`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7478c7c1cef6f2fac1a94602ee8f3da82c837046ff59373a7e4b0ff7c80792d4`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2c12e6ea0ce001ca93471951ca8dcc0495298302278d73494e484b8e2bc98a`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 6.7 MB (6738241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f9f9dbb9a785db7e4c991aa8a9be7748175670a26fec8149a5bf4cc395873`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6ec9901d5a7d6cb2b0128a7e57e88b0f6bea89ab38dde9c18579c1af3c16cd`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 49.6 MB (49594613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd808bff6af22e0e64530d2b3abc32eb78bd8295d185b85df18876e825afa34`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397a7aefe9e4dcf1ebfaa749a6beffa0cf59a2bf27ffaae8d4a1ce00dbbd7fde`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 64.0 MB (64001589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2300358455cf76e69f66ef31dae56b5e160d5690405ceada69f06d876550c2fb`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300abd503ad1c22215580e076391ab7d5c46383f27914ed1af277ce52f712909`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ca31e4f6a3ddc374cc289c760f4ae089e4455f624f93e5022e4942008217e6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e7d3871c186cb2431f5bb9c3decfa5a96aba3f2adc60a7fdd787af0b1d2ca3`

```dockerfile
```

-	Layers:
	-	`sha256:eb7e2205b6f99d2ff6d6d48ff4e8b355eff5547c80270491a507850d517890b8`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 14.7 MB (14749237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ee9d5d40c1d9b67dcf303e854953c9895e888daff2464cfb6a1c0cad4097fa`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:fd8e39c02230421a5ebff8154c31be78acaba6fc4692c8227bcdcc8374d0f7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175113066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c77f0f5954315c86ee82a02ae9dce316062bef810f0d4b30e8dca5a26c2a2a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccb4fbac12748ba7203bc1ad266e78f707250ed92c2358e1bce83b0e3a3030a`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac9411b2f7baca26a5b47dd55a901e4353f58ae981f42dbbf850d8e4c9c66f`  
		Last Modified: Wed, 06 Nov 2024 20:55:32 GMT  
		Size: 48.5 MB (48457495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b19b98e136403fc82a6ab22146666507fa09169be5639cf03ac516ab45af8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b744ce874ce6daa8b31d3782f2b35026e6b9181b6217b44e1db81dab3f83696`  
		Last Modified: Wed, 06 Nov 2024 20:55:33 GMT  
		Size: 71.5 MB (71514041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5f8bfef83403a0086d9bc9ce0dd873d0502c2ead882ada635a3252c72a0563`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd3a178e40bdf54a9c7412184a386176e391c4925b478e4f1a30a8ec6d9dc1e`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8400f1e807842d38d88c228b06a2f0d0344417270ffcc9228ee8532ee5db9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f7784ba52101501cec8017ceed1fab564a54d98324ccf709e9ccf874c7ac2a`

```dockerfile
```

-	Layers:
	-	`sha256:efd841bff3c6a93cb222bb497f575766fc1e2b393953d61a7c297521f99a8760`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 14.7 MB (14744315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae0d990eda5903edcc1a638027337372e2bdb71ef479a035d09a4e8bab0ced8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40`

```console
$ docker pull mysql@sha256:f3a00e618edc1f7ea047d86527b3f3c4654b5e9e3d10d59e879f84a6c6cb110c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40` - linux; amd64

```console
$ docker pull mysql@sha256:df0757d9bccdc23e6aefd784ac96903b8f4adf8b4b8ad77a6261435f64e9e0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170545091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4b39935f208286727fa100cc733bc2681da4df62d5354fc360a29a0f26d85a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7354d28ef157443d1e66e12099f882609bc688851e6408721caad44f8502f884`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7478c7c1cef6f2fac1a94602ee8f3da82c837046ff59373a7e4b0ff7c80792d4`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2c12e6ea0ce001ca93471951ca8dcc0495298302278d73494e484b8e2bc98a`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 6.7 MB (6738241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f9f9dbb9a785db7e4c991aa8a9be7748175670a26fec8149a5bf4cc395873`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6ec9901d5a7d6cb2b0128a7e57e88b0f6bea89ab38dde9c18579c1af3c16cd`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 49.6 MB (49594613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd808bff6af22e0e64530d2b3abc32eb78bd8295d185b85df18876e825afa34`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397a7aefe9e4dcf1ebfaa749a6beffa0cf59a2bf27ffaae8d4a1ce00dbbd7fde`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 64.0 MB (64001589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2300358455cf76e69f66ef31dae56b5e160d5690405ceada69f06d876550c2fb`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300abd503ad1c22215580e076391ab7d5c46383f27914ed1af277ce52f712909`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40` - unknown; unknown

```console
$ docker pull mysql@sha256:ca31e4f6a3ddc374cc289c760f4ae089e4455f624f93e5022e4942008217e6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e7d3871c186cb2431f5bb9c3decfa5a96aba3f2adc60a7fdd787af0b1d2ca3`

```dockerfile
```

-	Layers:
	-	`sha256:eb7e2205b6f99d2ff6d6d48ff4e8b355eff5547c80270491a507850d517890b8`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 14.7 MB (14749237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ee9d5d40c1d9b67dcf303e854953c9895e888daff2464cfb6a1c0cad4097fa`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:fd8e39c02230421a5ebff8154c31be78acaba6fc4692c8227bcdcc8374d0f7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175113066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c77f0f5954315c86ee82a02ae9dce316062bef810f0d4b30e8dca5a26c2a2a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccb4fbac12748ba7203bc1ad266e78f707250ed92c2358e1bce83b0e3a3030a`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac9411b2f7baca26a5b47dd55a901e4353f58ae981f42dbbf850d8e4c9c66f`  
		Last Modified: Wed, 06 Nov 2024 20:55:32 GMT  
		Size: 48.5 MB (48457495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b19b98e136403fc82a6ab22146666507fa09169be5639cf03ac516ab45af8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b744ce874ce6daa8b31d3782f2b35026e6b9181b6217b44e1db81dab3f83696`  
		Last Modified: Wed, 06 Nov 2024 20:55:33 GMT  
		Size: 71.5 MB (71514041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5f8bfef83403a0086d9bc9ce0dd873d0502c2ead882ada635a3252c72a0563`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd3a178e40bdf54a9c7412184a386176e391c4925b478e4f1a30a8ec6d9dc1e`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8400f1e807842d38d88c228b06a2f0d0344417270ffcc9228ee8532ee5db9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f7784ba52101501cec8017ceed1fab564a54d98324ccf709e9ccf874c7ac2a`

```dockerfile
```

-	Layers:
	-	`sha256:efd841bff3c6a93cb222bb497f575766fc1e2b393953d61a7c297521f99a8760`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 14.7 MB (14744315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae0d990eda5903edcc1a638027337372e2bdb71ef479a035d09a4e8bab0ced8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-bookworm`

```console
$ docker pull mysql@sha256:49b84fc5916192e766f6879127d4d871e7101e73bd15ca63df4c1d5ba6d08946
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.40-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:3e02ef51dfc79b03db86b7c0062d3bad3fd9f0387e2fa840842e7ef9d88d8e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184176649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1a2fa05087a2bce3781e5a57e32d535725a128a9aaf69b011d956b6face15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1debian12
# Mon, 14 Oct 2024 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2811da9b019eed58703a8ada1caa82533276039c52ab3a74636da84859bb40`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2baf8dba5bbe9c68e00b53d352e48e4318bcc4a3c0ea7fe20dec9e8e87ff76d`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.4 MB (4422704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614d15f9c06d6e6a1a248d99e306b85add43031f83f974b2c2022d053e71d9c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.4 MB (1445878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b0c5e04163f0547e7229170628d079ee2f838019b64fefc9340f72fe61981`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f22d133288ad4b83b330050601bd2eb187e6768ea330fc18eb963a1304fa8d`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 15.3 MB (15294765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620060781f1e82b4ac6bad00e2e313caaab1042776b930c56738c1a226f76e67`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69095101e4f64ba06332cc8edb2fff22d36813c27f809a8bd66d4825cf3a8316`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47961d443cea8428d3cd3f6ccbf24fd7a9e48b723b8618f8f18f6206623dc2a6`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 133.9 MB (133876747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15871d93458f7e05360fc45c0b2a69b059a68f66b3cbc5aeca7e17d7707fa3ee`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82da9494c1cfa82f7466d409529f09d1c38c9e30724b1afce7f1d6060a10f88f`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ceddd40e6b584c3483837f8f5963dfefe3a13ee11afc33b4bb749f8ab92ae5`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca39339c819cf8ea1fdb2d6531b8993ebfa93cf849801e2cf0f3737571ccefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9790f7c41dfb8ef68d613e084aa436d073d249302dc3722d4b519ee8eca4fff`

```dockerfile
```

-	Layers:
	-	`sha256:cfc62b48f0159d49308ec5353528a4853d89d4807bdf056f3148e66ffc9fe38c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.0 MB (3981572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3239c31101b2d7721588207b13bda72001e4f00ffd0cdac796931dacca981f98`  
		Last Modified: Thu, 17 Oct 2024 01:31:08 GMT  
		Size: 34.2 KB (34176 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-debian`

```console
$ docker pull mysql@sha256:49b84fc5916192e766f6879127d4d871e7101e73bd15ca63df4c1d5ba6d08946
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.40-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3e02ef51dfc79b03db86b7c0062d3bad3fd9f0387e2fa840842e7ef9d88d8e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184176649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1a2fa05087a2bce3781e5a57e32d535725a128a9aaf69b011d956b6face15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1debian12
# Mon, 14 Oct 2024 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2811da9b019eed58703a8ada1caa82533276039c52ab3a74636da84859bb40`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2baf8dba5bbe9c68e00b53d352e48e4318bcc4a3c0ea7fe20dec9e8e87ff76d`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.4 MB (4422704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614d15f9c06d6e6a1a248d99e306b85add43031f83f974b2c2022d053e71d9c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.4 MB (1445878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b0c5e04163f0547e7229170628d079ee2f838019b64fefc9340f72fe61981`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f22d133288ad4b83b330050601bd2eb187e6768ea330fc18eb963a1304fa8d`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 15.3 MB (15294765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620060781f1e82b4ac6bad00e2e313caaab1042776b930c56738c1a226f76e67`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69095101e4f64ba06332cc8edb2fff22d36813c27f809a8bd66d4825cf3a8316`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47961d443cea8428d3cd3f6ccbf24fd7a9e48b723b8618f8f18f6206623dc2a6`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 133.9 MB (133876747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15871d93458f7e05360fc45c0b2a69b059a68f66b3cbc5aeca7e17d7707fa3ee`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82da9494c1cfa82f7466d409529f09d1c38c9e30724b1afce7f1d6060a10f88f`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ceddd40e6b584c3483837f8f5963dfefe3a13ee11afc33b4bb749f8ab92ae5`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca39339c819cf8ea1fdb2d6531b8993ebfa93cf849801e2cf0f3737571ccefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9790f7c41dfb8ef68d613e084aa436d073d249302dc3722d4b519ee8eca4fff`

```dockerfile
```

-	Layers:
	-	`sha256:cfc62b48f0159d49308ec5353528a4853d89d4807bdf056f3148e66ffc9fe38c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.0 MB (3981572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3239c31101b2d7721588207b13bda72001e4f00ffd0cdac796931dacca981f98`  
		Last Modified: Thu, 17 Oct 2024 01:31:08 GMT  
		Size: 34.2 KB (34176 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-oracle`

```console
$ docker pull mysql@sha256:f3a00e618edc1f7ea047d86527b3f3c4654b5e9e3d10d59e879f84a6c6cb110c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:df0757d9bccdc23e6aefd784ac96903b8f4adf8b4b8ad77a6261435f64e9e0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170545091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4b39935f208286727fa100cc733bc2681da4df62d5354fc360a29a0f26d85a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7354d28ef157443d1e66e12099f882609bc688851e6408721caad44f8502f884`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7478c7c1cef6f2fac1a94602ee8f3da82c837046ff59373a7e4b0ff7c80792d4`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2c12e6ea0ce001ca93471951ca8dcc0495298302278d73494e484b8e2bc98a`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 6.7 MB (6738241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f9f9dbb9a785db7e4c991aa8a9be7748175670a26fec8149a5bf4cc395873`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6ec9901d5a7d6cb2b0128a7e57e88b0f6bea89ab38dde9c18579c1af3c16cd`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 49.6 MB (49594613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd808bff6af22e0e64530d2b3abc32eb78bd8295d185b85df18876e825afa34`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397a7aefe9e4dcf1ebfaa749a6beffa0cf59a2bf27ffaae8d4a1ce00dbbd7fde`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 64.0 MB (64001589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2300358455cf76e69f66ef31dae56b5e160d5690405ceada69f06d876550c2fb`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300abd503ad1c22215580e076391ab7d5c46383f27914ed1af277ce52f712909`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ca31e4f6a3ddc374cc289c760f4ae089e4455f624f93e5022e4942008217e6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e7d3871c186cb2431f5bb9c3decfa5a96aba3f2adc60a7fdd787af0b1d2ca3`

```dockerfile
```

-	Layers:
	-	`sha256:eb7e2205b6f99d2ff6d6d48ff4e8b355eff5547c80270491a507850d517890b8`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 14.7 MB (14749237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ee9d5d40c1d9b67dcf303e854953c9895e888daff2464cfb6a1c0cad4097fa`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:fd8e39c02230421a5ebff8154c31be78acaba6fc4692c8227bcdcc8374d0f7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175113066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c77f0f5954315c86ee82a02ae9dce316062bef810f0d4b30e8dca5a26c2a2a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccb4fbac12748ba7203bc1ad266e78f707250ed92c2358e1bce83b0e3a3030a`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac9411b2f7baca26a5b47dd55a901e4353f58ae981f42dbbf850d8e4c9c66f`  
		Last Modified: Wed, 06 Nov 2024 20:55:32 GMT  
		Size: 48.5 MB (48457495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b19b98e136403fc82a6ab22146666507fa09169be5639cf03ac516ab45af8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b744ce874ce6daa8b31d3782f2b35026e6b9181b6217b44e1db81dab3f83696`  
		Last Modified: Wed, 06 Nov 2024 20:55:33 GMT  
		Size: 71.5 MB (71514041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5f8bfef83403a0086d9bc9ce0dd873d0502c2ead882ada635a3252c72a0563`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd3a178e40bdf54a9c7412184a386176e391c4925b478e4f1a30a8ec6d9dc1e`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8400f1e807842d38d88c228b06a2f0d0344417270ffcc9228ee8532ee5db9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f7784ba52101501cec8017ceed1fab564a54d98324ccf709e9ccf874c7ac2a`

```dockerfile
```

-	Layers:
	-	`sha256:efd841bff3c6a93cb222bb497f575766fc1e2b393953d61a7c297521f99a8760`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 14.7 MB (14744315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae0d990eda5903edcc1a638027337372e2bdb71ef479a035d09a4e8bab0ced8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-oraclelinux9`

```console
$ docker pull mysql@sha256:f3a00e618edc1f7ea047d86527b3f3c4654b5e9e3d10d59e879f84a6c6cb110c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:df0757d9bccdc23e6aefd784ac96903b8f4adf8b4b8ad77a6261435f64e9e0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170545091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4b39935f208286727fa100cc733bc2681da4df62d5354fc360a29a0f26d85a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7354d28ef157443d1e66e12099f882609bc688851e6408721caad44f8502f884`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7478c7c1cef6f2fac1a94602ee8f3da82c837046ff59373a7e4b0ff7c80792d4`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2c12e6ea0ce001ca93471951ca8dcc0495298302278d73494e484b8e2bc98a`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 6.7 MB (6738241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f9f9dbb9a785db7e4c991aa8a9be7748175670a26fec8149a5bf4cc395873`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6ec9901d5a7d6cb2b0128a7e57e88b0f6bea89ab38dde9c18579c1af3c16cd`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 49.6 MB (49594613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd808bff6af22e0e64530d2b3abc32eb78bd8295d185b85df18876e825afa34`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397a7aefe9e4dcf1ebfaa749a6beffa0cf59a2bf27ffaae8d4a1ce00dbbd7fde`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 64.0 MB (64001589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2300358455cf76e69f66ef31dae56b5e160d5690405ceada69f06d876550c2fb`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300abd503ad1c22215580e076391ab7d5c46383f27914ed1af277ce52f712909`  
		Last Modified: Wed, 06 Nov 2024 20:49:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ca31e4f6a3ddc374cc289c760f4ae089e4455f624f93e5022e4942008217e6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e7d3871c186cb2431f5bb9c3decfa5a96aba3f2adc60a7fdd787af0b1d2ca3`

```dockerfile
```

-	Layers:
	-	`sha256:eb7e2205b6f99d2ff6d6d48ff4e8b355eff5547c80270491a507850d517890b8`  
		Last Modified: Wed, 06 Nov 2024 20:49:42 GMT  
		Size: 14.7 MB (14749237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ee9d5d40c1d9b67dcf303e854953c9895e888daff2464cfb6a1c0cad4097fa`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 35.0 KB (34950 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:fd8e39c02230421a5ebff8154c31be78acaba6fc4692c8227bcdcc8374d0f7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175113066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c77f0f5954315c86ee82a02ae9dce316062bef810f0d4b30e8dca5a26c2a2a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccb4fbac12748ba7203bc1ad266e78f707250ed92c2358e1bce83b0e3a3030a`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac9411b2f7baca26a5b47dd55a901e4353f58ae981f42dbbf850d8e4c9c66f`  
		Last Modified: Wed, 06 Nov 2024 20:55:32 GMT  
		Size: 48.5 MB (48457495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b19b98e136403fc82a6ab22146666507fa09169be5639cf03ac516ab45af8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b744ce874ce6daa8b31d3782f2b35026e6b9181b6217b44e1db81dab3f83696`  
		Last Modified: Wed, 06 Nov 2024 20:55:33 GMT  
		Size: 71.5 MB (71514041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5f8bfef83403a0086d9bc9ce0dd873d0502c2ead882ada635a3252c72a0563`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd3a178e40bdf54a9c7412184a386176e391c4925b478e4f1a30a8ec6d9dc1e`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8400f1e807842d38d88c228b06a2f0d0344417270ffcc9228ee8532ee5db9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f7784ba52101501cec8017ceed1fab564a54d98324ccf709e9ccf874c7ac2a`

```dockerfile
```

-	Layers:
	-	`sha256:efd841bff3c6a93cb222bb497f575766fc1e2b393953d61a7c297521f99a8760`  
		Last Modified: Wed, 06 Nov 2024 20:55:31 GMT  
		Size: 14.7 MB (14744315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae0d990eda5903edcc1a638027337372e2bdb71ef479a035d09a4e8bab0ced8`  
		Last Modified: Wed, 06 Nov 2024 20:55:30 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3-oracle`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3-oraclelinux9`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1-oracle`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1-oraclelinux9`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0-oracle`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0-oraclelinux9`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:2be51594eba5983f47e67ff5cb87d666a223e309c6c64450f30b5c59a788ea40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:05de0996fde5a3a3b4a8246eb8da2e2b51ca5c2b1e41681a988f4f0a4a506a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173870782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db11fef9ce975df1539448189656f9e3251b7984130c7a86e1b348bf298a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98254a2b68893c63a65d33c4a3ecad873c80ca37f8319dc0b0306c9356f8b0a`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad83e89f9817c63b0465118e66f72acebd55254ba295402e3d6695a5a3132a7`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d733ea779fa8cf07d196b1d10e02c7b12fb5656cad0db75329a669e24a13d`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 6.7 MB (6738321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1af2601dda99f2b3bb2da2c4217c31f9deffc462a3abfa417f9ce1c922e6c`  
		Last Modified: Wed, 06 Nov 2024 20:49:41 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0233a63dc5cdfea554e4f07d7a71fe61498c23877e33d9200757eb52953c8cce`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31e56c9bea56d45ec5ffb9c2de54b78a28bcf6000d9e01c975e7e98b97393e`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 48.2 MB (48186095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fb96d14e5b76821556077a81691cc916f4fb4c18f541fdce36d7c1f0292c9d`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57074c6269467b4014824df11aa71a7f0f13f16645b559db1c5535c49d7f693`  
		Last Modified: Wed, 06 Nov 2024 20:49:46 GMT  
		Size: 68.7 MB (68735828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7030c241d9b8e06ce893cedb05ff4029f7d84b8e25800fe2651f3c4b4f928fdf`  
		Last Modified: Wed, 06 Nov 2024 20:49:45 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3403b5d1bce7819f6a25d3142f9f6571e01dbc050c33e56a60ea792f1093dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc22e6599496957fa223f059e34e0d0ebf0ea74cbe6f437de5b91a55ba3f68`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2521d3222bb7b905c440dfbdcd979ddcb23a8447f01157b5cb5dc9365e8ea`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 14.9 MB (14861217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c7cc1790fffc2c3b07950455ae6ca002a9b019852bab5d0a631bb56b185b3f1`  
		Last Modified: Wed, 06 Nov 2024 20:49:44 GMT  
		Size: 35.3 KB (35314 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c1da7abf8e0ac1554a6b53fb62a777ecf9e91c03600ed3707939d97274ad1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171154347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1158ce681432027078e6fc3667c83421acacf8a5fee527a66db3e9eaff7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ffc17bdaaff54c6babd4854bfe27fd9aa28af8dbae7ae2601662b09fac432c`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf02f366390676952ae452fbd6cc6a22546df65f8ee9cff14978040378bb161`  
		Last Modified: Wed, 06 Nov 2024 20:52:30 GMT  
		Size: 47.1 MB (47091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c54cc0690c3619e95567ccfe4335ab63dbadb08e9675f4ce580be32847050c`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec2e5ac145a38dc7a0c44023146d9b2585404993a6c5285f94273ccc4f6e7`  
		Last Modified: Wed, 06 Nov 2024 20:52:31 GMT  
		Size: 68.9 MB (68921688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bebfc92493ed3ea1c553a27f3fc836c2b04fa99697155e33b4a9da58535fb`  
		Last Modified: Wed, 06 Nov 2024 20:52:29 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5cb2ecc813b44ef8590444eb992d3857e150ad56c817e1c655145f08474a8d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a340366b300587374a6a6c0e55f18eaf59abaf915d6e4f9a362b1b6f02d84b6`

```dockerfile
```

-	Layers:
	-	`sha256:123208640d6c708fee827f8d814ee24d058d6a90226fe6e6db9c59529be56a90`  
		Last Modified: Wed, 06 Nov 2024 20:52:28 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75439167a59d4410f9bb94fea7ffa60112a2511db38371d3fe077be1530988d`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 35.7 KB (35657 bytes)  
		MIME: application/vnd.in-toto+json
