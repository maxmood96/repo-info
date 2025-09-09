## `postgres:14-alpine3.21`

```console
$ docker pull postgres@sha256:d06dfab259e0a7b66d4675108ee79cc8951d55a62aa93683562f134001bff69e
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

### `postgres:14-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:d439d0e871e84c2847a79d9b671bda016369e5ba6f814790286f57ed6ad34d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108061915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fa8285e0f52178fbac7a06f2751ed960aa04887922f475d406b2d61a9c3b21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=14
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=14.19
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Mon, 08 Sep 2025 20:04:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcd59e1ab76a7b7a0500837298527127d7df8c0327a5fe0f64ff77bd4d8f1ef`  
		Last Modified: Mon, 08 Sep 2025 22:43:03 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ac6c9fb51f26c800ed69ca97f5b7082eb4267d1f7a3ec5023509deaeed7396`  
		Last Modified: Mon, 08 Sep 2025 22:43:03 GMT  
		Size: 914.8 KB (914817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c941f2c53488e9e9ff01ba6e2c097e63a856fbc1c951a2a1414bd7d326255b6`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8df9409616ac641c423c36efe48e109fb820b77ddb13dbd239cf8dbd5b80ce`  
		Last Modified: Mon, 08 Sep 2025 22:43:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d143c29520ce2cf152ecb4ef66b15e4e01ae87687eaf6752bc31c62a81dd75`  
		Last Modified: Mon, 08 Sep 2025 23:14:17 GMT  
		Size: 103.5 MB (103492667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654775b30c4ca794d26c90ec93776361cea37cb4d03f0549a2301dcdbda15db`  
		Last Modified: Mon, 08 Sep 2025 22:43:04 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f02af4e75ba6fea3272272bc1d7709f8bbea193b685fa2df5369115146cab`  
		Last Modified: Mon, 08 Sep 2025 22:38:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb9eebc2984d8c709f23bb66a7426bc4118bb2e2ed050653569add912008529`  
		Last Modified: Mon, 08 Sep 2025 22:38:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d4d2dcb270715abb57ac659140062209e5a86ff64ce3dbda5272a9bcd2848`  
		Last Modified: Mon, 08 Sep 2025 22:43:03 GMT  
		Size: 5.9 KB (5923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eba10f4f225af77469e5c2d9b15db5bf78932904f794e4c1d81a33148f1b250`  
		Last Modified: Mon, 08 Sep 2025 22:39:00 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:4d808d4c24405bba8be84f453b9bc9b43e022b821940898c36481c809d68e2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4384634afe9cb70d907a9a37e63075bd60b9ab4d28311aacf7de54cafb279b`

```dockerfile
```

-	Layers:
	-	`sha256:5137a86b0d280395f239527480b03990e1a389e6b9fd5c6e849c882e3ba405b0`  
		Last Modified: Mon, 08 Sep 2025 23:08:59 GMT  
		Size: 598.7 KB (598692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8933e242803f60ee9c5ad4b99d258eb4c5ad104066a66fe6b4fa57099990bb`  
		Last Modified: Mon, 08 Sep 2025 23:09:00 GMT  
		Size: 43.4 KB (43424 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:becf07c1f07a9d8cf1780ea77f4e63e3db4b20fccb2d0817af01a1cd7940cd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87888912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71d5169d65da1d67690bfa917da4cc3b8bd1a0faced04f1bc03db5f6b0399a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
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
	-	`sha256:bfc0d23853b14d2b9399ac8dba0e6d48c055329062ce04c1bef6754fe4b1360a`  
		Last Modified: Thu, 14 Aug 2025 18:58:04 GMT  
		Size: 83.4 MB (83424740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e80dc6bae177094d4e025f0b13434da56fb69db9f0ec4788b46e846cd1c297`  
		Last Modified: Thu, 14 Aug 2025 18:57:57 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ffa2155711b788114dbb76fa5a7b8684d660281c452f4de2f5f3548a862caa`  
		Last Modified: Thu, 14 Aug 2025 18:57:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d68b94ad0edc3d5c337ea2eba0c881eb85872518eaf458cb3b798f6b95463`  
		Last Modified: Thu, 14 Aug 2025 18:57:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5870744b5d915137387258c63bdc1d7f858ca1c61fc8829b66d96c794d392c2`  
		Last Modified: Thu, 14 Aug 2025 18:57:57 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7127aa78031b325608c388bee45a305077bb534d489f1a5cb09b0433bb12c6`  
		Last Modified: Thu, 14 Aug 2025 18:57:57 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:c2391ff99ce96d2f3314d8ba2a21d8ebb7ff601b3c96257ed9e07fa94c6115a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483e2fd7e06dab89dad76fc520d9235bb4ed0b95e1055d3a61a2348f28fee36b`

```dockerfile
```

-	Layers:
	-	`sha256:556adfbd5fdda3c016b1d36a8c45a0f6163b99d7557ae25c7ef75188a4057bee`  
		Last Modified: Thu, 14 Aug 2025 20:09:37 GMT  
		Size: 43.4 KB (43376 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ffb79203798cd386d984a95bcfb2203f60366bd99aeae893d479f765de985deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83141771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ce92984a4b852752182cf60f6ef4afe205df318bea1e1409ea58629fd30832`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2479436e58684e2eb112538b475b64df7a6f0cf622c2aca2d7639797003ee3b6`  
		Last Modified: Thu, 14 Aug 2025 18:55:36 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d6ea01dc2439d65ad9dee1318259d41e82100215755413d0040108baa9fa0`  
		Last Modified: Thu, 14 Aug 2025 18:55:36 GMT  
		Size: 1.1 MB (1083499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5e8ca01571f801604a91a356f4a79638d1a6336c1672944782dc73c9e1cc7d`  
		Last Modified: Thu, 14 Aug 2025 20:13:52 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8677a97a22961f3ee93622613e813b0d0803417ad6f01209358ebc161f892760`  
		Last Modified: Thu, 14 Aug 2025 20:13:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69972208c01d651139ed4314fadbfaa7cd2115e89305d9a7c352626fd1afb80e`  
		Last Modified: Thu, 14 Aug 2025 21:11:36 GMT  
		Size: 78.9 MB (78944525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9323d95fa8bfba0bceef30698a90490cb51e149e81e7eaa12e79842988bb0e`  
		Last Modified: Thu, 14 Aug 2025 21:11:12 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9324758bd5ff1423e45f5e5e519f774a68a2ef9df816e7128e987b688a022e2b`  
		Last Modified: Thu, 14 Aug 2025 21:11:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ccda956533b293667f22d5549259169d70024091f641787b7d7fe49476f560`  
		Last Modified: Thu, 14 Aug 2025 21:11:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec08220f2901039a091a2e7ccf8cb30b7c98d5cf22f777eaa3510dbd51107420`  
		Last Modified: Thu, 14 Aug 2025 21:11:13 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64246be794e80ee8fff92124f18d899816ad9e910732747def50a32f4e94e129`  
		Last Modified: Thu, 14 Aug 2025 21:11:13 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:50e29ed56e23b636d14249c804d34da895c5feae5b463150ca8efd195b5849f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041de27f885b9cc833acb6671a02bf3b90c75cb447c1ce089af704f9aeca3406`

```dockerfile
```

-	Layers:
	-	`sha256:fd7bab01b05407aa7922486b449a6dc32632f801b59ca48e4faf773563100ad1`  
		Last Modified: Thu, 14 Aug 2025 23:09:27 GMT  
		Size: 598.7 KB (598716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54eeb77bd3a31ada3e38f65410030a14f62d7bb5cc7360999e2c5662f1a86ff5`  
		Last Modified: Thu, 14 Aug 2025 23:09:28 GMT  
		Size: 43.6 KB (43591 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0ca94afcbd5fe1fd87722d01ddb99383ca1151a20b1e33057d1576c623fa9cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b5c17060271dcb15618305408ee72d0d88782225413515b7c2c29061921fec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
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
	-	`sha256:4650b4d73bfe6dfd050b3e00b603d30db3c16976f05dfe01b4a6f6768c013ebd`  
		Last Modified: Thu, 14 Aug 2025 19:27:48 GMT  
		Size: 99.1 MB (99110345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922fe9bdaa8ad7d1b06ecd8ac08f432e2c369f9d46859245f639169d26feca48`  
		Last Modified: Thu, 14 Aug 2025 19:27:32 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058f864b405ae15c2f44ae16ab7c3a465ef196bf061251d70b8a6339b84eca83`  
		Last Modified: Thu, 14 Aug 2025 19:27:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce5229f3756f8da7ea3e72a673f77dfb667ccff24aee0f0bfd0cd0511f7c297`  
		Last Modified: Thu, 14 Aug 2025 19:27:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859a67c4fae5a6699c05ced02987bc1e7ca3795db6d257dbfb5010d6c7768ab7`  
		Last Modified: Thu, 14 Aug 2025 19:27:32 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9798b5ad3b2b262be9bbe35e1ff160018b5a30845a724f5146aebc4b132776e2`  
		Last Modified: Thu, 14 Aug 2025 19:27:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:e29c01c32130c212ca4f24290966ac3705cb984bca6fec7e4c751bc7c16bc063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cce3e31aeb092053d10052c9a2139bff0f22472c386d91639afff8ce122cb2`

```dockerfile
```

-	Layers:
	-	`sha256:009ef738074a21ff19cb7e332b792e81ee8465f28b3f7c01158c696d1183f4ab`  
		Last Modified: Thu, 14 Aug 2025 20:10:27 GMT  
		Size: 598.7 KB (598728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdefd86319d07295b062bc9f54cad85389f8659de9b628180d799a17c5dc6749`  
		Last Modified: Thu, 14 Aug 2025 20:10:27 GMT  
		Size: 43.6 KB (43627 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:1405f780399c7d96ce1f8378f6eca727f8ba7c4fa4d740457ed41966a0d1ea56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114183360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e874770ecd7eadb9605c0699ab8d3187b792f65e94dc31860929ef56bb3b4df0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=14
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=14.19
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Mon, 08 Sep 2025 20:04:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19558c3367d559a61862a4d5f2ae2b887ef9222885b0595db31b70c295f5f157`  
		Last Modified: Mon, 08 Sep 2025 22:43:10 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88166db9ed809b8856506f995e02ba8fba309979015c2ae5d4db9497a8b6bd7`  
		Last Modified: Mon, 08 Sep 2025 22:43:10 GMT  
		Size: 885.2 KB (885175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc89429875dab8493dc7a0a30b32e0818da448b7deabf49fda2febdc18b280cf`  
		Last Modified: Mon, 08 Sep 2025 22:43:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aa11162452cc78099f67b333db3dcdbaf58b3aa5ccb964e758ef8202655e71`  
		Last Modified: Mon, 08 Sep 2025 22:08:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0dc01d95457bd706624c122c47087a40620ca9b87d6e8ec1b70067edd8f79`  
		Last Modified: Mon, 08 Sep 2025 23:14:32 GMT  
		Size: 109.8 MB (109820588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500011154f96eec6cfbe28b9822e33409de792cd351acb11e35dfd2a7e2c00a5`  
		Last Modified: Mon, 08 Sep 2025 22:43:09 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625fd222984a3866115afe812a6b2aebf79cdf7f2824c16831a6c81e55b23a57`  
		Last Modified: Mon, 08 Sep 2025 22:43:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aec0db621bb846f4b0d67bc6aab4245bd5f0feb9528e16e27ebcc8e646a61aa`  
		Last Modified: Mon, 08 Sep 2025 22:43:10 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9258cc320ea1923178025d744a7721828da5bbcff32958002c6f14ab453933ad`  
		Last Modified: Mon, 08 Sep 2025 22:43:13 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec85a096e6e55a553277799bcb4cca933f1684a210dbd40637eb23fb65ab96`  
		Last Modified: Mon, 08 Sep 2025 22:43:10 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:ca126742c7e54264c205a03d36f357d790950a7ecb4fe57bed5235644aeed109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea5f25153c936aee20b33f45f706aab96e1a57740860b91bd8c32d901ad1d97`

```dockerfile
```

-	Layers:
	-	`sha256:92f660bd8d7d2eb591732989ef1b05889144b9af05735ff091be274bfbb35d42`  
		Last Modified: Mon, 08 Sep 2025 23:09:13 GMT  
		Size: 598.7 KB (598677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d912ee5aa55857927d696c5f40c4420ffea660b8c789457e49cc440cf7f415a9`  
		Last Modified: Mon, 08 Sep 2025 23:09:14 GMT  
		Size: 43.4 KB (43386 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:a56a4dd17590552204cc49f1b8b4bb17c056f95bcf12103287805b13805ddf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91938206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1965f49d9bcee0c800c0c1fdc360b54bc8d360b24f810b5abf0fab92460204`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8dda28bfc0d36b2cb180c6fd3e6a4cd86ecd59274144d20796a06aa044d95c`  
		Last Modified: Thu, 14 Aug 2025 19:18:59 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ad6b1df0987d63949c70018c4fea86e55f4647d138d50f9d0d6b1a34a79140`  
		Last Modified: Thu, 14 Aug 2025 19:19:02 GMT  
		Size: 1.0 MB (1032144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1811f8ad9016fdae08bfba73eb5823d071995c3df0399e43c62da53c16d864`  
		Last Modified: Thu, 14 Aug 2025 19:32:29 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d7f33c27276d664ab88c3f78c3c3159c094409cf70f5db8b7b76e4faad699b`  
		Last Modified: Thu, 14 Aug 2025 19:32:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f894a96f26104c101aa336164be3e085603d9fa4d6d1aebf2c9a8b8e5a7d0ae6`  
		Last Modified: Thu, 14 Aug 2025 19:55:52 GMT  
		Size: 87.3 MB (87320056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04949c7721861bb3de6dd370d4e679ccf888c1b28352a5e51847631759e0358f`  
		Last Modified: Thu, 14 Aug 2025 19:55:33 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6e06770fd74380ef5a9c538b09802a4cc0137310622b5fcf4b592e2babc417`  
		Last Modified: Thu, 14 Aug 2025 19:55:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55b1a816ff000ac6852917e49bf11f98868bce6bf82ef2a022875a0512cd6e6`  
		Last Modified: Thu, 14 Aug 2025 19:55:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbfc0cb6855027f49da061b0e1e84ddfe8ffa6593fd8e84b004391eeb18bf24`  
		Last Modified: Thu, 14 Aug 2025 19:55:33 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e598bf2cecc11982a0587c39f9be89af7bd3ba63fbb22fc03884df5f21f06052`  
		Last Modified: Thu, 14 Aug 2025 19:55:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:8574997b101b2a7c8d655692cce116e58822d1c09121b24bbd4fb9e890220525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.6 KB (638580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fd466e32b5025a9b33ba1cdd657eb703ed280b7d44e25f92ac6ae83473e851`

```dockerfile
```

-	Layers:
	-	`sha256:444302c3b693e5dab186495b52d79ff6285aa26233255ed0c8dd649344fa5adb`  
		Last Modified: Thu, 14 Aug 2025 20:09:53 GMT  
		Size: 595.1 KB (595105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69e5cbe0ff3599eccbd74d541fa4103593faab258779808846c9fceb27b2157`  
		Last Modified: Thu, 14 Aug 2025 20:09:54 GMT  
		Size: 43.5 KB (43475 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:6b8e6d00642c90d534a083185ca1011eed1404e78b86418a1859606d050697ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108161715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3d004ca9a3071bcdc3942bfc2099755c111b26edb12aa5cc76493698e57bc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
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
	-	`sha256:99ff73cb83ff95cd3fe3390cca7fe98ead3af3f7eaab789fae97b8d74ceab76b`  
		Last Modified: Sat, 16 Aug 2025 18:10:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dc9ca0ae2804ca5f780b8c8c64a1f57a291a2fb246d2145e51b10e549dce8`  
		Last Modified: Sat, 16 Aug 2025 18:10:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460a3b785dd7519b57f14480445d542c5fc6295adef8dfca5d4b725b81f31b1f`  
		Last Modified: Sun, 17 Aug 2025 01:31:55 GMT  
		Size: 103.7 MB (103710332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bb0a9ab1496396879807d118e8df7333c9b89759fd11e3779714c96b28d9da`  
		Last Modified: Sun, 17 Aug 2025 01:31:47 GMT  
		Size: 9.2 KB (9212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3454b6720d5d05e96261cfcd2f51aa60df545f3298244690c58eab1328a329da`  
		Last Modified: Sun, 17 Aug 2025 01:31:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6c7467eaa74272055b72326297c59e97871c3ebac567ed71980a0ce9c2d6d1`  
		Last Modified: Sun, 17 Aug 2025 01:31:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cf3b9f03885a4175c9c740c6e79e850424cadb23d100e6eb7ae093588fed95`  
		Last Modified: Sun, 17 Aug 2025 01:31:47 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d75c9185cd3dbc1c2b3eb80076afd378f98c8872f4e2ea46aa9d5e83b41bc86`  
		Last Modified: Sun, 17 Aug 2025 01:31:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:a1a06600cd9c8d868c4c1b891bd0d26ad50b5239c4843e8ea14fd9997c8c2849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25ef039e289cb3d81a1ad1a846293ab2b8a160ae26fe7e4763770d22e2419ed`

```dockerfile
```

-	Layers:
	-	`sha256:82a470a0f5ec0afeb6298c62e421c4d289f9bce084eddc24540df386f26220fa`  
		Last Modified: Sun, 17 Aug 2025 02:08:03 GMT  
		Size: 596.8 KB (596763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e892cb16d659dbc21dc8f1d6d38de3ae78e8bf9df17ee63d4f7dc5a4cf8b5bc`  
		Last Modified: Sun, 17 Aug 2025 02:08:03 GMT  
		Size: 43.5 KB (43481 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:557094f85bae738942156728e6eb5e1624a7eef6dbccf29131d118f481241f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116827015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41df18dda76ebfac638be6076eb15f569f317abb253f71534eb0557074e90298`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf403390a37eed6f4bb75f6f5da24ef2cbbe8774ada82627e4d0e821092f247c`  
		Last Modified: Thu, 14 Aug 2025 19:27:54 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86202da6bb77005318244a960b1e8c704d587a448f1ca52331d1e81ccfa2b4d0`  
		Last Modified: Thu, 14 Aug 2025 19:27:54 GMT  
		Size: 1.1 MB (1081103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f874035dc8e0bdfe13d4565fe528274a63ad2b9ae6d16df5918abd6a2b4e521`  
		Last Modified: Thu, 14 Aug 2025 21:14:09 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee52d05cc2214a16d5d2a764d203277b34907a271da9644c99dcf76911703a`  
		Last Modified: Thu, 14 Aug 2025 21:14:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a230314d5df0c31a268fdf122e30bb8481f08ceb5a1f334cb3f9dccf5be270`  
		Last Modified: Thu, 14 Aug 2025 22:31:18 GMT  
		Size: 112.3 MB (112266924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3652e62d1d64e9afc4ee3809a0cb9226171950ca222c30f732751d6b9bdb730d`  
		Last Modified: Thu, 14 Aug 2025 22:30:58 GMT  
		Size: 9.2 KB (9211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9101b017c232e80ff6ee5ac9297a50352ede4a43a4b1b76eec6fca872eeb85e7`  
		Last Modified: Thu, 14 Aug 2025 22:30:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5883e832ffa891222b1cb04464e97ac3829cfd451dd9c895db9938f949b79fff`  
		Last Modified: Thu, 14 Aug 2025 22:30:58 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4473bd5348dbb78c4f55d9a7912665e1bad97368fad998254d6692e2d8aefb`  
		Last Modified: Thu, 14 Aug 2025 22:30:59 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a71307f83b179b230dcfd5b98bb23a699992aecffe6b1a3718125ae1594316`  
		Last Modified: Thu, 14 Aug 2025 22:30:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:f0d72c0d2a2ada69adfcef54386e46f0f2b612ebfb7d0f2a04ad77a63ea539e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4687ac1f7a9c1d234e64bc00a4067a493748f3345ecc764fbf28a8c95dc75da`

```dockerfile
```

-	Layers:
	-	`sha256:52fce35811cbdd0abb94454fe6e679d1a0c85febbc6f76d334dc06b268784d63`  
		Last Modified: Thu, 14 Aug 2025 23:09:40 GMT  
		Size: 596.7 KB (596745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e069f20489e073ff04586745f612343ec5b97ef39644d707ee5dab76e696d9`  
		Last Modified: Thu, 14 Aug 2025 23:09:41 GMT  
		Size: 43.4 KB (43433 bytes)  
		MIME: application/vnd.in-toto+json
