## `mysql:innovation`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json
