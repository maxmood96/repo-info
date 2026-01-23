## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json
