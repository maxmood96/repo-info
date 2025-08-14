## `postgres:13-alpine3.21`

```console
$ docker pull postgres@sha256:46ffd6576f57b34b7949f153f7efc452d9a4847ab40e01ccd3c623741971eca9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:13-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:7184e4c5a5bc1db15dbdc8236cee877b1539008d7e73444aa0e4392fd9b64abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106926888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151061f036dd2f4b5e03c395f507c0167db375fe567f5fcdaf21c8f50ea88a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Thu, 14 Aug 2025 16:07:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fc4fa2ca7089f04b201ec4715a9f858f751fc16ee83dc09463304d56860419`  
		Last Modified: Thu, 14 Aug 2025 18:23:59 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4d8315be60b8e81151452e5b71a7b93964f5ce5c40c6a05c8405a1e2f2a9dd`  
		Last Modified: Thu, 14 Aug 2025 18:23:59 GMT  
		Size: 1.1 MB (1115526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e7e313f646b6cd60ffaedd13569d950ddde0837fb99cd5de5f11b658c34292`  
		Last Modified: Thu, 14 Aug 2025 18:23:59 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106bfcc855f141e1a4bdea8df780546ae62646a5613a5096949af2e394527534`  
		Last Modified: Thu, 14 Aug 2025 18:23:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe0df9050303446eb8f8a9b8d3b3107d1f09ca0f44fb4b3860f4ca30b47d4a`  
		Last Modified: Thu, 14 Aug 2025 20:12:00 GMT  
		Size: 102.2 MB (102157106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3cb66b39f18cc311176e4cf53ff7914e5461fb8a295295ec3e23a297ae4f56`  
		Last Modified: Thu, 14 Aug 2025 18:24:00 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7074591e7b9a0a414e3f564637af4703fe61e71500159333156ae8cd4d5d60`  
		Last Modified: Thu, 14 Aug 2025 18:24:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb574b376a9e2a1aa3ed5e39eac78d763d8dbdbe324b0474acac04da70e56fa`  
		Last Modified: Thu, 14 Aug 2025 18:24:00 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583547c90c7b98c43337c4a5b7b04a7d4c8f0de05ba6f1bf487d3b9b947b3e24`  
		Last Modified: Thu, 14 Aug 2025 18:24:01 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ada0782318710baf82265ccca602a91ac27f1e1d39279f1d7890dcc7f065dc`  
		Last Modified: Thu, 14 Aug 2025 18:24:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:3a32941bf3617a334cbab0a1be849232f267dc4649961c301b3bec7b091299a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.7 KB (638709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ce51940a3a35c9673c346a65b13bf8929b7b1ab8c661556a487f261a70505d`

```dockerfile
```

-	Layers:
	-	`sha256:270e686d1c2b03138043ee959c5dfa6f0f3f720d87e495403d45ca84f4832cfc`  
		Last Modified: Thu, 14 Aug 2025 20:07:54 GMT  
		Size: 595.6 KB (595561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:765e8db00bf4ede7ea72f21c9c62d0dddffcb9148ba4001b23712f71e5ccbf36`  
		Last Modified: Thu, 14 Aug 2025 20:07:55 GMT  
		Size: 43.1 KB (43148 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:ad6034c64ac39fac6cf4626f7dce804d2d3c935551779270ef15d4fe73abe219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86586242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ce0890864e61befc717077c70c36a831fbe67534ea2e45b17b851134486b86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Thu, 14 Aug 2025 16:07:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c24d3e045a6ae3a2737e134a0660bb67966f1c4c59f473117ca5bfb7f462df`  
		Last Modified: Tue, 15 Jul 2025 22:03:20 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85a4c1614afc683eca7c5ab777456f2ae53dd7e1347e7e75764a6a74abf3b8b`  
		Last Modified: Tue, 15 Jul 2025 22:03:21 GMT  
		Size: 1.1 MB (1083487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0535ca87f130f01bd91aa140a599a3b6ee5d8f43b88e249c7c036a020c97a1`  
		Last Modified: Tue, 15 Jul 2025 22:20:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a590464760964dee563efddc9e8fba7d79df0dc36493bcf3cf136c63fbf94eca`  
		Last Modified: Tue, 15 Jul 2025 22:20:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6d977a81757a53f8b22ac896ded341ddb728527ce051630f89179f98298a34`  
		Last Modified: Thu, 14 Aug 2025 19:04:58 GMT  
		Size: 82.1 MB (82122258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291c6beec2cbb492956646da611eefacba8cc9e8c9252538afead07d70b166ac`  
		Last Modified: Thu, 14 Aug 2025 19:04:49 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a616c01a382727553e19397b96e2f2d48948aa8238390a5f554feb7afab624ef`  
		Last Modified: Thu, 14 Aug 2025 19:04:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1b4fd0fd9e89c52a85ec1cf214218325964ab76ba0ec3d67610136135fbf0c`  
		Last Modified: Thu, 14 Aug 2025 19:04:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7bba39b7e46f8e09c522ccd9239d3ca255afdb28ffe33f10e5fbd350289ab2`  
		Last Modified: Thu, 14 Aug 2025 19:04:49 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6672a8928bb1fbed7305a962ec4b4641543073796f25b2b2cb21f6018c004ed4`  
		Last Modified: Thu, 14 Aug 2025 19:04:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:fcc74e0d217b4968fc666cd76a07d193f2fd550ec9d8bd2fac0f019220aa534f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 KB (43090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b075f1775b3795af3ae643dfa2f1ad1c6740483464dd862861f264e0980b504c`

```dockerfile
```

-	Layers:
	-	`sha256:1394cc19e08be74ddb76c490edc5ea277a039e4e723ff224d122f15b1c7f639a`  
		Last Modified: Thu, 14 Aug 2025 20:07:59 GMT  
		Size: 43.1 KB (43090 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1a2de64c35e9d3bc47e56038abd976fafda9ecd01011a9170cfba21a04640f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81872879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0db866b0cbba0df7c8fdb582a1169f2d8da813993e519eed3a57c77aa4dd151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Jun 2025 18:27:47 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["/bin/sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV LANG=en_US.utf8
# Fri, 06 Jun 2025 18:27:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_MAJOR=13
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_VERSION=13.21
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Fri, 06 Jun 2025 18:27:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Jun 2025 18:27:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jun 2025 18:27:47 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f3486cf29d0276b4ac8fbb65b102ab22ae5618fb042837b80f87e637b02102`  
		Last Modified: Tue, 15 Jul 2025 21:48:42 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e280f6d7d0584205565e6b71ba0d85887f9a443bdeb5686d452b8c7e204d5be4`  
		Last Modified: Tue, 15 Jul 2025 21:48:43 GMT  
		Size: 1.1 MB (1083488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fb28f5b006def17f8ecd81a69d69c91ae8956810d98732d5b50a1dd609916d`  
		Last Modified: Tue, 15 Jul 2025 22:05:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2a6075ee206ff91d1b258f59ee3dec1834d46f4da114bf543a980c7d57e1c8`  
		Last Modified: Tue, 15 Jul 2025 22:05:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d6d0ae33b26c14eba289c30ef859c1f4a471b702f2530a0a888f9a3ba588`  
		Last Modified: Tue, 15 Jul 2025 22:29:04 GMT  
		Size: 77.7 MB (77675838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a7005be0497cb31d9053cd93b4e6612a9f48c10077b40f1ac634f1b8634489`  
		Last Modified: Tue, 15 Jul 2025 22:28:58 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543cbb00e6e6fdfb2c3daaca1a888c040535b7ff5751bc8c65f097fe54d435e2`  
		Last Modified: Tue, 15 Jul 2025 22:28:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfd2e54af52ee3b153dcd85e61ac0647e2148849d429e41ece24af1e938de87`  
		Last Modified: Tue, 15 Jul 2025 22:28:58 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282d7a221c7a1253b4b386b2361d42b5e717f25fa17fe61f40d3aa220edda89`  
		Last Modified: Tue, 15 Jul 2025 22:28:58 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e33bf46d3916cfe49ea2a79dd06d705f21b63f55f04ccac0bbbcdd71f3e8b`  
		Last Modified: Tue, 15 Jul 2025 22:28:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:4b65de78789d77e94b844045e97592e9b71e202d943101407e3bdb1c9ced11e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae14be0c3e630f6e4918e01f8b6380ea579d22f333f09239610891437422780`

```dockerfile
```

-	Layers:
	-	`sha256:da1a6093c0972966fdf04c43274b43393b4437c2fd3b0d8a3d1239db8ff2eacf`  
		Last Modified: Wed, 16 Jul 2025 02:08:12 GMT  
		Size: 595.6 KB (595581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d23c7ce33d4edcea5658e77868beb67a1173fd601e77d911b237d8671c277fe6`  
		Last Modified: Wed, 16 Jul 2025 02:08:13 GMT  
		Size: 43.3 KB (43305 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:fc7224483d867ec546d84725d9fd9d218bc27a8d8b12e03e11e8013709cee302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102825442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7b9736070a1be60f0dbecbe1cf0dae445f076eb0e5f1ca5b212f4ace7b7e20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Thu, 14 Aug 2025 16:07:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0500e99ece82743454c50a08c0096387587592b762bcd82bde615671de2024a9`  
		Last Modified: Thu, 14 Aug 2025 18:57:34 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e8c3ce0b2d4fdb59659874d9a5099fdfb9996a16960ffb02ad370697f0ff35`  
		Last Modified: Thu, 14 Aug 2025 18:57:34 GMT  
		Size: 1.0 MB (1042486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1955b6a04ed68235e0d981512a3832f5113738d70fa2ed45a1b135161226e7b0`  
		Last Modified: Thu, 14 Aug 2025 19:12:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ef4a1f173221a39b19f0de13e787160a010a523f5c3222607bce9aa06a3bc4`  
		Last Modified: Thu, 14 Aug 2025 19:12:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42191588b5f1f0875dd128823b7501782ce72da68df92887f70bb4277afbd286`  
		Last Modified: Thu, 14 Aug 2025 19:34:31 GMT  
		Size: 97.8 MB (97779332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd596f5d5b69d76ba52538c4d10c0a6326f4c76e468d0be84b4866006d77998e`  
		Last Modified: Thu, 14 Aug 2025 19:34:18 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ef4cc23191e047eea04ed9d669400538d94873103d9c566abf79a35c4bc06`  
		Last Modified: Thu, 14 Aug 2025 19:34:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457e12e9eff43fe6354277911b98244843246486de16734d9b5e2cbdc8799fcb`  
		Last Modified: Thu, 14 Aug 2025 19:34:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba8d7534429027006287ab8434d211da47f746ea60cb5e44d9e5e642a914db`  
		Last Modified: Thu, 14 Aug 2025 19:34:18 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f2caa1cf583045e8407419a30e51ac3f773eecd2f77b2b01f353829e1d1186`  
		Last Modified: Thu, 14 Aug 2025 19:34:18 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:ce6ce6008df7463265aaf1fb71e46a7d490b6cc33245533280623f864d4009a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77179d07b163e1c8ce6a5d0e0ebe1eecb74537c53d51396ef7e8a635fa0c92f2`

```dockerfile
```

-	Layers:
	-	`sha256:4f6b4a107b7d85065556207a2e1dbd687625c79ed031c4bdaf2eaafe6c9cc486`  
		Last Modified: Thu, 14 Aug 2025 20:13:38 GMT  
		Size: 595.6 KB (595593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a677073e79a31edae2abc3e212e5afc32509e16576a6b8c9f2c8a5a3f4a3db3a`  
		Last Modified: Thu, 14 Aug 2025 20:13:39 GMT  
		Size: 43.3 KB (43342 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:f62162258814649edc4c9d8a127bc58a4999720bdb3734bfe452f328a5bf4829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113025754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c849fd7f36e5b9e51ac85b5dde425ff40a9e719f57d8e2fccd321d0ece94f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Thu, 14 Aug 2025 16:07:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d90c5713da92995ff3893d42ee0b87d4be35f5fde866923cc996fe47897f85d`  
		Last Modified: Thu, 14 Aug 2025 21:04:57 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913a34e64629bd899c2df98529236cd4eaa98e7e148dcc182e8bcd3357de6ee`  
		Last Modified: Thu, 14 Aug 2025 21:04:57 GMT  
		Size: 1.1 MB (1091455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ec6eb7d4ffdc4e099216c05083a4adbcf7ba11e96924f4548e70ac15b02731`  
		Last Modified: Thu, 14 Aug 2025 21:04:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c27868070f0aa5ed6dc4a94e747eca21524fd8dde7d09e03e755020754ad0a9`  
		Last Modified: Thu, 14 Aug 2025 18:20:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa13e8f143f030966844caf715937427392460ed9c60476918a52d257c59398`  
		Last Modified: Thu, 14 Aug 2025 21:05:03 GMT  
		Size: 108.5 MB (108456889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc781916058b50901a3f394557b6bd1264709b8b2fc8a520c5f9670b0077141`  
		Last Modified: Thu, 14 Aug 2025 21:04:58 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad76e23d223f6317a9d233e4a43f80b1237a6316dfd8b28a7c7c7ab48f9c0e0d`  
		Last Modified: Thu, 14 Aug 2025 21:04:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4a9d1b7ebf980d20990e6cb86dff6e63056a912410d7799c8df404bb97285b`  
		Last Modified: Thu, 14 Aug 2025 21:04:58 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164aee9fdf0e8723f97acd4ec3a1cb7c50261e92744d4ef3f5c29bac7afc54d7`  
		Last Modified: Thu, 14 Aug 2025 21:04:59 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6a874b6c452ccebf921b71f9d458566d22d8fae9c9e4459728687bb1484973`  
		Last Modified: Thu, 14 Aug 2025 21:04:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:69af85cc034ef6aa576b5b3d2fc5a7952f44e63582c973f5f90da56d9330cfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.7 KB (638655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919bcade189fcaae2612f05232eed9dcc9911f302e9ecf71f4276e5197849659`

```dockerfile
```

-	Layers:
	-	`sha256:803d21dfd4a1e88391be4a552849aeb381078d8f50cac1bea2ef3225153cc1c2`  
		Last Modified: Thu, 14 Aug 2025 20:08:10 GMT  
		Size: 595.5 KB (595546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f19be92b30e41872cb8a4c4e8158da63ec1e3c46807475066b2e2ed773fd5b25`  
		Last Modified: Thu, 14 Aug 2025 20:08:11 GMT  
		Size: 43.1 KB (43109 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:a77f8b875ef17668c48a29195839dc56a21d5154c0a1ad1290a2dde099dc811b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90460847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1aa7b27de3132e5efc9e1485b4b35eb6d2daf2654f2df207b6f00706358cff5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Jun 2025 18:27:47 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["/bin/sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV LANG=en_US.utf8
# Fri, 06 Jun 2025 18:27:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_MAJOR=13
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_VERSION=13.21
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Fri, 06 Jun 2025 18:27:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Jun 2025 18:27:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jun 2025 18:27:47 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d150f0e5a84464f51b24b96104e9c461f6aa57b0d596b53a3b61d1828eb167ed`  
		Last Modified: Tue, 15 Jul 2025 21:49:56 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559507c038b9e2c6c1217225ede50c505cf2e95ec527aef9412ee27ad0a229df`  
		Last Modified: Tue, 15 Jul 2025 21:49:57 GMT  
		Size: 1.0 MB (1032134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86585882e1d45c093f8c658d5be147b9d7c184e5b77a6a270ed0b036c5cee58`  
		Last Modified: Tue, 15 Jul 2025 22:08:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46622dd8b9c47a1d1c9474038023c96aaf9165949835dc3d6bc15936e2bcbb1`  
		Last Modified: Tue, 15 Jul 2025 22:08:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bc18e61921305f971d42acd6dbc67baf61fa6e132f698e13fafea137f1c4c8`  
		Last Modified: Tue, 15 Jul 2025 22:30:19 GMT  
		Size: 85.8 MB (85842897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228f6c6391f08f830e19aa305c529e6992ce23b4dae0023cc944376d57dc91a`  
		Last Modified: Tue, 15 Jul 2025 22:29:51 GMT  
		Size: 9.0 KB (9019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a2eb0088faa9a56b8b8087063353f6fb6992f8e22e3a217cc45c62366683f`  
		Last Modified: Tue, 15 Jul 2025 22:29:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b72885a1e1db4b3b9fce4076d1703478f084af3bc6cf5413b50dab6fbdd427`  
		Last Modified: Tue, 15 Jul 2025 22:29:51 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae08c98221cc2de813b5090666d79e77d2723ed9502997fde558c1f239e66cc4`  
		Last Modified: Tue, 15 Jul 2025 22:29:51 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4157554893bbacf794d49355dbad3499232e5f013f365dfc6db929764fa5e231`  
		Last Modified: Tue, 15 Jul 2025 22:29:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:6458c77b1c87f263fd6ff07d87a3a7c14658b71021e2f43330f09a55855d0469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 KB (635160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee63cdd750eacf86ec476c59b0f2a02b4c7964174e02494766c37db9a0b3bf16`

```dockerfile
```

-	Layers:
	-	`sha256:789deeee8b70de6161ea10e22f7a70cb495ee560bcc53e3f7e250f96037f10b3`  
		Last Modified: Wed, 16 Jul 2025 02:08:23 GMT  
		Size: 592.0 KB (591970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c040813001ede1983ce0c6d5d29b727b6248738027ef7fd8b9bd3e994cc94bdd`  
		Last Modified: Wed, 16 Jul 2025 02:08:24 GMT  
		Size: 43.2 KB (43190 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:5ab0530a102ba1a7f77f7549b0b8cdad67cd0eaabc55e56093de7e9fdfb3874e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106362648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b9f84247414d6361e67671501940bb31db03bffe79e5a52f244cac80e5ebdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Jun 2025 18:27:47 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["/bin/sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV LANG=en_US.utf8
# Fri, 06 Jun 2025 18:27:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_MAJOR=13
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_VERSION=13.21
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Fri, 06 Jun 2025 18:27:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Jun 2025 18:27:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jun 2025 18:27:47 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d3c0f56503ab40c4140d482406fc770090c1cfa210c2d815c27c3258a8846`  
		Last Modified: Thu, 17 Jul 2025 05:47:43 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff15b55dbea7fde51e6fef1d6c983e6787f061f6e664e60be0bed1e73ab2ba1`  
		Last Modified: Thu, 17 Jul 2025 05:47:44 GMT  
		Size: 1.1 MB (1085403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c75913cbc26940254112728bd4519792604d59b87d57d1b6a516b5f3203015`  
		Last Modified: Thu, 17 Jul 2025 09:23:46 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b89ec7c8499297647a2732eec0bdb3c4565a294b6c8fa401cb6602bab03a5`  
		Last Modified: Thu, 17 Jul 2025 09:23:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d0c04f0f68f1838f87d04787698c037a93767255818abe9382af38465f560d`  
		Last Modified: Thu, 17 Jul 2025 14:20:16 GMT  
		Size: 101.9 MB (101911454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bcfb8603bdb72fcd2451bc42f5029095871616a5a36135ca9a0b1bfb8df88a`  
		Last Modified: Thu, 17 Jul 2025 14:20:09 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4e73594aaf85e8b1564835f1be3996f8b900317d7366ea566cfbd1263480e0`  
		Last Modified: Thu, 17 Jul 2025 14:20:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f9dd0483ca993a28694d27977457c92d613780801513fa6a9b4b0c15fc163`  
		Last Modified: Thu, 17 Jul 2025 14:20:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a028ad564029b840abf522f321980d993c48b9541b90197511565bc2293b52`  
		Last Modified: Thu, 17 Jul 2025 14:20:09 GMT  
		Size: 5.9 KB (5932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58f2671a2e30f526e62b71a39269d3a83e19b3853a4083b8ce535716627c65`  
		Last Modified: Thu, 17 Jul 2025 14:20:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:5ea686bc8e66ad0976e9ae389c3d3b4c7aece2e39ccd80eb44b08ae72c4f76cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12487939b2a4d49eda8920223f64d6298b55f09283a159ec987858b367b5b2a3`

```dockerfile
```

-	Layers:
	-	`sha256:39eec56653413317a7fda473c4ea313c958784b1291945366cc37482eb83a369`  
		Last Modified: Thu, 17 Jul 2025 17:07:43 GMT  
		Size: 593.6 KB (593628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baede6ea9ee575428d3cda340d61b599172a476aeb9ba5fd318e16ab1d111fb`  
		Last Modified: Thu, 17 Jul 2025 17:07:44 GMT  
		Size: 43.2 KB (43196 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:f8fb319cf433a1669ad4516860377af3a4221b6840df385488eba9dd17aa5717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115363320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d152fb57a329d7475f3692138061e461b6694e73983f4c1b00e978a4afeb75d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Jun 2025 18:27:47 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["/bin/sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV LANG=en_US.utf8
# Fri, 06 Jun 2025 18:27:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_MAJOR=13
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_VERSION=13.21
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_SHA256=dcda1294df45f033b0656cf7a8e4afbbc624c25e1b144aec79530f74d7ef4ab4
# Fri, 06 Jun 2025 18:27:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Jun 2025 18:27:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jun 2025 18:27:47 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08ce6f43a6a5f10e7f4be1ad3b21d953126a6a3fadf3e2748946ca632e9cccb`  
		Last Modified: Tue, 15 Jul 2025 22:02:49 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405b45240bca888a7a97d0169873d3fe563c9899d16570f76b85d85bb758d59f`  
		Last Modified: Tue, 15 Jul 2025 22:02:49 GMT  
		Size: 1.1 MB (1081100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7523b5868d4d92fc8ae8806c0f90a18733af8ceeea6964a3c024ad8c9ffa363`  
		Last Modified: Tue, 15 Jul 2025 22:15:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868f0e6a9e7859a6484717f524b199aca136527776655f1b5a5516413c07ebae`  
		Last Modified: Tue, 15 Jul 2025 22:15:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbc0ad9418a2cf860c50113eb13818a0d1bdf919491d2575694d5a3d70e13a7`  
		Last Modified: Tue, 15 Jul 2025 22:38:13 GMT  
		Size: 110.8 MB (110803443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17731b02af8e2f62a75bf3410b9f3c5bc1b583c76c9de3674364661096ec8174`  
		Last Modified: Tue, 15 Jul 2025 22:38:06 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15466a0fa48ba4df964596cefdb44fb340e854f3e8b6f611e89932ba6853a26`  
		Last Modified: Tue, 15 Jul 2025 22:38:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441cdd6c1c4b114ebbdeab6330b53b62a8e8afc1356d972ea6c2beb540cd52f3`  
		Last Modified: Tue, 15 Jul 2025 22:38:06 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e077500e87dd4dfacd704e7be64d877e030fa562aabe2631913904e91f077c`  
		Last Modified: Tue, 15 Jul 2025 22:38:06 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d158e19e24a5ca7eab4a2ebb6b1d410983a04362fd3767c3b734b643c7e14bc`  
		Last Modified: Tue, 15 Jul 2025 22:38:06 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:cbb5092a1cd3018de81cd9891cd9066c6cecb045aef966b0e4d207b4d8c44a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d69b6b4cdee9d98d850bfe20997ac92a7d1237e5bf8e33caab9a835d6885eaf`

```dockerfile
```

-	Layers:
	-	`sha256:3e439391ecb4d3ac2c8397881ae5d942e514c9b46b02931629cedcace77dd96f`  
		Last Modified: Wed, 16 Jul 2025 02:08:29 GMT  
		Size: 593.6 KB (593610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869ace62abce5abee742eac5aebe07b422be54a7f23b475a730c61927595cec6`  
		Last Modified: Wed, 16 Jul 2025 02:08:30 GMT  
		Size: 43.1 KB (43148 bytes)  
		MIME: application/vnd.in-toto+json
