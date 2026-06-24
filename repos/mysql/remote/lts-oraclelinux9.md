## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:ad88e1c86cbf12ef52d0a0360cd4b774d22956c5ee9c565645fb019d7aacb6c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:55e529b57e06b3da98df40600de2245a0ab4bb4b979e3ead4339349b0b50bf4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270842639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f49cc49cf9606caf19780a08c07d04d4736a86aad8548cbda99147640e564aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jun 2026 23:31:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Jun 2026 23:31:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 23:32:19 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Jun 2026 23:32:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Jun 2026 23:32:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Jun 2026 23:32:50 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 23 Jun 2026 23:32:51 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Jun 2026 23:33:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Jun 2026 23:33:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Jun 2026 23:33:22 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 23 Jun 2026 23:34:02 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Jun 2026 23:34:02 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Jun 2026 23:34:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 23:34:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:34:02 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Jun 2026 23:34:02 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6b21eb7a1e3e8c85b9f7c55e523b7309abb9be51ed5d639b708a756b2568459d`  
		Last Modified: Tue, 23 Jun 2026 23:31:18 GMT  
		Size: 47.9 MB (47923466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b86c090661773d54f5d9948a9573c514eab5992ca49bdf91859efebee7978f`  
		Last Modified: Tue, 23 Jun 2026 23:34:37 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fddb948e8a7138d3395b85b055f9aad8e64d607924d3f77c0c6a50450be47c`  
		Last Modified: Tue, 23 Jun 2026 23:34:37 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caad7b89f9fee1375685366f5c63a8ec9026c37474cbdffae147838ea2761ee`  
		Last Modified: Tue, 23 Jun 2026 23:34:37 GMT  
		Size: 6.2 MB (6193013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1152ace190ff9e978df0707433aba6cdac4a5fc8d1dca6d4cd32e61a89b812`  
		Last Modified: Tue, 23 Jun 2026 23:34:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3737f34f1214462a45fb814994c5af78dd0a1ec1fe152b1d809aae393e831864`  
		Last Modified: Tue, 23 Jun 2026 23:34:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f320bd2c8dda6c44fba5e8a3d8ecfa5807254ca71b4e8c53247a4b60c0e8f`  
		Last Modified: Tue, 23 Jun 2026 23:34:41 GMT  
		Size: 57.0 MB (56997315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047567c900ab5e4781a7e753a51a24859283a2e8364d6402ab5f5fad1a8962ef`  
		Last Modified: Tue, 23 Jun 2026 23:34:39 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33485abd4a2e2bf1fab992c426c48bc2c7d66ceeb5bb47d94e5121e0f1100a27`  
		Last Modified: Tue, 23 Jun 2026 23:34:43 GMT  
		Size: 158.9 MB (158935922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae77f7c30a429c38877bcf9ac7a6da572cc3df84768fde99d923be2cb00f9e6`  
		Last Modified: Tue, 23 Jun 2026 23:34:39 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d10d841d48f44912c923404a9cc2dd4a46fc5300963c010019179798b834741f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16834277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27eef0f8061007fe0f93034081c23bb1fc3a5360809b2841617f3747d95efd80`

```dockerfile
```

-	Layers:
	-	`sha256:86b43b4257d4fc7dfc96589ea8cabc65842555130c7eb1a5036c35f7c93f7386`  
		Last Modified: Tue, 23 Jun 2026 23:34:38 GMT  
		Size: 16.8 MB (16799169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35c8d9e39e0c1f6ffa052d342c7231d0cecfbf4f66a2e161e4f3d07bff6827bd`  
		Last Modified: Tue, 23 Jun 2026 23:34:37 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e01839b42f698a1e125bd86e37b0b575a1bf6aa09b8ee0207c04072416f757bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267248432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb812632299b38da6faac8d2c9a47cad0b5a737e0f0d4758751cb97184cddbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jun 2026 23:31:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 23 Jun 2026 23:31:02 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 23:32:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Jun 2026 23:32:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Jun 2026 23:32:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Jun 2026 23:33:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Jun 2026 23:33:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Jun 2026 23:33:22 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 23 Jun 2026 23:33:22 GMT
ENV MYSQL_VERSION=9.7.1-1.el9
# Tue, 23 Jun 2026 23:33:22 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Jun 2026 23:33:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Jun 2026 23:33:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Jun 2026 23:33:59 GMT
ENV MYSQL_SHELL_VERSION=9.7.1-1.el9
# Tue, 23 Jun 2026 23:34:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Jun 2026 23:34:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Jun 2026 23:34:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 23:34:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:34:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Jun 2026 23:34:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:14f0bac426a67d312501b30c0b419c0d5c2265f32077f348593b94dd76f064ac`  
		Last Modified: Tue, 23 Jun 2026 23:31:13 GMT  
		Size: 46.5 MB (46470688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd6d1db021f95d6b3919ceba15304691c4021bc25340e7ad5bc3acdeade345f`  
		Last Modified: Tue, 23 Jun 2026 23:35:18 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf40bfd83a5034e34467b8c19750f34a291df6b5f5a368679eab71fd087e474f`  
		Last Modified: Tue, 23 Jun 2026 23:35:18 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3b7021842bef27c263c2838759fce192c516106839a558727664bfbf775a95`  
		Last Modified: Tue, 23 Jun 2026 23:35:18 GMT  
		Size: 5.8 MB (5818424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fcadc25fa62541f33360c8207bb2028619b5f85169dc08929165820a294742`  
		Last Modified: Tue, 23 Jun 2026 23:35:18 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cbf08ed511246ed09586f8da7e203618d99322f60806b0357bdbe256045e16`  
		Last Modified: Tue, 23 Jun 2026 23:35:19 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf0ea313fe97703ad9b4e4db578264c893a092ce27371fd9fafdcaabc1e6689`  
		Last Modified: Tue, 23 Jun 2026 23:35:21 GMT  
		Size: 57.0 MB (57002000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5485a61b4619e9a174d19cf4656264e3113bbbc0ca88327918f5bbd41d33fec4`  
		Last Modified: Tue, 23 Jun 2026 23:35:19 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5116950faaea840795acd111d7c7738210fbb0a05e4ee9b8e800f2dc1e9c27`  
		Last Modified: Tue, 23 Jun 2026 23:35:23 GMT  
		Size: 157.2 MB (157210433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b47c579fe5d75675ef27d217cad67805240634f0bb7ee1fdded8ee04f60317`  
		Last Modified: Tue, 23 Jun 2026 23:35:20 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1c733fd3e19a8709dcccfb79114115c918d3f7f480b1daa3542fbeb181780c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16833090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4a1cebd9fff84e8dd7eecd866e0fc70f7afac0c325e51973e4e89b58fca415`

```dockerfile
```

-	Layers:
	-	`sha256:0e677ce595b584e99a8eeee0c18b765473fe993fc25cb3a170654b81ee5574d8`  
		Last Modified: Tue, 23 Jun 2026 23:35:18 GMT  
		Size: 16.8 MB (16797641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4445691a31b703115ea86b9e6c75b97ca5bf864673dbdffcc4feca30064fbbdd`  
		Last Modified: Tue, 23 Jun 2026 23:35:18 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json
