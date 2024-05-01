## `mysql:lts`

```console
$ docker pull mysql@sha256:f7a8e140a7d6d1e6e0c99eeb0489c50a186ee4ac44ff55323a176529b9a43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:53a71a83be1fcbb1489c0fe23d377297f55b77a6c6ce816ca8fa30225adfe2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179341247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251f0669c6ec890f73deaaf7a7891d8f0cd80821d89b9122b950b679a331c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe9b2df4d05db3b7e249359d1e613682fa3f2c6b1a5425297826102fbef66b`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98c884ffd9ded4226246ffc1dc788bc14b9f3d8b94a5218e1ceed16bbce6d7`  
		Last Modified: Tue, 30 Apr 2024 23:51:43 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0e3e0c511ea6802887fbd56ff5b94184ba87b65f3aff0204a6a03216bfcd`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 4.6 MB (4599789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64520c05a6b1b103b680e92e3d2f25bb616a6259a7631625de8a88083993b59c`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3ebffe5345bf0b168246eb753a3824b01d85c353cdb26924d418de27322eb`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be2eca8f885426e56640bb42c1d5c0ac6be94ce24c5e763bfec7322a7bcc674`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 55.6 MB (55565648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810320f66957eced0dc72d3c938fbf3af47cbccf450ad5e80400ae6c1882e5d5`  
		Last Modified: Tue, 30 Apr 2024 23:51:46 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c425b59d0ec08ecb9ea47d38f9eeaa65c33e9718ffc91608a3556dcb8fc29e6`  
		Last Modified: Tue, 30 Apr 2024 23:51:48 GMT  
		Size: 66.9 MB (66863077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7387b81cae9182cd820343599b7b7432d2d71a707e84d62edc5e57da5955ce0b`  
		Last Modified: Tue, 30 Apr 2024 23:51:47 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:1428fbc99fd757d0553e1f14e47379e2bece98a3b6973932fdaddc6dd33171e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14812465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76845e51122a392850911f26ed69146a0941ca077f4801a609072e495026fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:317e850b1e19b8eafa1b0ceef34783d95fbb1f3f0b5d38965767570936d3ca23`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 14.8 MB (14777374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f37eece2d2f368cff32246af89a9f298aec0374bb9047d61d3105a5c4186af`  
		Last Modified: Tue, 30 Apr 2024 23:51:45 GMT  
		Size: 35.1 KB (35091 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cf99e569402db84ac017aa56d09059f0b226f9a9c5644de24cffd4266dbda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9b4335a45c26b4204202c74127df42d2a28b22180e37f261c3809eb462b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el8
# Tue, 30 Apr 2024 12:45:29 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 12:45:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 12:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 12:45:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 12:45:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae691a8c1b16066cca244ed4ea39e9b5c9af6dbf8d0347ed9ceeade76a8e750b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe011e50abc101883db1ab22a9bb6244d829c9bbe68c05b6874c0c1ed124a87`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c88c8fbaa893a4e5b948f4691a54b78782bcf57f77b47feff2c928dbce7653`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 4.3 MB (4302741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d028b2b1f150e0aeb6bfeaa5b9a244f5e9603ab59991c75aa9e0d26af02482`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc284ef09f941151cf5166e86b07fcc19f66f26f235d7dc6f20913bb6b4de338`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00367d65ff8291d336c1e5f8d314f111717488b4657e5da52543c33b829504de`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 54.6 MB (54633231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4b7ff3dc2fade4a92765d67a8c5ce7565bcdbf4c3d2c86d58790a732d37c1`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafe7641a560f53680cd7f1572d853f011df819bac82c80b1bc568446ecd6c28`  
		Last Modified: Wed, 01 May 2024 00:29:03 GMT  
		Size: 67.3 MB (67283710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b85ac37bb0900dbd819827cfdb8ae885be535195d33bc2dfac13b79e9c534f`  
		Last Modified: Wed, 01 May 2024 00:29:01 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:b0701fac0befd17e4cdbdbb39fa07cb5237a6b439fb49f21cda49f39be1b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75308f5373963ad1bd230e3d4c9bfca49ac4dddbce1af270171bba973f5685a`

```dockerfile
```

-	Layers:
	-	`sha256:416437ab84a9e25108a8a94da095cb890a8d5158e2cb5719e340d4f946a58baa`  
		Last Modified: Wed, 01 May 2024 00:29:00 GMT  
		Size: 14.8 MB (14775654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3324096fdc8f73215f25425dee83087e5e91b5eb863938333beced58a0b0d97b`  
		Last Modified: Wed, 01 May 2024 00:28:59 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json
