## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:c9f0c66a87356518d4b30dbc065eb4567e4a04aff4d0ff194dea0973e5985b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:b317a3603ff116b06891b20180c5a79db2ef84f9bc827bb61986533f8feb139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236d29cb31b6801ae118b0cd64b8eafff369ccbc35eef2bc16df257ae3630627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:32:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:31 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:32:52 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:32:52 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:33:15 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:33:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:33:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709f9999ba9fca88b3f8b16dc99aa2ccb35a5d51de1b559e7eb31f2982a7b9d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88358ea2a37f7f1fd8a3310b5aa9d8b6197384655570ffde8a926030b428f9fd`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f63f165ac1f0d790e6ccc8870f319a536b2b82ed74090726c25125e8d71b31`  
		Last Modified: Tue, 06 Jan 2026 18:34:33 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b56c3fd28fa1c8c8bb6780c7226366a9a9faee462e4306e8c8c1af6fd5d6d`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7c7451801c506c5434314c284c735201385c50d1ebb5ac06844dd52017b85`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe44792537467abf8cd9cc3497f1b21164511c424080b30b89efe4a35277d67`  
		Last Modified: Tue, 06 Jan 2026 18:34:36 GMT  
		Size: 51.3 MB (51339629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07354dc33547059f72e3bf239e4353706c430a340c3cab1a8e77adce171d14b`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698677a468d5af4ada4ce79d7bbdcf218cdc182160c323a97687dde46ea20cc`  
		Last Modified: Tue, 06 Jan 2026 18:34:44 GMT  
		Size: 169.1 MB (169113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96a80bb47fbb6940c265a8f3ef707c3c6674b953ef44398b126e0912b3d314`  
		Last Modified: Tue, 06 Jan 2026 18:34:32 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b54645e48b4346d729374e20cf3f23ad107d7528f1afc669806e7d19dfd67013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0385e46bf1cad1c2119efdf7a68ac9fbde56e511ed204b37f0787ded02029fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66c6165c3a16202cbb2b053079fadce3b20f7215326ecde185306589169a7307`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 17.8 MB (17811688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d7f97b5c4522633c0814deb5c57e19e22dd90153653e9dc76aace61597b15e`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:5803f493c8ec1029e443636801105bd16e53ef28a420ef465c88d5b6f0497467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269808229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6724bf044bd7c02a5c236dbd72b5dd6ea43fbfca0fb0019930d52ab13c2dfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:32:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 06 Jan 2026 18:33:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:01 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 06 Jan 2026 18:33:30 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:33:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 06 Jan 2026 18:34:01 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 06 Jan 2026 18:34:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 06 Jan 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 06 Jan 2026 18:34:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2653216549473db1ae1b74b57a452f94ceafe129679260d1cd8ba9a0b27eae77`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aebf50e281b3dbc004f6417d888e0a081d51ff89069ebfb069d0b63403b85a7`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95683f341f858cf0e1f39362484c5bbc31bd83b12664ac9eceec7b387f99616`  
		Last Modified: Tue, 06 Jan 2026 18:35:30 GMT  
		Size: 5.8 MB (5799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab579436a91cdb7ba519047dba88b32d8755071dc76367035cc4ac5be2e8418`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef469011926034bbe2df3069e79fa4047ce4899752be06458eb361523a35fd`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3d8641a8ecfc8a5cd927394dd31ee42d6f681c82362ef9e10061bcb7cab8b5`  
		Last Modified: Tue, 06 Jan 2026 18:35:41 GMT  
		Size: 50.0 MB (49962792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624be88f1666ed155c0db69e5694628f852c63b34e0771159ac3782d70df40eb`  
		Last Modified: Tue, 06 Jan 2026 18:35:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a5f1de5df62d1b667b092cf18c66d3c09240956bb0ed49fdb03dffa6cb4e4`  
		Last Modified: Tue, 06 Jan 2026 18:35:47 GMT  
		Size: 167.4 MB (167393456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691a4e39239db33fa3338ac7924527453265006428e7d749e055ecb5ce0c822`  
		Last Modified: Tue, 06 Jan 2026 18:35:29 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a26d9672945438dda6e43e7b789d29afa7ccb068b7777b45ef41655695d121e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f75d2ef6deb3d19388c7549de1b15955b08115f7f7939faa3a7a0dad6eaafe5`

```dockerfile
```

-	Layers:
	-	`sha256:883c25bdbf0948e9e20d55778cbf3ff82d635790a19c1e4f370366130c3dd57e`  
		Last Modified: Tue, 06 Jan 2026 19:03:33 GMT  
		Size: 17.8 MB (17806827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7ec6e11e73ada0fc396b5ec1289ff595e65841b53d0718c3ffb13c4509fd8c`  
		Last Modified: Tue, 06 Jan 2026 19:03:34 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
