## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:16c128b276a52d9549d416d121bb8ad5368d7089e39f582b79079cb7455e8dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1717a37c2adc7772b569eb727bb198b6792f7d50c2adb4839ba637b5c9d88f42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165659693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71276df4a871c5c09ff8411247609cc9683d85290f9dc9b1871dd6e366a28f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sun, 04 Jun 2023 17:54:32 GMT
ADD file:39d09c6c7c3a0f64981f5cbcb12cc8f0128979c3d4b91d74c84fe62aca5ea87e in / 
# Sun, 04 Jun 2023 17:54:32 GMT
CMD ["/bin/bash"]
# Sun, 04 Jun 2023 18:53:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sun, 04 Jun 2023 18:53:08 GMT
ENV GOSU_VERSION=1.16
# Sun, 04 Jun 2023 18:53:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 04 Jun 2023 18:53:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sun, 04 Jun 2023 18:53:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sun, 04 Jun 2023 18:53:40 GMT
ENV MYSQL_MAJOR=8.0
# Sun, 04 Jun 2023 18:53:40 GMT
ENV MYSQL_VERSION=8.0.33-1.el8
# Sun, 04 Jun 2023 18:53:40 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sun, 04 Jun 2023 18:54:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sun, 04 Jun 2023 18:54:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sun, 04 Jun 2023 18:54:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1.el8
# Sun, 04 Jun 2023 18:54:52 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sun, 04 Jun 2023 18:54:53 GMT
VOLUME [/var/lib/mysql]
# Sun, 04 Jun 2023 18:54:53 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sun, 04 Jun 2023 18:54:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sun, 04 Jun 2023 18:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 Jun 2023 18:54:53 GMT
EXPOSE 3306 33060
# Sun, 04 Jun 2023 18:54:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3e0c3751e6482e67b70ffad144b2cb9aec9be672df2642a322e875e51b748aeb`  
		Last Modified: Sun, 04 Jun 2023 17:55:32 GMT  
		Size: 44.9 MB (44872720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7914193c6f0e6bf32545a75c783e4f919ef1fd267a806876c5d2f72da6c4be54`  
		Last Modified: Sun, 04 Jun 2023 18:55:22 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4b3f820487ae4bd2869d410c4e4dc497042a73306e0ba99071b261e33190c1`  
		Last Modified: Sun, 04 Jun 2023 18:55:22 GMT  
		Size: 982.8 KB (982825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63683b304e3d24e14589c48906cad17ead6bdf22ecf67b6291c12f5bc1544ec3`  
		Last Modified: Sun, 04 Jun 2023 18:55:21 GMT  
		Size: 4.6 MB (4614163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad9069836bd68adbe6be6e2c3aab749575e961266cd5ca27831330c21bb80d7`  
		Last Modified: Sun, 04 Jun 2023 18:55:20 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de90cd4c0e5df7a54d89ca2140cf329f530b89fe8c79de8873c66cfada8f5de6`  
		Last Modified: Sun, 04 Jun 2023 18:55:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892e565e2cf01a43d9d6d4b4053893b1b1ea7c36b5b77965eabe762292eb491b`  
		Last Modified: Sun, 04 Jun 2023 18:55:26 GMT  
		Size: 58.6 MB (58610758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73057d123da0d3d34811ea0383a736c549907f639c24ab1bf576813c3ad40ba8`  
		Last Modified: Sun, 04 Jun 2023 18:55:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1a3c0ec34ee20aec3f319f1f72ab7e94a9171b755be01adc71c30b19406ecb`  
		Last Modified: Sun, 04 Jun 2023 18:55:28 GMT  
		Size: 56.6 MB (56569548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fe8dc4ffe938cf78e257d45b0831df9a5053470ebed1d6978a85d061cb6dad`  
		Last Modified: Sun, 04 Jun 2023 18:55:18 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807488ae889657196a0f63400133a21d65d2ed24ecb1a05faed222acdbeac0d`  
		Last Modified: Sun, 04 Jun 2023 18:55:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7d0a45fa34f810414c187b8e414828be93e8590ce89f91df5bd705d3d5b15b55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169393383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1732fe3340d5c0968312658c137eaa840f53c3bb83b5f962a67e3bdd784724b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 15 Jun 2023 23:40:30 GMT
ADD file:37cef5fcd08f57d005adb8f14f69ecc78a9c669280f45f7d81b1c899489e93ba in / 
# Thu, 15 Jun 2023 23:40:31 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 23:57:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 15 Jun 2023 23:57:04 GMT
ENV GOSU_VERSION=1.16
# Thu, 15 Jun 2023 23:57:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 15 Jun 2023 23:57:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 15 Jun 2023 23:57:34 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 15 Jun 2023 23:57:34 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 15 Jun 2023 23:57:34 GMT
ENV MYSQL_VERSION=8.0.33-1.el8
# Thu, 15 Jun 2023 23:57:34 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 15 Jun 2023 23:58:02 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 15 Jun 2023 23:58:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 15 Jun 2023 23:58:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1.el8
# Thu, 15 Jun 2023 23:58:35 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 15 Jun 2023 23:58:36 GMT
VOLUME [/var/lib/mysql]
# Thu, 15 Jun 2023 23:58:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 15 Jun 2023 23:58:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 15 Jun 2023 23:58:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 23:58:37 GMT
EXPOSE 3306 33060
# Thu, 15 Jun 2023 23:58:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:029ab4a5f8e75aadbbba1505624cf10a4c35a0fd897cc85b9e7536785b8ba37c`  
		Last Modified: Thu, 15 Jun 2023 23:41:45 GMT  
		Size: 43.6 MB (43601336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379e18ca6956bdccee2f520f4ccc7284781f399b535905304436bc35591490d2`  
		Last Modified: Thu, 15 Jun 2023 23:58:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311296d6436fbeadfd03e0ae0355dcc5f5c1c98558f1614c769c7bdcff3b027e`  
		Last Modified: Thu, 15 Jun 2023 23:58:53 GMT  
		Size: 913.0 KB (912993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e90a5b94ab12d36935e1a1a25334fe6fbd1f53268e896bdc55ad3d53af1825`  
		Last Modified: Thu, 15 Jun 2023 23:58:51 GMT  
		Size: 4.3 MB (4294980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db50017c9a15b71f9511f7f1f5a9711477d408a11c8264e41c89cb0e9a43b26`  
		Last Modified: Thu, 15 Jun 2023 23:58:50 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161c1da0ab84372390263bf0c351228b372f7a644e62a4119cbcf24f5d80db52`  
		Last Modified: Thu, 15 Jun 2023 23:58:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edd797f390f0eaaee4fd70be5ab6000ec7a107da17615e56e136a36fd68c975`  
		Last Modified: Thu, 15 Jun 2023 23:58:55 GMT  
		Size: 57.7 MB (57684788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4467fea2ad904bac6b4971ed2d25a804a158d13f73d3ac1462ba7d4727e0c6`  
		Last Modified: Thu, 15 Jun 2023 23:58:49 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce24500a1de2c8409b9bb7a667cb5d30255c8c5208d4600de7e94f55e145a51`  
		Last Modified: Thu, 15 Jun 2023 23:58:56 GMT  
		Size: 62.9 MB (62889613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083135b3ad0925a8ae1c9176583bdd752145ba88e670b100f38f85d422424b0c`  
		Last Modified: Thu, 15 Jun 2023 23:58:48 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e3c290ce1494cfc96725e6ca52a984ded53b6b11965df8973a305bfcfe31c`  
		Last Modified: Thu, 15 Jun 2023 23:58:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
