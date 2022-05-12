## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:0e5a4f3064c00a4b0a5ca90ad1aa805837f52633242b8c168d67607d207165b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:4d5e8763440bd8c7af3c68132796e201a8297d4d77df2c978e96c51678cb2c4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126910013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23eb9a154db6b6e6b0ba7c0a0f656d5741f848b3d2ac66af2bf6113d5ba1d209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 12 May 2022 20:58:56 GMT
ADD file:8ac79c33c3bdf8a0a1c23cc009fabc3ead9d97891d701ad21090a6bc542521e2 in / 
# Thu, 12 May 2022 20:58:56 GMT
CMD ["/bin/bash"]
# Thu, 12 May 2022 22:39:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 12 May 2022 22:39:33 GMT
ENV GOSU_VERSION=1.14
# Thu, 12 May 2022 22:39:36 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 12 May 2022 22:39:46 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 12 May 2022 22:39:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 12 May 2022 22:39:48 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 12 May 2022 22:39:48 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Thu, 12 May 2022 22:39:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 12 May 2022 22:40:02 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 12 May 2022 22:40:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 12 May 2022 22:40:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Thu, 12 May 2022 22:40:21 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 12 May 2022 22:40:21 GMT
VOLUME [/var/lib/mysql]
# Thu, 12 May 2022 22:40:22 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Thu, 12 May 2022 22:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 May 2022 22:40:22 GMT
EXPOSE 3306 33060
# Thu, 12 May 2022 22:40:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cd32cd816e68367704ec22e6e4d27af6a08b27e32aca3d0bd7a47424e37d0b91`  
		Last Modified: Thu, 12 May 2022 20:59:41 GMT  
		Size: 48.8 MB (48758049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1cac655dec3bbc6c5dd2efa9156e4798ca4cbb99f1311853f490d7092ba3ad`  
		Last Modified: Thu, 12 May 2022 22:41:03 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882efd5b0b9e419c5b8707b94c9916f62f166a427c37954da0aefc0f7c744ca0`  
		Last Modified: Thu, 12 May 2022 22:41:00 GMT  
		Size: 930.2 KB (930225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8424ed51a7a3d46b24a5876e22e1d42a033170139757b9b003be5da80d6c33a8`  
		Last Modified: Thu, 12 May 2022 22:41:01 GMT  
		Size: 3.8 MB (3761150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd7d8c8b2c6eb0293ce188c4627a483f57d6c6cd1409bee035ee58fbcd39f41`  
		Last Modified: Thu, 12 May 2022 22:40:59 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d485f7c40504fc4261d3b5cb62305b4f41a0507cb46e11c2c54b65a2ca6d39`  
		Last Modified: Thu, 12 May 2022 22:40:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15656ef8b782ab3e6234de4f2c4854115373be8ab28b59f9f014dbff120037af`  
		Last Modified: Thu, 12 May 2022 22:41:01 GMT  
		Size: 25.5 MB (25476162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3786d73cb960fecd724e6bcf500defd0e02cf03a7869863adb65266d025b909e`  
		Last Modified: Thu, 12 May 2022 22:40:57 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3f7291494d2e057d61cfdeff9c32d944d87bcc349fe31f2a79bf85be661461`  
		Last Modified: Thu, 12 May 2022 22:41:06 GMT  
		Size: 48.0 MB (47974917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2399c35146d1646f6f535235dfce69c437e13576fa19a283fdb340323b36fdfe`  
		Last Modified: Thu, 12 May 2022 22:40:57 GMT  
		Size: 5.1 KB (5139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
