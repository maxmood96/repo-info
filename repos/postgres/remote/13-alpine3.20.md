## `postgres:13-alpine3.20`

```console
$ docker pull postgres@sha256:1d5c8b1f0923d14640650f8eaf15ad2da442e8563f34c99431312541bb1ec887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `postgres:13-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:bc788b742ee18862382cc49593054bede4a0904c9fac6c51038197c4fba1b5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92716994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b717a994c289d69dd5e673c194f2e585a192d889b9fe30fff3eca511ef25ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV LANG=en_US.utf8
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_MAJOR=13
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=13.15
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 22 May 2024 20:39:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 May 2024 20:39:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 20:39:44 GMT
STOPSIGNAL SIGINT
# Wed, 22 May 2024 20:39:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 May 2024 20:39:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5271b407095cb288bb4318cf0883067303a8271fe697378b9d8dc9dd20bff72c`  
		Last Modified: Wed, 22 May 2024 23:59:29 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee693eaf4689a3fe3c5e2fffad4d3f0bbb90c466c3a049a1090aa538da23f0c`  
		Last Modified: Wed, 22 May 2024 23:59:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d6e86e7e4756480512188c2e6d3684d3b449dcaa80654252cb8161ec48022d`  
		Last Modified: Wed, 22 May 2024 23:59:31 GMT  
		Size: 89.1 MB (89078889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb1e66ea639ef4aa67113edafdb972eb8c0b11fe0b35e5b2efb7842ed53431d`  
		Last Modified: Wed, 22 May 2024 23:59:30 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6c24d149f5f0459582d672fb5ed618264f357f788a1908ce2b4f1a14f92d73`  
		Last Modified: Wed, 22 May 2024 23:59:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddc0406bb2dd637b280e008b627a64202857ad6d8a783e87f4a79a3ed1aca26`  
		Last Modified: Wed, 22 May 2024 23:59:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03315bd92398e55277e0125b0fd1102a4dd34d73e6a8b282de84a1712aaa11`  
		Last Modified: Wed, 22 May 2024 23:59:31 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bd70cabccf0aee1b5aa55b21b7e69d39421c8bff70b1998d4b1313acd7a9d7`  
		Last Modified: Wed, 22 May 2024 23:59:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:4efdccda9cf5fcaa3912a84da83ddd19ceeb0a133f7fa8a32d4cad1b50e4ea8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.6 KB (613605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263ada4caf6eb9adb06d1938fa5d9b7ef127efbb692ebcc6a12bfd729300cf7c`

```dockerfile
```

-	Layers:
	-	`sha256:8b1b7d394caf3b36f24614f29e50591049a967b1927e1cceb1753c7665ff4703`  
		Last Modified: Wed, 22 May 2024 23:59:30 GMT  
		Size: 576.4 KB (576355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2988edcce6172765269823b098181787445b116dce67b130d24e9a37567cd4`  
		Last Modified: Wed, 22 May 2024 23:59:30 GMT  
		Size: 37.2 KB (37250 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:7292ce3d6afadce1f05744b87d0dd3aba8ef550b28d775ae2e774b23bfce5d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91551010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea5de4c471ad22f0a513c5b4b8014c3cf51f82fbfbe47c8a550db4a3362c06b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV LANG=en_US.utf8
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_MAJOR=13
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=13.15
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 22 May 2024 20:39:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 May 2024 20:39:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 20:39:44 GMT
STOPSIGNAL SIGINT
# Wed, 22 May 2024 20:39:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 May 2024 20:39:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488c12f7241f8fc1619496d0d9d0cd195e25eff576860b2c2fc6ca7b1b2cd31a`  
		Last Modified: Thu, 23 May 2024 00:04:16 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c861b766de241bc0614704b27253da7792cf04d055bdac6cddc8c05b2f7b2f0`  
		Last Modified: Thu, 23 May 2024 00:04:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6f06553d0aad992011d8ffec8ebc95d2cf1c8ffeba2dffd34abf7974b1ba72`  
		Last Modified: Thu, 23 May 2024 00:14:06 GMT  
		Size: 88.2 MB (88169944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fd4a68a19e2d7c349282585473bd6b9eb03a8425a668dfdca05910e8033426`  
		Last Modified: Thu, 23 May 2024 00:14:03 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6cf316c2da573b51c6998f02957d2c15d729c81790797610c70b6ae33d5d0b`  
		Last Modified: Thu, 23 May 2024 00:14:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7115cb23c6b59b32f9ebda87e42e1d290ca2629175855fa34138fe485fd5a13`  
		Last Modified: Thu, 23 May 2024 00:14:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b633d0369ec9d2e3f18be8b4c6bf1e5bf670591c010bf8528a5aae8f4193c849`  
		Last Modified: Thu, 23 May 2024 00:14:04 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a832eada58fa6aef3e0918771653a90ed280e9604c55e62e965f211e237a77`  
		Last Modified: Thu, 23 May 2024 00:14:04 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:aa9d6a1e92f55fd1d048bfb37ead8ee9d6166437ea8d792f875b8bea9b2aa9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (37013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5685053f5d25e548390c1ae68f8118e0be84043ec822c3cb569fbf4cb61f55b7`

```dockerfile
```

-	Layers:
	-	`sha256:0088d4917940e7ef754065df334da61d2a9ffb984149a1840d6b628d78913523`  
		Last Modified: Thu, 23 May 2024 00:14:03 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:68eda1f42888278da7fd2250bef1b24d3631f1502876deca7bbae7c0ce0eb87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86031142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459ed84d75c84b1a1ea0e1e5585a039148c483defdb2c80ede84f992f064395f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV LANG=en_US.utf8
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_MAJOR=13
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=13.15
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 22 May 2024 20:39:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 May 2024 20:39:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 20:39:44 GMT
STOPSIGNAL SIGINT
# Wed, 22 May 2024 20:39:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 May 2024 20:39:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfcf42c43f866e18aaea8ebded327323f09b2078fcf795fdabccf5beba409ae`  
		Last Modified: Thu, 23 May 2024 00:47:46 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024165db62c15a8a795ac5b1220a322ad3720e5297b7e12d65df63ceb28b747f`  
		Last Modified: Thu, 23 May 2024 00:47:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecd693dfd4f6ac7d593348ac4158b16d569146e6987ef88402665b778887cbd`  
		Last Modified: Thu, 23 May 2024 01:12:40 GMT  
		Size: 82.9 MB (82921099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f314adccf91bfba5331225ff234b1539a8c4dae3ea0c1db01404335cd04b695`  
		Last Modified: Thu, 23 May 2024 01:12:38 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357db75a3ed78f60bdbf901041584ac98d7f0cb49929b768cf1fab52c182aa54`  
		Last Modified: Thu, 23 May 2024 01:12:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ec5942ccedc6634bdfd4ab14f1cdff60d4f99a5f1a24a77b3ad8b1ebd46034`  
		Last Modified: Thu, 23 May 2024 01:12:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14984b5205211cacb689e95808795128f4de19c9463d2a4151b6c8cebd22e25c`  
		Last Modified: Thu, 23 May 2024 01:12:39 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e736098d8ff1b888f6790405879e08a5a8a5838d947adfce93eb50f84a8ee`  
		Last Modified: Thu, 23 May 2024 01:12:39 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:1a1ec3d1ad5f98886ef853d5cb3f3ecf3cf6dc5c194cc85e60d3b3227d2a6916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.6 KB (613623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4130ce3f9c232898331d0aa3050667038c78c03a7f323483b3506434024a587f`

```dockerfile
```

-	Layers:
	-	`sha256:fce817b534e5f21b4db339755e605061037ed4eb006878cbb682282b59ad3459`  
		Last Modified: Thu, 23 May 2024 01:12:38 GMT  
		Size: 576.4 KB (576391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e980c493b67064525911808e2232222cab41084e61c511954a5413eed0762ee4`  
		Last Modified: Thu, 23 May 2024 01:12:38 GMT  
		Size: 37.2 KB (37232 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:69426781894af4d5edc9d13105cb98d8aa1d1e858491e4aa9a55b69101f3438d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98004399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2072efd7cb17a1fe944178ee89d73a555f5fc687624b007816e42219b3717a11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV LANG=en_US.utf8
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_MAJOR=13
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=13.15
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 22 May 2024 20:39:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 May 2024 20:39:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 20:39:44 GMT
STOPSIGNAL SIGINT
# Wed, 22 May 2024 20:39:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 May 2024 20:39:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676d4dc9edc56835f1bc4c2204961477719cd85dd8fe6c04b93ded53dc0aaa6c`  
		Last Modified: Wed, 22 May 2024 23:59:17 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266df942e3e71ffb8de184de1c8592b7c9244b2a2cbf1e7887a034554073e3d`  
		Last Modified: Wed, 22 May 2024 23:59:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ef01dbc25e4de9b71bfbdb2df7242baaf07579f8474fd1a0f31d0bfa2be41`  
		Last Modified: Wed, 22 May 2024 23:59:19 GMT  
		Size: 94.5 MB (94521203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47c7fa1ba2b71201d49f8de130f353e6590a92266e7ab2417712ab9d57b8e7a`  
		Last Modified: Wed, 22 May 2024 23:59:17 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96fecda07fee11325339ddd4a255f4afe19f55a74c351a1b5dbd947d085e436`  
		Last Modified: Wed, 22 May 2024 23:59:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076b7efc2ae1a6a60cbab0e78a8417552bb5cd6a786876834519e5a896375080`  
		Last Modified: Wed, 22 May 2024 23:59:17 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780558fc64d2670d9df18ce917b9124aba691a305868063ad56a965f615d4cc1`  
		Last Modified: Wed, 22 May 2024 23:59:18 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d24281f0c9290fe49e0f36f8c5ded102646c84f7768787152cbbc8538acfbd`  
		Last Modified: Wed, 22 May 2024 23:59:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:8ed2ee93aa201d2cfe84658f7f6f5406c0c6e8173acb08dcf5a14aec7e7f33e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 KB (613539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baae06e18b8a74f39e2d313cf6a5e8b2d6db628ad519fed3ee29ed12e65b58e9`

```dockerfile
```

-	Layers:
	-	`sha256:97137b3c850a4682f35ce005e04cc0dacf2c3fa9206598c9057700bbbfe4ec8d`  
		Last Modified: Wed, 22 May 2024 23:59:17 GMT  
		Size: 576.3 KB (576330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c299e0e5729cd2a8d1e40854b5a33e095056d0d2790bdcb7e27add8f5940bf14`  
		Last Modified: Wed, 22 May 2024 23:59:17 GMT  
		Size: 37.2 KB (37209 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:a3ea655c8d6701afcc262fec716ad6661df2f5f7f68707a5888c901df9ee83d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97189654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9770dd174d044257c626059fe5cfa8602108fcd3cf447b81578ba17f82ffa51a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV LANG=en_US.utf8
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_MAJOR=13
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=13.15
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 22 May 2024 20:39:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 May 2024 20:39:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 20:39:44 GMT
STOPSIGNAL SIGINT
# Wed, 22 May 2024 20:39:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 May 2024 20:39:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3b02b639f60b95c8bee42965fc2865ea862fb498bba9bb97d5948c11d6e061`  
		Last Modified: Thu, 23 May 2024 00:41:48 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc56b9f64c4f38953ead8536055652cb2059e7ade17f1f4541ab8b371fae904e`  
		Last Modified: Thu, 23 May 2024 00:41:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33012d07fd3689b6ff1f95038c3c13bc4533076a8a9ef8ced670bb6f2e1976b2`  
		Last Modified: Thu, 23 May 2024 00:51:14 GMT  
		Size: 93.6 MB (93603797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c803ca9dad9126d3e5f853e673820b8dc723d25da5b155d2473458b8a027eb`  
		Last Modified: Thu, 23 May 2024 00:51:10 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02058f52f63b0d0f5a9f6ee3f37d364a09a283c454c2e482a8f42008302ea6d7`  
		Last Modified: Thu, 23 May 2024 00:51:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a1224a08cc9a4d3ae129959adb48a3236e44835735546c0be6e3ca74706f6`  
		Last Modified: Thu, 23 May 2024 00:51:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea28b9d4d76658e4288e6f480c631bb09b50f5b49c28c2327db3fb718b35665`  
		Last Modified: Thu, 23 May 2024 00:51:11 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0331aa69ff2b15507be7e2d5c4fa2ebb5d891e0670f75b31b8b702e49a82db42`  
		Last Modified: Thu, 23 May 2024 00:51:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:27784d0e54000a690ec70bdb7cefb8419ea3c54edec68af704d33f4e77836504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.0 KB (610048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562aa4c521e5e79380507e63e295cea7f2c985d5e4736e54b09a36cf4b21664b`

```dockerfile
```

-	Layers:
	-	`sha256:2318bb6b4b4fbab853e80a80eb5061d4553a75248b001672a7fd577e70c4c2c1`  
		Last Modified: Thu, 23 May 2024 00:51:10 GMT  
		Size: 572.9 KB (572914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a023aa136d91efb131d7f33cadd6615971f745367a2f37b80a7ab4990b353f51`  
		Last Modified: Thu, 23 May 2024 00:51:10 GMT  
		Size: 37.1 KB (37134 bytes)  
		MIME: application/vnd.in-toto+json
