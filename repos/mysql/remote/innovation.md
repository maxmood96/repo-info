## `mysql:innovation`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json
