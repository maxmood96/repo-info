## `mysql:lts`

```console
$ docker pull mysql@sha256:ad394eabaf5d728b88fd79732d94091f2165379e9b43e9748364b8c094f26e14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:e8a0639002fef32021b634569e9194b46796ac54fa8381aa2ebdef0b90a235ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (237019646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db55517bc03908442b1e2e26452939896238cb3058e50dcc1416dc6d58a1991`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
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
	-	`sha256:10aec8a104c7ecf055b7137fb34a3666fce4dff1b9f6d210fb88eaddd4c8c329`  
		Last Modified: Thu, 07 Aug 2025 23:49:00 GMT  
		Size: 49.5 MB (49497127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b0ea5c7edfe1818669b1ac83f5f9ff0ba0bac3326748cb5be448695cfdfc6`  
		Last Modified: Fri, 08 Aug 2025 00:11:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48102d6aaafe573ae9f89e38e13e9d85a44d65c869ff9f48ffad3bb8652b165c`  
		Last Modified: Fri, 08 Aug 2025 00:11:48 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b263198a79949862aeb194411c528ca334da3edc1e2131e03cb82424cf3bcd40`  
		Last Modified: Fri, 08 Aug 2025 01:00:55 GMT  
		Size: 6.8 MB (6818626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29def2d20dd4699f552df613e1a9f19e8a7196127efaf7efeea2151c4335b0dc`  
		Last Modified: Fri, 08 Aug 2025 00:11:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ca6c0b3caf397e1d7fd07f9e15849060e08c5c68463a0f69404125e1418743`  
		Last Modified: Fri, 08 Aug 2025 00:11:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29875012b20a580222bf8dc9c5273bf64490d33dbcb6bcb21f38c9384e3dfa48`  
		Last Modified: Fri, 08 Aug 2025 01:00:58 GMT  
		Size: 47.8 MB (47767206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ec2e3797974a2a77cf597a989c66e9df35c6ad48ec792d8bf663e66d2d4144`  
		Last Modified: Fri, 08 Aug 2025 00:11:59 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d7adf4bfa3ce9b75b3ffab6073ad2b312d200a7bbce00c534cdaadd7796ed`  
		Last Modified: Fri, 08 Aug 2025 01:01:04 GMT  
		Size: 131.9 MB (131944209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d93b00a66880988ec0c1c85681cecb01cd61d7e6460c8fc4e8979972f56c22`  
		Last Modified: Fri, 08 Aug 2025 00:12:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:94fcaa5c64e07f84885f93fac3d379b36a9ef33a72976dda686f9e7beb0612a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e11210a36ebb9494680996a9ad8a7b7338c2984506d1d91325f373ddf0328e8`

```dockerfile
```

-	Layers:
	-	`sha256:d5021b0359782e96e0343475acc31cc7fe38e8f52fb9a789e374883070fcd940`  
		Last Modified: Fri, 08 Aug 2025 03:02:30 GMT  
		Size: 14.8 MB (14804922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6667c2e6768b7778fdb95b273c1c4f2737881b694f1ab4be03799e5fa22eb938`  
		Last Modified: Fri, 08 Aug 2025 03:02:31 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dc80dc8fb761af4c489607085ab973bfb5b286e554259fb0c1aa3570a37ee782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2df3d226bacc2aae919ea834a0cc467836f51ee75a4a77a6e4318b6c28cd1`
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
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12642f09769eb349de06aea10d4609cc12eb81e238714e9af45811813b4231`  
		Last Modified: Thu, 07 Aug 2025 23:57:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739cdd12ec77d448f93849150c53cf301f3e1de9e8af8a68273b7b367e8b9431`  
		Last Modified: Thu, 07 Aug 2025 23:57:46 GMT  
		Size: 913.4 KB (913442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e901e4e4c139386b4b372483359fd51925a811eb3795cab994e3902dcc8723`  
		Last Modified: Fri, 08 Aug 2025 00:16:15 GMT  
		Size: 6.4 MB (6446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19592870864a65bb7b34d3cf1a267cc76ac1fcca4d5619e47de3cc2d8419c399`  
		Last Modified: Thu, 07 Aug 2025 23:57:48 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39bf601a8f38d3a3f8386fff1821a460baef80efd721aa299dad351d4835f`  
		Last Modified: Thu, 07 Aug 2025 23:57:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef658516113bc95ec87c99c1b2d4b9d336afe851893f9bfbb1d4945529e459b`  
		Last Modified: Fri, 08 Aug 2025 01:46:58 GMT  
		Size: 46.7 MB (46653469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4c1e6baf03c096209eae8ddfd7414900ff578117fb867bf73d756bd7bd1fb`  
		Last Modified: Thu, 07 Aug 2025 23:57:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688f8e7baa3ad3488ea7f0689a918efea096803d9caadc5714bf71ef1b36f36`  
		Last Modified: Fri, 08 Aug 2025 01:47:07 GMT  
		Size: 130.3 MB (130342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c46015e74a3cb49be59fb76e2bced8cf5ddd337f1531307d0af78fb050e8ee`  
		Last Modified: Thu, 07 Aug 2025 23:57:56 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:a6e2a4424a2fdf5da85a5657e13df2e6d1990a199f94c21eb9bd6355d8fd0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e01fa3bb50c6a0a4c4f259afd8355bc12963f461947fd9498aa39810efbb88`

```dockerfile
```

-	Layers:
	-	`sha256:6f92339c56022c949bbc1f028fe64c8252db1ed85a94e98d721e0945f4a08f65`  
		Last Modified: Fri, 08 Aug 2025 03:02:40 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374db211c0cda7d4f3d824a08c11a1412692c328cf4700b1684c2307b2445d0`  
		Last Modified: Fri, 08 Aug 2025 03:02:41 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json
