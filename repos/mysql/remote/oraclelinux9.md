## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:e0e81e2a9d38248893cb99ebe623359001e7feedc12617ec38589f8e52f8f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a04a60356334e1626dac5d4112ffa034b1e5b2f924eccf2c0e1d5e9513bb7a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275362860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbb21ac6e2a564ebe755fd077cfb79101602ec73f64b6e771e06419393d9de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:29 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 23 Sep 2025 19:30:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 23 Sep 2025 19:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 23 Sep 2025 19:30:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4ab4514f3f70fa2330887139eb97081f25773cc9f80e3343f80f8c6d6af79`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41962a6e179c9630f56de1dc1368caf7b8399e3f3e0380f1ea5071f45d80f6`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c273bf16257d1e1a07bc95d589cc2edb505bfe35634e15131e245c40de4c`  
		Last Modified: Sat, 18 Oct 2025 00:12:40 GMT  
		Size: 6.8 MB (6819546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7bb6f233809aa02e940808745b6dc2ead230f9b1b8014b6dc43239cb37021c`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14016e5704e9f43fb6a9fbb23dae339f98687d697b92770b1e531790ee61bf66`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec820315573127dd853c96854b89163d1b3ab1391255a222edfb876eca7b45`  
		Last Modified: Sat, 18 Oct 2025 00:12:43 GMT  
		Size: 49.3 MB (49286447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab5c52ff909849cbd904a4255c1ddfa85b4dee19e47d4de85ae40eb9b1bc1e`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df181eca63856fca89bc5f93aaea67c105b5565dca29c095fb856bbca46fd0`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 169.0 MB (168967326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e127489368459c556965f2b35c97b5055e709ec8bf3fe4c20cbe6a58a2162`  
		Last Modified: Sat, 18 Oct 2025 00:12:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:227443b5e664e0ac4121d18211f9d55a6f29907049d55f7630a10d84ec574f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7a61aabf216d0948ccabb7c40f9318074a8c54d68b1db5cdaf37fe9abdae9f`

```dockerfile
```

-	Layers:
	-	`sha256:50a66f9d377b015a692d476a32002aa1b6f12f9c58380af5a9d4f986414edee2`  
		Last Modified: Sat, 18 Oct 2025 03:03:14 GMT  
		Size: 17.7 MB (17699301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96513412703073e1d666b1e1e022722407349f85c6c72486f107685272bc9c90`  
		Last Modified: Sat, 18 Oct 2025 03:03:15 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

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

### `mysql:oraclelinux9` - unknown; unknown

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
