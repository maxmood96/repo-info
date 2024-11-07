## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:6bc3ac72e858ad6ecb651229520fe14848b885ed01b3f08e2b201a25a5f49476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:71da9b9b29db60ff36bae7c55b517428c86f56f97832b6cab5eb207e7e3ab5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171090177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66f13824d51223b7dc62e4ac5bfd421263e51d2208558d97401f533658af36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3df8465314eb14486cc9db3231db658622369f1ba77f9b40b5ff383b2a368`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1cd7434237619cc425ecf9b532f9abb9138942436b2bcc5515c5b20ab07221`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68a3d6699c6dc383024eb9f32e52d61b1e75f707028473192ad99d6131833`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 6.7 MB (6738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd18f0a1d738f44635df1c032d9ee461fcb704e147c4704b4897b0e05ee935`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b413c932fe53c3dfec02713f5a901e93c62aaecb0488a5805e7a9ec18271fc8`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea237e91839f2ba65d78c2faf2d5c7e4235518520383723c536fa528c75c51`  
		Last Modified: Wed, 06 Nov 2024 21:52:26 GMT  
		Size: 47.5 MB (47537753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14bea4ae90d3e6f829e6c17d5d8f40ce13301486d9b972a8d8443c52f3d73d`  
		Last Modified: Wed, 06 Nov 2024 21:52:24 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3925a49a01457d78a69506f0710563b70606f7b255579322d325f92de23d0`  
		Last Modified: Wed, 06 Nov 2024 21:52:27 GMT  
		Size: 66.6 MB (66603624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c128e29a0db891337ad96dfff60c48874a31841f383ddc03cc0076fc61048a`  
		Last Modified: Wed, 06 Nov 2024 21:52:25 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d090f1afd48c5d955112e225d88f9bd7842b0e064ddcc55e4bb21de913032b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411804080d9540b9e1aed8a1014b1dfb7adbc353e0b86ecbbf2544d9a3d7717e`

```dockerfile
```

-	Layers:
	-	`sha256:61a84c00a93f2cbbecf8a6d3aa6978094ad5f4adb429e27ad37733e9d39b387c`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 14.9 MB (14856758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4aeae5f4e1373402e96c69a93a39305ec04f5b1d58711b65466bd3914c8113`  
		Last Modified: Wed, 06 Nov 2024 21:52:23 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ec222b681dd4ccea2f24b25d1c601713af8a0a92261bf6c878d03e7ea03b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168376703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167e41e4142004f0554551fdee255b0ea096a792cb37053e4c212ecbcadff4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c6c53fd855e1a3b641f7120edb980ec5abdacd154feaab212e4841906620`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31f49f8fe3f277a32f97bfab22015af69fcf01fc569249c0dc18e1a4c59b98`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3af4e8f7691c80db5487b014072835ce330b1f4df7acca98f0ddd14c17aba`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 6.3 MB (6326803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be80e519a045db238a9a194aec4f4cfcb922a0bbf413338162d378f768a3b`  
		Last Modified: Wed, 06 Nov 2024 20:52:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772a6f2cd098361c120e56eaf9dcccec7202f6893fce4f2fac304b09bcec0d7`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6991f1713d0886f5355f93fb3ccca01e4780d3c4607bac61d3661a0b5484a7b`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 46.4 MB (46428551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0e1f59c6b7a803c0cb16ad072ac59613d409e80fa067843de0f217b64a384`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6f3b454d056b02f880779aa2189e9231aefbeeff4b35e7eb0babb80d8014`  
		Last Modified: Wed, 06 Nov 2024 20:54:04 GMT  
		Size: 66.8 MB (66806740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b55c20de4b2dbdc5be1fe33f03e572ba12cc7f60f8546635300495e94a79a`  
		Last Modified: Wed, 06 Nov 2024 20:54:02 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:cd3e128bf27544cc2f31628baf72e343005faaa126025fce16b6fc6450517f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f19b12c867cfca885482f91f58e793f0fa69ce427869dd9846dae06e20cf`

```dockerfile
```

-	Layers:
	-	`sha256:110ef4c2ca1e0b5f94c878db14a696a004a50a80c10746ec768fb7860695b928`  
		Last Modified: Wed, 06 Nov 2024 20:54:01 GMT  
		Size: 14.9 MB (14851908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb7093fe45ff166bcc1f941d51b45e2460a1a513dd99e2ead7e606083e20cf`  
		Last Modified: Wed, 06 Nov 2024 20:54:00 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json
