## `mysql:innovation`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json
