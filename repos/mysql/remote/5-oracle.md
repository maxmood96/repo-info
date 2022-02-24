## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:253bd7f3bfdccabebd72464fddc9b40ca31b5ab7d49920c0116d3735d71480b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:256f1ebd8c797259f9d6c9f0a49b998c6026affa9241ccacb5f6154712d67fe9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123651154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17d550601049dc421ceb55d32268b687afa85f3d3c7d2e44f0933481f8de1c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 24 Feb 2022 01:15:28 GMT
ADD file:a953cc04974b35909ddbd8826601c0824f8cc920ebc522046d4ca64e69c2c26f in / 
# Thu, 24 Feb 2022 01:15:29 GMT
CMD ["/bin/bash"]
# Thu, 24 Feb 2022 02:03:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 24 Feb 2022 02:03:22 GMT
ENV GOSU_VERSION=1.14
# Thu, 24 Feb 2022 02:03:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 24 Feb 2022 02:03:37 GMT
RUN set -eux; 	yum install -y 		gzip 		xz 	; 	yum clean all
# Thu, 24 Feb 2022 02:04:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 24 Feb 2022 02:04:14 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 24 Feb 2022 02:04:14 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Thu, 24 Feb 2022 02:04:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 24 Feb 2022 02:04:35 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 24 Feb 2022 02:04:36 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 24 Feb 2022 02:04:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Thu, 24 Feb 2022 02:04:55 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 24 Feb 2022 02:04:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 24 Feb 2022 02:04:56 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Thu, 24 Feb 2022 02:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Feb 2022 02:04:56 GMT
EXPOSE 3306 33060
# Thu, 24 Feb 2022 02:04:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5269884ada0dd8683c910050c7cf3a447be8fcb9f733519f759745b117b217cc`  
		Last Modified: Thu, 24 Feb 2022 01:16:17 GMT  
		Size: 48.3 MB (48331243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f788c506c6e5f4a4e107be34e9b6356c6c489484c46f88eae308550de07436bb`  
		Last Modified: Thu, 24 Feb 2022 02:05:33 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f7b4aa0ebbb65aa0bab43b9cd2f97d812202617a10243b927624fb54cbfe16`  
		Last Modified: Thu, 24 Feb 2022 02:05:31 GMT  
		Size: 930.2 KB (930230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90423e7e7fecfed89177a178f9d28778d36df940d5a54234849150e5ed20ce95`  
		Last Modified: Thu, 24 Feb 2022 02:05:31 GMT  
		Size: 2.7 MB (2667671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb82ffd9f493695f2e3c9fec1a7e40d3ceaabdcc081c3d1794a94cf27f5d93a`  
		Last Modified: Thu, 24 Feb 2022 02:05:31 GMT  
		Size: 2.7 KB (2663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c2dff4544e72402e3ef5137bec894d50c1504475d4cbf5dbd0f715fcd5ce50`  
		Last Modified: Thu, 24 Feb 2022 02:05:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be69a52a3f26204183bc525d0db65ae573faa1e5af6390af49903b17d744e5a1`  
		Last Modified: Thu, 24 Feb 2022 02:05:33 GMT  
		Size: 25.4 MB (25397238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5072b6a3aa35f9a183a2949a36dbb1adbb45b2c278b9a633c7b1af236cf1d79`  
		Last Modified: Thu, 24 Feb 2022 02:05:28 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e416428d3c99f9f999a4a42ff559213a190dcc22acbe8c9b9b39ef298cb5771`  
		Last Modified: Thu, 24 Feb 2022 02:05:38 GMT  
		Size: 46.3 MB (46315443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ce6ad18c57a7b5b81fa8e0250e26511d9d03e2e215847d2aa8827dc69fa2d`  
		Last Modified: Thu, 24 Feb 2022 02:05:28 GMT  
		Size: 5.0 KB (4953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
