## `mysql:lts`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json
