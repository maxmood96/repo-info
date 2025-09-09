## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
