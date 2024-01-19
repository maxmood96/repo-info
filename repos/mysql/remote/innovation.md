## `mysql:innovation`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json
