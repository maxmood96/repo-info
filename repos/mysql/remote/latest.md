## `mysql:latest`

```console
$ docker pull mysql@sha256:569c4128dfa625ac2ac62cdd8af588a3a6a60a049d1a8d8f0fac95880ecdbbe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:1b2b0dbae3ccc2739726fb22c50394afb414f122d0d2945c2662315c47a007c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277540772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b0ca07d79d7d19c8da64558c3ccdd4ea635ac2193f551a1cb5370f33b494e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f78fcd9ccb610500632aecc1bfe9e99e435e59db4bbc4bbbcd3d88c42cc978`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494c372d15c3b92efb09997030051878646d920a87c1b3fbe0cd97db2035b923`  
		Last Modified: Wed, 22 Oct 2025 02:42:43 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee80f7340cccc4aa006efed1341c559a2208d5aa56ca63333c693e0e4f626c`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 6.8 MB (6819639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480d01bd7a6a054f0991aaa1cb36f2c5c0ddbc31a3a745501d6de0969d1095f0`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e15e3ed24cc4f9aca80d06d9e1c326fdf2d6c9010aec6ade4a5b6adcb0909`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276de9b557163ac7f4e24ada733affb7896174f8bc5a53bd45585ec6dfae78f`  
		Last Modified: Wed, 22 Oct 2025 02:42:57 GMT  
		Size: 51.3 MB (51321454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd145fbb4492429860f19b1c488cfd5e7b3917ea74516712e292e9d752b481f`  
		Last Modified: Wed, 22 Oct 2025 02:42:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f7744d0e71a4f56974497ec5607084830ecccc031503a866c71ec5dcbc1d7`  
		Last Modified: Wed, 22 Oct 2025 04:22:51 GMT  
		Size: 169.1 MB (169110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa606d8d58de0a0d2990e09dfe17f14ee464e557af363532ea90a49a685182`  
		Last Modified: Wed, 22 Oct 2025 02:42:54 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:54cbc65c17e56327079dc13852fe057cbfa83c415f2313fed68074ca5af44ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17865377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c395c6b440ceae150416c04c3941853bf4e8a3485ff4d5591be41807a3ad64f`

```dockerfile
```

-	Layers:
	-	`sha256:5749196f2538dcab18d4c445b831abee3f15af6ca3f7051fd60dbcc220d4a04c`  
		Last Modified: Wed, 22 Oct 2025 06:03:07 GMT  
		Size: 17.8 MB (17830059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223a17449c8335efc7f979f04e8a24b19f6b6c74eb7fad5fd19dad2a425e14b`  
		Last Modified: Wed, 22 Oct 2025 06:03:08 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4da94ed67fc2695883a64f3720dd8f3490c5cc5560667b6b15ed2f2b5cf3323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272616912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa344fa543e03d111daa10b6a8474ad2bb5c6d3c4f3d10e443e3434e42e32bb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 21 Oct 2025 16:26:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Oct 2025 16:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 16:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 16:26:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Oct 2025 16:26:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cb767785c6192fb7510ab5e3dbcd38c5808a826b1d174cb2afbb9362610c5`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3284b0d66176c7ab8a32274a474751a67d325a0fca26b7ba7be89ad1ded17951`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 737.5 KB (737529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd8cadb823e40da39e6aa549ea6683a2f5f9c2bfc8bf197e351e840e7bc4bb`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 6.4 MB (6445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8114797ee6f2cd67249493e130baf782ddc3b7dfee7aad0691c5695674c6981`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a4e33375732e45093846450c223ca063ccea2b1b51832fcffb44709564fc2`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb72166c81f17cf2283db80fbb471a65acd4cfe66a283a158ebda0e67cb01`  
		Last Modified: Tue, 21 Oct 2025 23:41:19 GMT  
		Size: 50.0 MB (49953680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6c3c04d2e239d3680d2263ea73bf72c9ea2b6f56b24754baec560baee63f8`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4464c8f33a229d135fe54db6b1b818436c749cce236e626b8dc0f96372ead31`  
		Last Modified: Wed, 22 Oct 2025 00:03:30 GMT  
		Size: 167.4 MB (167384282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ce7b7747e937adf712f5cf57d2b46536a05b3266fe60c211c9cd33239d469`  
		Last Modified: Tue, 21 Oct 2025 23:41:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:92f7311eb1cef8eb48189516bfcedf4f28d4660552d4224a731dc1a1ab95b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17860861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0f7eae7d712200b01cea01645acf3bc81d16a6af9628b8d3a053ef19e8f6a`

```dockerfile
```

-	Layers:
	-	`sha256:5de8dc2da949f82a2bba71e1ea46f2acee7dbefe88e4ded381e25a62b88bb4c5`  
		Last Modified: Wed, 22 Oct 2025 00:03:06 GMT  
		Size: 17.8 MB (17825202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3185f59b680aef401fd9f9c0035cffec567528673263da328c99e5ef8b78aa94`  
		Last Modified: Wed, 22 Oct 2025 00:03:07 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
