## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:740f4abb8df45ddc7a38907d65127ce1fd830f0ef3acae49baa954e3e232efe3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d5834be9554907e05040ace3652a285a735c7bdb3d3203a3d02c86595ac52389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232928920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7ec93b2d27e7d772611f2b99684f935655405b35040e1398c6028ef9373d85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Apr 2025 22:21:58 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:21:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:21:58 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:21:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2e0d7a943c50e207f5dc2de837a65181aae50e9748620216168ea33a11ab6e`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c584d53017d7d4ad0c40c96692ea91019a6627ecbbcef7e1af5cd683443eb75c`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a083e6773fe2be31d64cc73560d304a17c0920665948e0ddf2adbc8657b1118`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 6.9 MB (6896508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a3958f09f67bb463e1a0f4797d768a508205d1a6a1ba2e0982ad82334f0b5`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce034e276703d9aa589e3795f5d88fbdb0b552e5f613298d6feefab44d8bbf89`  
		Last Modified: Tue, 15 Apr 2025 00:07:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321a2421328f68399c4629383ca60cf4469987325af27a832bde75280482f76a`  
		Last Modified: Tue, 15 Apr 2025 00:07:55 GMT  
		Size: 47.6 MB (47625498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee09a5947995ebd1ac8eba326f4673ed1ad96b06c750803741b981e12958401`  
		Last Modified: Tue, 15 Apr 2025 00:07:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858243b9b468c97fe06f4816777806dd3f5123cc4f7d4c0d89d1e74ba58d5496`  
		Last Modified: Tue, 15 Apr 2025 00:07:56 GMT  
		Size: 128.3 MB (128323222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b30d20c5001b17348fc58f9a4f83f6af20ef1b959012b39f9b7e9f0b74a1e9`  
		Last Modified: Tue, 15 Apr 2025 00:07:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:adcac7043fe4113b0a3647ff72a9255f8dccdcc7f3479ba909b654114a930ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a9a860dc8368874b03efd4eef7ac4ee2462442f62916d1afaf23a74df56cbb`

```dockerfile
```

-	Layers:
	-	`sha256:720fbf9caaac32370cfa751ad19e4b2a535405c3eef8a0facd749848b52c2ef7`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d56edbb79bb1a940fdc2062e5e580e3eade56caf349e3997936467b989f809`  
		Last Modified: Tue, 15 Apr 2025 00:07:53 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:fb65643b68efeb31e3568387fdfd936234ff99109af594ab14545dee1f348739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228395821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7459ebb97186273e186ebc4a70b47e41ad9922ee09efcaab32f7cd8283bf41ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Apr 2025 22:21:58 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Mon, 14 Apr 2025 22:21:58 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:21:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:21:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:21:58 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:21:58 GMT
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
	-	`sha256:03e4166ec9246dfb24f78dc29c72bba5e8a1ec684416156e13878a9cbce82062`  
		Last Modified: Tue, 15 Apr 2025 00:12:06 GMT  
		Size: 126.8 MB (126797114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc1ff7cfb43ba3097210e487e1a0d6d9185c11f2f0a736062ab17a523bdcdf`  
		Last Modified: Tue, 15 Apr 2025 00:12:03 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6626d2dd1e22c78d65921be2e90cc1f1360f8c44f4d677f2e1b6ca199c008f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d99c639aa227bda53294003cbbe4444c1c14b56fa4c59c8b3f7b74093e31b18`

```dockerfile
```

-	Layers:
	-	`sha256:58e9ae11c1ccaf9d9c5b5a633aedd6a76958bcfe2c497c7875a19e8da6027cf3`  
		Last Modified: Tue, 15 Apr 2025 00:12:03 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb445664056092858e39170ae90ed9a6ca6cc0769423d6504e1de19d83a054a1`  
		Last Modified: Tue, 15 Apr 2025 00:12:02 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json
