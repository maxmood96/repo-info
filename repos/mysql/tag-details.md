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
-	[`mysql:8.0.37`](#mysql8037)
-	[`mysql:8.0.37-bookworm`](#mysql8037-bookworm)
-	[`mysql:8.0.37-debian`](#mysql8037-debian)
-	[`mysql:8.0.37-oracle`](#mysql8037-oracle)
-	[`mysql:8.0.37-oraclelinux9`](#mysql8037-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.0`](#mysql840)
-	[`mysql:8.4.0-oracle`](#mysql840-oracle)
-	[`mysql:8.4.0-oraclelinux9`](#mysql840-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:8`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:7be6469428941fb76720439b8dd9b659520e4eb79e25e0f8516c3cc56c85a8ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:5ef3be4ea5cef8284a189c9d5c5e195bf9f964f9f79ee143d782b7206d113e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169059193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a39efdaa0e614fa654568e3db75c847ccf834872bb6dd19da932d83e01c1884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98f197fdb0f5ac8c3cb30ed8c40893c809ceb64d51a26dde2c25f73eaf807f`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8212d3737c98ba7ed1ed296973af035315a8697ec51911eb02774845d861cfd7`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977370f8b4972671c5e23b27fadfe1b29227a40069618ad7c7840beb30504d9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 9.8 MB (9755188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e12eae409d1c35ad2a3840eb83f63e9f4a84b703f23b7ac4694d07d0efa31e`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebe27f2f14a7ce430e2b64084ad94c523e55aef800ceea3482899e3f4936021`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c86eb65950b78873c308808c4e3bfe1d2cd69fe16d5f505486f7c23a14881c`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 49.2 MB (49162694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c587904a3fd2818bfb3ee56cf2c210650342deb8d56fec8b76cf64e46c6de9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49f7afeeee8c277d339480507cf466f95c3911ecb387ae52bbf11b390e15a42`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 60.2 MB (60183723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb1cf601a487c26fed88fc911f538a6e01bd02f396c5f3b621374c50c937823`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a590886c42d3cfc5073c45132805debf2cd499e9dec8fcef5b2035333df103f`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:d417eadf6ff1d7982e472d5316b03641cc1f2f972e2044804e31f0c84b9f64d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b5cd6fae9e52d0921f84c5d89aaaa9487ee011745c3932b6ee8a0cbf5c3e03`

```dockerfile
```

-	Layers:
	-	`sha256:ddf11d9aee61712bc300946c025344243fe71d58ffaf9d588ceed2b90aa03429`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 13.4 MB (13449033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b50899f8cb41d4e5c6c35cbd2ca3cb1afa119fcdfe3352c849026a16ed6a96`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 34.9 KB (34899 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f4360337f719defad09baa2b7903241df4fe10767bc3da7208cc9fb912b50e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176323852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8053e13c41910f7a256d1813b7f94389bb2037cdc6d5d4b1c227a4e964c587b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cbeb759403d76c018dc9047dadc7a00c9a6bdb78d7664004ecf487631fce98`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ceebeb4e87b339016212257a51b4182c29ec87324baf655e99d3514e2148b3`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 58.1 MB (58142450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70daaf3f7c42ba469d3b17a67f38fe65546ccd13c3d3b9e764773ef6564d4c75`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4c19f9b852bc18085d7a237f610b8d17e9ae3cf9df27dfcaedb17ad66989f`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 62.9 MB (62873495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c347df2d48aa6a0a13b204f922e3aa0d2a903a2141f7fec56e238827618f83c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8903dbcded2d02243b239de4f8e5856b1408a76d92a85ea8da3eadb51665215c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f1be1d3c82c2db05575f68e30fa53a8013b4b7c5b8e89c755c34895dcc8bcbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5bd00c9bd1aec121e35b9fec92b8a58853f6285580685787191df7fefdd80c`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0b935e4f2c33fbf4a4605b9a99a5e7e4a9926dd4c7745cc672cda56ae80e2`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 14.7 MB (14664719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eff94985dd0ee34d72bc4ce77345aad13b06e0555aea06a2238c9b1154b6d7`  
		Last Modified: Wed, 01 May 2024 00:30:58 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:23e2890afb54aa00ea7ff4f4f657fc5a853e37d7d9a85d9d1ed8b1dbee7694e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:3d02aa81c903a42cebc6e6bb407e1694ab1818bda55bf15b61a2742624fb8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bfd90cb949d20f852d49d5ad85491c93c1b9b91d45fe208e380321720f5899`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bde18031fe909f543254cc2e733160f72a752205a2949c6b40a4fb93b5019`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f5b132130169e78e654966bd3298ae5547afe735d026b6c503f9cd781578b3`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.4 MB (4422801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55afbcd0ee95b43da7f32cf64b89260ace0979ea80882f734ffa5d0c3b59312`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.4 MB (1449199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143e159e9ba53f9ab249e4dd23b8146c96256ec7429fd67b703970048d25410`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9824c3f585b77f8a653ef04d6f855bd4f083fc9c13ff653d2b1af5e3016162`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 15.3 MB (15281632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d8aed07a3abd808a32a1c8f93bb986712dcc84c94ce5595119523ccaad776`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668217c0d32afdc03ae00ca9b951002c2712c6294d9428c48b34c1806db544b`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1222274583182e0fc12661ac9ce631dc065e4cc10dcda00a146d33f1fabe87`  
		Last Modified: Tue, 30 Apr 2024 23:50:29 GMT  
		Size: 134.4 MB (134409341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93646b643b58c7717ff573c97f8732ea09bd6d616bf98ce13d1fe87e96531f`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7470a28f457e6deac3f34c84d6c8dbe20300497a2245d679d7dced2b8b7ad8`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34841c68669377f766eee6f5b9fe388c30796c6ec46e96452fc5ad2d2ce592`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:d1ab433d5294c0fd73d3b0dbd930072a2b008063272b1535d23e5b2aac7f8825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a86630f43c05e4d6049f3171246f462c68e29f488209ee07adf1d9301375a6`

```dockerfile
```

-	Layers:
	-	`sha256:c80288de35aea4344988f230740a6e5e3d3d3d7c957084b23bd95c884ce4d68c`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ca3c8ebbcb5ff586f0a9c49e88b165735b31fed5b7bfeace4df33efb746cb2`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:23e2890afb54aa00ea7ff4f4f657fc5a853e37d7d9a85d9d1ed8b1dbee7694e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3d02aa81c903a42cebc6e6bb407e1694ab1818bda55bf15b61a2742624fb8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bfd90cb949d20f852d49d5ad85491c93c1b9b91d45fe208e380321720f5899`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bde18031fe909f543254cc2e733160f72a752205a2949c6b40a4fb93b5019`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f5b132130169e78e654966bd3298ae5547afe735d026b6c503f9cd781578b3`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.4 MB (4422801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55afbcd0ee95b43da7f32cf64b89260ace0979ea80882f734ffa5d0c3b59312`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.4 MB (1449199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143e159e9ba53f9ab249e4dd23b8146c96256ec7429fd67b703970048d25410`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9824c3f585b77f8a653ef04d6f855bd4f083fc9c13ff653d2b1af5e3016162`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 15.3 MB (15281632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d8aed07a3abd808a32a1c8f93bb986712dcc84c94ce5595119523ccaad776`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668217c0d32afdc03ae00ca9b951002c2712c6294d9428c48b34c1806db544b`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1222274583182e0fc12661ac9ce631dc065e4cc10dcda00a146d33f1fabe87`  
		Last Modified: Tue, 30 Apr 2024 23:50:29 GMT  
		Size: 134.4 MB (134409341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93646b643b58c7717ff573c97f8732ea09bd6d616bf98ce13d1fe87e96531f`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7470a28f457e6deac3f34c84d6c8dbe20300497a2245d679d7dced2b8b7ad8`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34841c68669377f766eee6f5b9fe388c30796c6ec46e96452fc5ad2d2ce592`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:d1ab433d5294c0fd73d3b0dbd930072a2b008063272b1535d23e5b2aac7f8825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a86630f43c05e4d6049f3171246f462c68e29f488209ee07adf1d9301375a6`

```dockerfile
```

-	Layers:
	-	`sha256:c80288de35aea4344988f230740a6e5e3d3d3d7c957084b23bd95c884ce4d68c`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ca3c8ebbcb5ff586f0a9c49e88b165735b31fed5b7bfeace4df33efb746cb2`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:7be6469428941fb76720439b8dd9b659520e4eb79e25e0f8516c3cc56c85a8ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5ef3be4ea5cef8284a189c9d5c5e195bf9f964f9f79ee143d782b7206d113e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169059193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a39efdaa0e614fa654568e3db75c847ccf834872bb6dd19da932d83e01c1884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98f197fdb0f5ac8c3cb30ed8c40893c809ceb64d51a26dde2c25f73eaf807f`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8212d3737c98ba7ed1ed296973af035315a8697ec51911eb02774845d861cfd7`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977370f8b4972671c5e23b27fadfe1b29227a40069618ad7c7840beb30504d9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 9.8 MB (9755188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e12eae409d1c35ad2a3840eb83f63e9f4a84b703f23b7ac4694d07d0efa31e`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebe27f2f14a7ce430e2b64084ad94c523e55aef800ceea3482899e3f4936021`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c86eb65950b78873c308808c4e3bfe1d2cd69fe16d5f505486f7c23a14881c`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 49.2 MB (49162694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c587904a3fd2818bfb3ee56cf2c210650342deb8d56fec8b76cf64e46c6de9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49f7afeeee8c277d339480507cf466f95c3911ecb387ae52bbf11b390e15a42`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 60.2 MB (60183723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb1cf601a487c26fed88fc911f538a6e01bd02f396c5f3b621374c50c937823`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a590886c42d3cfc5073c45132805debf2cd499e9dec8fcef5b2035333df103f`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d417eadf6ff1d7982e472d5316b03641cc1f2f972e2044804e31f0c84b9f64d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b5cd6fae9e52d0921f84c5d89aaaa9487ee011745c3932b6ee8a0cbf5c3e03`

```dockerfile
```

-	Layers:
	-	`sha256:ddf11d9aee61712bc300946c025344243fe71d58ffaf9d588ceed2b90aa03429`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 13.4 MB (13449033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b50899f8cb41d4e5c6c35cbd2ca3cb1afa119fcdfe3352c849026a16ed6a96`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 34.9 KB (34899 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f4360337f719defad09baa2b7903241df4fe10767bc3da7208cc9fb912b50e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176323852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8053e13c41910f7a256d1813b7f94389bb2037cdc6d5d4b1c227a4e964c587b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cbeb759403d76c018dc9047dadc7a00c9a6bdb78d7664004ecf487631fce98`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ceebeb4e87b339016212257a51b4182c29ec87324baf655e99d3514e2148b3`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 58.1 MB (58142450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70daaf3f7c42ba469d3b17a67f38fe65546ccd13c3d3b9e764773ef6564d4c75`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4c19f9b852bc18085d7a237f610b8d17e9ae3cf9df27dfcaedb17ad66989f`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 62.9 MB (62873495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c347df2d48aa6a0a13b204f922e3aa0d2a903a2141f7fec56e238827618f83c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8903dbcded2d02243b239de4f8e5856b1408a76d92a85ea8da3eadb51665215c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f1be1d3c82c2db05575f68e30fa53a8013b4b7c5b8e89c755c34895dcc8bcbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5bd00c9bd1aec121e35b9fec92b8a58853f6285580685787191df7fefdd80c`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0b935e4f2c33fbf4a4605b9a99a5e7e4a9926dd4c7745cc672cda56ae80e2`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 14.7 MB (14664719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eff94985dd0ee34d72bc4ce77345aad13b06e0555aea06a2238c9b1154b6d7`  
		Last Modified: Wed, 01 May 2024 00:30:58 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:7bfc86b7256896e3f53e85b29159b18a9f3f53c4b96a1e99a7dc5939bf5e65f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5ef3be4ea5cef8284a189c9d5c5e195bf9f964f9f79ee143d782b7206d113e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169059193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a39efdaa0e614fa654568e3db75c847ccf834872bb6dd19da932d83e01c1884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98f197fdb0f5ac8c3cb30ed8c40893c809ceb64d51a26dde2c25f73eaf807f`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8212d3737c98ba7ed1ed296973af035315a8697ec51911eb02774845d861cfd7`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977370f8b4972671c5e23b27fadfe1b29227a40069618ad7c7840beb30504d9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 9.8 MB (9755188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e12eae409d1c35ad2a3840eb83f63e9f4a84b703f23b7ac4694d07d0efa31e`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebe27f2f14a7ce430e2b64084ad94c523e55aef800ceea3482899e3f4936021`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c86eb65950b78873c308808c4e3bfe1d2cd69fe16d5f505486f7c23a14881c`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 49.2 MB (49162694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c587904a3fd2818bfb3ee56cf2c210650342deb8d56fec8b76cf64e46c6de9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49f7afeeee8c277d339480507cf466f95c3911ecb387ae52bbf11b390e15a42`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 60.2 MB (60183723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb1cf601a487c26fed88fc911f538a6e01bd02f396c5f3b621374c50c937823`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a590886c42d3cfc5073c45132805debf2cd499e9dec8fcef5b2035333df103f`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d417eadf6ff1d7982e472d5316b03641cc1f2f972e2044804e31f0c84b9f64d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b5cd6fae9e52d0921f84c5d89aaaa9487ee011745c3932b6ee8a0cbf5c3e03`

```dockerfile
```

-	Layers:
	-	`sha256:ddf11d9aee61712bc300946c025344243fe71d58ffaf9d588ceed2b90aa03429`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 13.4 MB (13449033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b50899f8cb41d4e5c6c35cbd2ca3cb1afa119fcdfe3352c849026a16ed6a96`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 34.9 KB (34899 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37`

```console
$ docker pull mysql@sha256:7be6469428941fb76720439b8dd9b659520e4eb79e25e0f8516c3cc56c85a8ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.37` - linux; amd64

```console
$ docker pull mysql@sha256:5ef3be4ea5cef8284a189c9d5c5e195bf9f964f9f79ee143d782b7206d113e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169059193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a39efdaa0e614fa654568e3db75c847ccf834872bb6dd19da932d83e01c1884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98f197fdb0f5ac8c3cb30ed8c40893c809ceb64d51a26dde2c25f73eaf807f`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8212d3737c98ba7ed1ed296973af035315a8697ec51911eb02774845d861cfd7`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977370f8b4972671c5e23b27fadfe1b29227a40069618ad7c7840beb30504d9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 9.8 MB (9755188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e12eae409d1c35ad2a3840eb83f63e9f4a84b703f23b7ac4694d07d0efa31e`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebe27f2f14a7ce430e2b64084ad94c523e55aef800ceea3482899e3f4936021`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c86eb65950b78873c308808c4e3bfe1d2cd69fe16d5f505486f7c23a14881c`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 49.2 MB (49162694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c587904a3fd2818bfb3ee56cf2c210650342deb8d56fec8b76cf64e46c6de9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49f7afeeee8c277d339480507cf466f95c3911ecb387ae52bbf11b390e15a42`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 60.2 MB (60183723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb1cf601a487c26fed88fc911f538a6e01bd02f396c5f3b621374c50c937823`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a590886c42d3cfc5073c45132805debf2cd499e9dec8fcef5b2035333df103f`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37` - unknown; unknown

```console
$ docker pull mysql@sha256:d417eadf6ff1d7982e472d5316b03641cc1f2f972e2044804e31f0c84b9f64d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b5cd6fae9e52d0921f84c5d89aaaa9487ee011745c3932b6ee8a0cbf5c3e03`

```dockerfile
```

-	Layers:
	-	`sha256:ddf11d9aee61712bc300946c025344243fe71d58ffaf9d588ceed2b90aa03429`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 13.4 MB (13449033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b50899f8cb41d4e5c6c35cbd2ca3cb1afa119fcdfe3352c849026a16ed6a96`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 34.9 KB (34899 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.37` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f4360337f719defad09baa2b7903241df4fe10767bc3da7208cc9fb912b50e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176323852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8053e13c41910f7a256d1813b7f94389bb2037cdc6d5d4b1c227a4e964c587b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cbeb759403d76c018dc9047dadc7a00c9a6bdb78d7664004ecf487631fce98`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ceebeb4e87b339016212257a51b4182c29ec87324baf655e99d3514e2148b3`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 58.1 MB (58142450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70daaf3f7c42ba469d3b17a67f38fe65546ccd13c3d3b9e764773ef6564d4c75`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4c19f9b852bc18085d7a237f610b8d17e9ae3cf9df27dfcaedb17ad66989f`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 62.9 MB (62873495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c347df2d48aa6a0a13b204f922e3aa0d2a903a2141f7fec56e238827618f83c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8903dbcded2d02243b239de4f8e5856b1408a76d92a85ea8da3eadb51665215c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37` - unknown; unknown

```console
$ docker pull mysql@sha256:f1be1d3c82c2db05575f68e30fa53a8013b4b7c5b8e89c755c34895dcc8bcbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5bd00c9bd1aec121e35b9fec92b8a58853f6285580685787191df7fefdd80c`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0b935e4f2c33fbf4a4605b9a99a5e7e4a9926dd4c7745cc672cda56ae80e2`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 14.7 MB (14664719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eff94985dd0ee34d72bc4ce77345aad13b06e0555aea06a2238c9b1154b6d7`  
		Last Modified: Wed, 01 May 2024 00:30:58 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-bookworm`

```console
$ docker pull mysql@sha256:23e2890afb54aa00ea7ff4f4f657fc5a853e37d7d9a85d9d1ed8b1dbee7694e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.37-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:3d02aa81c903a42cebc6e6bb407e1694ab1818bda55bf15b61a2742624fb8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bfd90cb949d20f852d49d5ad85491c93c1b9b91d45fe208e380321720f5899`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bde18031fe909f543254cc2e733160f72a752205a2949c6b40a4fb93b5019`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f5b132130169e78e654966bd3298ae5547afe735d026b6c503f9cd781578b3`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.4 MB (4422801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55afbcd0ee95b43da7f32cf64b89260ace0979ea80882f734ffa5d0c3b59312`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.4 MB (1449199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143e159e9ba53f9ab249e4dd23b8146c96256ec7429fd67b703970048d25410`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9824c3f585b77f8a653ef04d6f855bd4f083fc9c13ff653d2b1af5e3016162`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 15.3 MB (15281632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d8aed07a3abd808a32a1c8f93bb986712dcc84c94ce5595119523ccaad776`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668217c0d32afdc03ae00ca9b951002c2712c6294d9428c48b34c1806db544b`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1222274583182e0fc12661ac9ce631dc065e4cc10dcda00a146d33f1fabe87`  
		Last Modified: Tue, 30 Apr 2024 23:50:29 GMT  
		Size: 134.4 MB (134409341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93646b643b58c7717ff573c97f8732ea09bd6d616bf98ce13d1fe87e96531f`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7470a28f457e6deac3f34c84d6c8dbe20300497a2245d679d7dced2b8b7ad8`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34841c68669377f766eee6f5b9fe388c30796c6ec46e96452fc5ad2d2ce592`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:d1ab433d5294c0fd73d3b0dbd930072a2b008063272b1535d23e5b2aac7f8825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a86630f43c05e4d6049f3171246f462c68e29f488209ee07adf1d9301375a6`

```dockerfile
```

-	Layers:
	-	`sha256:c80288de35aea4344988f230740a6e5e3d3d3d7c957084b23bd95c884ce4d68c`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ca3c8ebbcb5ff586f0a9c49e88b165735b31fed5b7bfeace4df33efb746cb2`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-debian`

```console
$ docker pull mysql@sha256:23e2890afb54aa00ea7ff4f4f657fc5a853e37d7d9a85d9d1ed8b1dbee7694e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.37-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3d02aa81c903a42cebc6e6bb407e1694ab1818bda55bf15b61a2742624fb8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bfd90cb949d20f852d49d5ad85491c93c1b9b91d45fe208e380321720f5899`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bde18031fe909f543254cc2e733160f72a752205a2949c6b40a4fb93b5019`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f5b132130169e78e654966bd3298ae5547afe735d026b6c503f9cd781578b3`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.4 MB (4422801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55afbcd0ee95b43da7f32cf64b89260ace0979ea80882f734ffa5d0c3b59312`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 1.4 MB (1449199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143e159e9ba53f9ab249e4dd23b8146c96256ec7429fd67b703970048d25410`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9824c3f585b77f8a653ef04d6f855bd4f083fc9c13ff653d2b1af5e3016162`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 15.3 MB (15281632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d8aed07a3abd808a32a1c8f93bb986712dcc84c94ce5595119523ccaad776`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668217c0d32afdc03ae00ca9b951002c2712c6294d9428c48b34c1806db544b`  
		Last Modified: Tue, 30 Apr 2024 23:50:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1222274583182e0fc12661ac9ce631dc065e4cc10dcda00a146d33f1fabe87`  
		Last Modified: Tue, 30 Apr 2024 23:50:29 GMT  
		Size: 134.4 MB (134409341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93646b643b58c7717ff573c97f8732ea09bd6d616bf98ce13d1fe87e96531f`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7470a28f457e6deac3f34c84d6c8dbe20300497a2245d679d7dced2b8b7ad8`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34841c68669377f766eee6f5b9fe388c30796c6ec46e96452fc5ad2d2ce592`  
		Last Modified: Tue, 30 Apr 2024 23:50:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:d1ab433d5294c0fd73d3b0dbd930072a2b008063272b1535d23e5b2aac7f8825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a86630f43c05e4d6049f3171246f462c68e29f488209ee07adf1d9301375a6`

```dockerfile
```

-	Layers:
	-	`sha256:c80288de35aea4344988f230740a6e5e3d3d3d7c957084b23bd95c884ce4d68c`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ca3c8ebbcb5ff586f0a9c49e88b165735b31fed5b7bfeace4df33efb746cb2`  
		Last Modified: Tue, 30 Apr 2024 23:50:25 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-oracle`

```console
$ docker pull mysql@sha256:7be6469428941fb76720439b8dd9b659520e4eb79e25e0f8516c3cc56c85a8ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.37-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5ef3be4ea5cef8284a189c9d5c5e195bf9f964f9f79ee143d782b7206d113e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169059193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a39efdaa0e614fa654568e3db75c847ccf834872bb6dd19da932d83e01c1884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98f197fdb0f5ac8c3cb30ed8c40893c809ceb64d51a26dde2c25f73eaf807f`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8212d3737c98ba7ed1ed296973af035315a8697ec51911eb02774845d861cfd7`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977370f8b4972671c5e23b27fadfe1b29227a40069618ad7c7840beb30504d9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 9.8 MB (9755188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e12eae409d1c35ad2a3840eb83f63e9f4a84b703f23b7ac4694d07d0efa31e`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebe27f2f14a7ce430e2b64084ad94c523e55aef800ceea3482899e3f4936021`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c86eb65950b78873c308808c4e3bfe1d2cd69fe16d5f505486f7c23a14881c`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 49.2 MB (49162694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c587904a3fd2818bfb3ee56cf2c210650342deb8d56fec8b76cf64e46c6de9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49f7afeeee8c277d339480507cf466f95c3911ecb387ae52bbf11b390e15a42`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 60.2 MB (60183723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb1cf601a487c26fed88fc911f538a6e01bd02f396c5f3b621374c50c937823`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a590886c42d3cfc5073c45132805debf2cd499e9dec8fcef5b2035333df103f`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d417eadf6ff1d7982e472d5316b03641cc1f2f972e2044804e31f0c84b9f64d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b5cd6fae9e52d0921f84c5d89aaaa9487ee011745c3932b6ee8a0cbf5c3e03`

```dockerfile
```

-	Layers:
	-	`sha256:ddf11d9aee61712bc300946c025344243fe71d58ffaf9d588ceed2b90aa03429`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 13.4 MB (13449033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b50899f8cb41d4e5c6c35cbd2ca3cb1afa119fcdfe3352c849026a16ed6a96`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 34.9 KB (34899 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.37-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f4360337f719defad09baa2b7903241df4fe10767bc3da7208cc9fb912b50e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176323852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8053e13c41910f7a256d1813b7f94389bb2037cdc6d5d4b1c227a4e964c587b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el8
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cbeb759403d76c018dc9047dadc7a00c9a6bdb78d7664004ecf487631fce98`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ceebeb4e87b339016212257a51b4182c29ec87324baf655e99d3514e2148b3`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 58.1 MB (58142450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70daaf3f7c42ba469d3b17a67f38fe65546ccd13c3d3b9e764773ef6564d4c75`  
		Last Modified: Wed, 01 May 2024 00:30:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4c19f9b852bc18085d7a237f610b8d17e9ae3cf9df27dfcaedb17ad66989f`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 62.9 MB (62873495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c347df2d48aa6a0a13b204f922e3aa0d2a903a2141f7fec56e238827618f83c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8903dbcded2d02243b239de4f8e5856b1408a76d92a85ea8da3eadb51665215c`  
		Last Modified: Wed, 01 May 2024 00:31:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f1be1d3c82c2db05575f68e30fa53a8013b4b7c5b8e89c755c34895dcc8bcbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5bd00c9bd1aec121e35b9fec92b8a58853f6285580685787191df7fefdd80c`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0b935e4f2c33fbf4a4605b9a99a5e7e4a9926dd4c7745cc672cda56ae80e2`  
		Last Modified: Wed, 01 May 2024 00:31:01 GMT  
		Size: 14.7 MB (14664719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eff94985dd0ee34d72bc4ce77345aad13b06e0555aea06a2238c9b1154b6d7`  
		Last Modified: Wed, 01 May 2024 00:30:58 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-oraclelinux9`

```console
$ docker pull mysql@sha256:7bfc86b7256896e3f53e85b29159b18a9f3f53c4b96a1e99a7dc5939bf5e65f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.37-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5ef3be4ea5cef8284a189c9d5c5e195bf9f964f9f79ee143d782b7206d113e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169059193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a39efdaa0e614fa654568e3db75c847ccf834872bb6dd19da932d83e01c1884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98f197fdb0f5ac8c3cb30ed8c40893c809ceb64d51a26dde2c25f73eaf807f`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8212d3737c98ba7ed1ed296973af035315a8697ec51911eb02774845d861cfd7`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977370f8b4972671c5e23b27fadfe1b29227a40069618ad7c7840beb30504d9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 9.8 MB (9755188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e12eae409d1c35ad2a3840eb83f63e9f4a84b703f23b7ac4694d07d0efa31e`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebe27f2f14a7ce430e2b64084ad94c523e55aef800ceea3482899e3f4936021`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c86eb65950b78873c308808c4e3bfe1d2cd69fe16d5f505486f7c23a14881c`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 49.2 MB (49162694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c587904a3fd2818bfb3ee56cf2c210650342deb8d56fec8b76cf64e46c6de9`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49f7afeeee8c277d339480507cf466f95c3911ecb387ae52bbf11b390e15a42`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 60.2 MB (60183723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb1cf601a487c26fed88fc911f538a6e01bd02f396c5f3b621374c50c937823`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a590886c42d3cfc5073c45132805debf2cd499e9dec8fcef5b2035333df103f`  
		Last Modified: Mon, 06 May 2024 17:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d417eadf6ff1d7982e472d5316b03641cc1f2f972e2044804e31f0c84b9f64d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b5cd6fae9e52d0921f84c5d89aaaa9487ee011745c3932b6ee8a0cbf5c3e03`

```dockerfile
```

-	Layers:
	-	`sha256:ddf11d9aee61712bc300946c025344243fe71d58ffaf9d588ceed2b90aa03429`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 13.4 MB (13449033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b50899f8cb41d4e5c6c35cbd2ca3cb1afa119fcdfe3352c849026a16ed6a96`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 34.9 KB (34899 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0-oracle`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0-oraclelinux9`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:e4054c2973be8766370769312786404fbb4557fb591d9ad37beb2d00a2c574a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:96c332225878600240197ae810767dd7e4e5e246bc1f57c2ec94cad14d315640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171750074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df03e3cfc9471071296cc2456a66e238e7f84b6f2c8dd91330422505502804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed19546d518d0f164f97177682a5f85144e1de05c24b62d0c8439e023cce00`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501aa8e883deb323ac6b074d691f213a333cadf707a23b7fcea6d623dc27d9da`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c0b888a0f7e9043d1bc59384e4358443fe39429349dee365a030a4b717328`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 9.8 MB (9755190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670b7e1bbfd0e5cd441b36b56a307b909cb59be10b778e456922efe40c9ad26`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d50b789abe8f3bf3c7dc066ec2ec4d838cf0502558840d1cb6d7fbff0562e2`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd9fbae13f7c396a235c6e2f37ed5b4c4b649897c83e9124346f72756664dce`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 47.2 MB (47234025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7592f6de1dd34b1cf3d6962b44203c6b3bea8457a671b37741d0fccd47e74`  
		Last Modified: Mon, 06 May 2024 17:28:45 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795b8ab791a09064c3b3c69853cf89b86706fca1cb6d4912efa98b63a95f90e`  
		Last Modified: Mon, 06 May 2024 17:28:47 GMT  
		Size: 64.8 MB (64803395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cffac37cee141de0d62bd62b64127dfe273a5c6b7f54752170168d40c5633e`  
		Last Modified: Mon, 06 May 2024 17:28:46 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1983fbbc4e5e49e340c8225c12bf9036597783c8269f9f842f65c2ca985cf02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13595041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb676d2fd76b8a8e3566d1290684689d65d650e2e194e0b52d9c6b5478ccc58`

```dockerfile
```

-	Layers:
	-	`sha256:c92df696b83eb6f8d8b25ded2f6431e2ba36bebc2977149081bb68389db533f8`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 13.6 MB (13559950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909f5a3aef56695e2889d19b5901504445511b0ea4f65cf0bc7cc90ea32595`  
		Last Modified: Mon, 06 May 2024 17:28:44 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9c775bfbb32aa68de2aae2dc3801e1b27e6816deff71f5e9e71071cd1389d1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168851017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1b6f60db861741e0daf178410ac370c0433ab51c6b4c9debf8e59c73c470a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae186b7bd2a4bf79217c3f00080aba9dbd3987825f4302b4bda158308ae2678`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130f1dda4331229753037f918a7af3edacea070f4ab495a51c39dac81847685`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e957ad183cfb465a682a104902c6dd1c737cc9d03361976b92eca15ddcc92`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 9.2 MB (9169807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748ca1e5c1679df097a564d719108bb40f8cc51dda66b88432b4e38b67c1815`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9bd2b73010e9a5b472150ef6ffe20ddae8c8dfe066aece2c532cbb6d8b87b`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c62009fa89483168a4927bfdb86267d703b3520f0fbdda4757a1eb20fbf552`  
		Last Modified: Mon, 06 May 2024 17:41:02 GMT  
		Size: 46.1 MB (46111987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d96d7b1886937e2e53358881528e8540afb88d588b7d77eb8101af303d0b4c`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ca5475bbeb66ebddd6460d9ec4a3eff42ad2febdd494e79ca4060fccc0d43`  
		Last Modified: Mon, 06 May 2024 17:41:03 GMT  
		Size: 65.0 MB (64983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415aecb3e424bb192460b9f5f8b97284b4d43241b104638cbe0e58a85236676`  
		Last Modified: Mon, 06 May 2024 17:41:01 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f44c38693f0ce23ee05f5383885e54aef4d4eda8e58d4cd4c6156107a9b1a475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab65333fd304809a8de2b3a4909249d80ae7d4a1ed7acfefffccfc4b896cd41`

```dockerfile
```

-	Layers:
	-	`sha256:d38f5494c566d0d25d112390ead0e21721abecc9a600965527f64d4ec5ac22f1`  
		Last Modified: Mon, 06 May 2024 17:41:00 GMT  
		Size: 13.6 MB (13555122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b753352bb8048a26710116e1973c1b170079da5bd83afc4fe4910a12b4470`  
		Last Modified: Mon, 06 May 2024 17:40:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json
