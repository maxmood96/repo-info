## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:c5467c2e0e1b0363d9b67633dff98d3e0ab5be2fa70f90e12fc4b63dc79a5f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:df4cfb291d2e44cee88e995cd0314051bc23de5814ae8469807a58a8ae966453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266374976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d5e0d25756954afbd8fbb67305dca03f684396c2d37924e9dffc1f16f10236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:47:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:47:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:47:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:47:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:47:26 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:47:26 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:47:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:47:51 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:48:26 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:48:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:48:26 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:48:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556889a7ea216ad993d14d786fec2a310897f46f72c5799716600756689b23e4`  
		Last Modified: Wed, 21 Jan 2026 23:20:57 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64679a587865f9dbf4ec5a178ce931cff203bfaa5baf2fa94c9ea74454a5b2c1`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be98706b18411ee96bb21a56f00071769beb2e6b60a99663d89c1adaff64f2d`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 6.2 MB (6175130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba34685a51a62b769b2d92599e879e535ae38e6afe3414d6dda8446a134a88b`  
		Last Modified: Wed, 21 Jan 2026 22:49:18 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21766700fc3f665ea0b679a3600facb0dc3fe12fb1817ba557a5c35a7b8bbef6`  
		Last Modified: Wed, 21 Jan 2026 23:03:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab4d3d2b3f465d2622d858417736b9d33e72d28eeaf5717901f7c69f8564802`  
		Last Modified: Wed, 21 Jan 2026 22:49:22 GMT  
		Size: 51.5 MB (51455805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7baff9b9ec4d330ed11d726685186939f5c27a671099027d086f87b14a80c39`  
		Last Modified: Wed, 21 Jan 2026 23:03:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6adb7c320bc33bab6847a70821f252318d5699ed31346e268c75e73d8ab6e`  
		Last Modified: Thu, 22 Jan 2026 00:02:03 GMT  
		Size: 160.6 MB (160636465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acadf0e1453f883c90e7d134be916f8db341b2a9cf7d41807b14da29efd0fac`  
		Last Modified: Wed, 21 Jan 2026 22:49:00 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7979e3f17f815c535f0456a82770c50f364022755c9e8b7fa702d58cfa1577a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919e1d63bd52ae3e9c329fa94f32c838744148210b0993ab17546ef55c71b0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d3a76eac00ed9c149160e311b3b6b6f337d5487c37889c9f7b87f0a2caa41492`  
		Last Modified: Wed, 21 Jan 2026 22:48:59 GMT  
		Size: 16.3 MB (16297380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59561772ffcb448fc74b9b90a5706f491b8e83f5adc09664dc9065c5528411d4`  
		Last Modified: Wed, 21 Jan 2026 22:48:58 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:82fca4df9fe6179173542d99ea2ef0a8ca3288a448a3eb2450cf25d69fa6d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a97355555f9a80c5f0be5f19afd517cf962c4b2f6eb0b9cb85cf1d0644412d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 22:52:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 21 Jan 2026 22:52:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:52:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 21 Jan 2026 22:52:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:52:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 21 Jan 2026 22:53:11 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Wed, 21 Jan 2026 22:53:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:53:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:53:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:53:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:29:32 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b97ba280c2402a350d4fb92781217f8e821919aa1817fc58535b8189206ea3`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d4b379f5d476c9db4581814d636cd7ea810c961f1a6c7bb2b8d4fd9f20dab`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 737.5 KB (737532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca316e35afa1c3dbc114fbb4af7b672bd851675e52e5953b30127aeeb7ed4f`  
		Last Modified: Wed, 21 Jan 2026 23:40:35 GMT  
		Size: 5.8 MB (5797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe8cedf0e06861042d3b8d2ead56431d69d86bffaa5eccc4a76a56c5b722ed`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503364c2ef5455ca6cd1d95132b1e591df132f9efe086719f4d0cd3848d324`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e912f3b012caedf3921783bbf8bf7122e16d20abd3d5dc895c591c5856c8f`  
		Last Modified: Wed, 21 Jan 2026 22:54:31 GMT  
		Size: 50.1 MB (50086528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b12e4097253fc054e98fb79fe32c7854736986bf288c1aa91da7129f5ac70c`  
		Last Modified: Wed, 21 Jan 2026 22:54:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8e9992cd435f9effbc14da74eb71b1909972f62d82d94b110ff87d15e58e7`  
		Last Modified: Wed, 21 Jan 2026 23:13:57 GMT  
		Size: 158.9 MB (158941435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f32736fa44e2d8b6e9ef14ce9df5edf470e8563a3ea62c2fe57f7889c175a2`  
		Last Modified: Wed, 21 Jan 2026 23:11:21 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f19559953e6691ae3bf76f61b42e7521478053162e2f68d1522d705abc65139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa8052602e023b2ee598b883d0051719faf757dab7126df1719218685638ee8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97c40b03aee91de311df824337c9ea2721e5e5d31ae3069b4e8e72018cf9d2`  
		Last Modified: Wed, 21 Jan 2026 22:54:29 GMT  
		Size: 16.3 MB (16295836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7adf4674ecc55f1c5f92e2f84326e7d7e5089f43f48dfdd22b39ee36bbc85e9`  
		Last Modified: Wed, 21 Jan 2026 22:54:28 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json
