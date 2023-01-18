## `mysql:latest`

```console
$ docker pull mysql@sha256:f451d12bbfe17bb9866b42a74c0df5898e1812260b2a95ad91d86c0e111fe5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:f287894fec0829612a3e921fbc849c0fb0f48356e0ade1e30a790e119274db61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151967668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6c84943bbf34dfa9ea6bd491ef95a049c41a6fc2a9ea0bc36134b1b093860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:21:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:21:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:22:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:22:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:22:23 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:06:08 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:06:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:06:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:06:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:06:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:07:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:07:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:18 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0296159747f12f208fbf9721970ca290348698ac443cf98311477b6e44f18acc`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2f9b664bd354b5b8823bbdda42cf0813f2d8d3b5693f952c0a8516af84a826`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6519f81c2689152b478834162cfe2f21ef37c472108a3e3a03a6ac0f5cbdd9`  
		Last Modified: Wed, 07 Dec 2022 02:25:24 GMT  
		Size: 4.6 MB (4608004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb5e56d458a7652c87ab8c3909c0ad098feaa81e73649bb37704701ca3ee6d`  
		Last Modified: Wed, 07 Dec 2022 02:25:23 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810ed59509062a1c771f01b920f00fca2b3a126e561355506188bdc924e65c0`  
		Last Modified: Tue, 17 Jan 2023 21:09:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d365517771ca199779a25f2faf5c1d75408f7e57cd0e6bdd34181b9ec720d`  
		Last Modified: Tue, 17 Jan 2023 21:09:53 GMT  
		Size: 56.2 MB (56220298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d785f9637b9cdede74b0f332edd33b652fe329dbba2ff0e27388af786fc23`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75755e293f40636019b4c1c800464f9e4969f3bbb0920be3f77c31b5c22796f4`  
		Last Modified: Tue, 17 Jan 2023 21:09:54 GMT  
		Size: 46.3 MB (46332108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b9182546d2f7832e16d2f174914a30f32048a2cb313a889e774bcaeb2f0c8`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0145b16e9f9ed8b2695da8098729f6337a67c57d2853d9edbcb4caab78b99`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8a7599f63dda9798f0eb1c6a4d813eebab2f8137a0fcc5ab97cadaa0bcffc42c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150880296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07039bb92a6f9fe85e7d50648e3d0bdab8504f1b25ceed88157bf3dd843fe009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:50:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:50:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:50:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:50:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:50:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:15:43 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:16:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:16:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:16:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:16:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:16:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:16:47 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:16:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:16:47 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:16:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec1cb1944f64443d61a29e94cddba36d0cb8a09c80e0247375445bc62b842e`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aede38c79379349fd3e9d191f92be36e68adc230840ae21c015f166b96e2067a`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b980849561d1ed6bffe5deb621498e150f4f0f148af7a2654dd90ed42d7bfb`  
		Last Modified: Wed, 07 Dec 2022 02:52:09 GMT  
		Size: 4.5 MB (4464908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f503d79ed4bc3c439b28068291b1260757ab2de86163c8954962d88ff917e22a`  
		Last Modified: Wed, 07 Dec 2022 02:52:08 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2b43a7e4bae0b356fff0c9bc14905bd8d305d062cb4ea5d1c2275a4c39273`  
		Last Modified: Tue, 17 Jan 2023 21:17:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c2bb95bebe3faba3509fb704207e81b5c81c2831256fa63f314d15a5e7513f`  
		Last Modified: Tue, 17 Jan 2023 21:17:13 GMT  
		Size: 55.6 MB (55610757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78004d73f3aef777892e3870fc76db5b6a7f7b33c313aedf7a6b873911d41c9`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871208cde4a40b9f8a4a07d620ac334441848d9ec993bd7fabc452cba1595116`  
		Last Modified: Tue, 17 Jan 2023 21:17:11 GMT  
		Size: 47.2 MB (47165727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ffd21fbf398e2c8ee0fdee514c745b169697ed03a5eeb632d6cd573b6de66`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2fd13901dca583f16c51f1a7d094bd0b629d231e5cc8b1781fdfd9e61c1e7`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
