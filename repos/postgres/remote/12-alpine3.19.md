## `postgres:12-alpine3.19`

```console
$ docker pull postgres@sha256:0083aacd5fa18e147d304a3cf3cd327c48b8e9488b2a02292a26f9d23c9bb818
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `postgres:12-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:ece0a8e07cb9de19e4054d5838c4cbe10135e7f6cb2050dad3df23a619573bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91972295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2247d3e23c5ab2170037bdef05553e8d2f2a2b78dca7e0f40e2208a6d25221`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c769d8d77aec50e12b081f78b4bc613dbbe60bd253f9d58af69ef2382d04e1ca`  
		Last Modified: Sat, 16 Mar 2024 00:00:23 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b0ca72b17d95b50af23cdd688e43a4dc0adff2dec07af68c11e834ccbffef7`  
		Last Modified: Sat, 16 Mar 2024 00:00:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da40a38e5aab75338a9c1fc768bf36db9423f0f60810bfb4bea028085a3a785`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 88.5 MB (88547596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd41d8466042eac8789503054fe9bb1b24b3157f58d53a9f46d64cf2ce508c3c`  
		Last Modified: Sat, 16 Mar 2024 00:00:23 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6866d4a6f5d7755e7d448eb846421df0b84ead62ce4e4cda45034de5ec20b275`  
		Last Modified: Sat, 16 Mar 2024 00:00:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2922012aa8756a2abf3597c66b6a8d270085872147313dcad481a936264def2c`  
		Last Modified: Sat, 16 Mar 2024 00:00:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d974fc96381a9d34cbee926b342749ea977d92e34faae725f3e350941adf08`  
		Last Modified: Sat, 16 Mar 2024 00:00:24 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc9c6d608c1650db07cf4a15eb010a2c43465f8e2907a8b452c6d0384660823`  
		Last Modified: Sat, 16 Mar 2024 00:00:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:f4f982c0bd4eb50a8e795c9a1679bb5c04d26d2360f6ab235b45d23a526368f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.9 KB (991905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ea9e9895d4f6a56e808c403cd04bf687f01ffbd2cf552b65c871ffdc0ea303`

```dockerfile
```

-	Layers:
	-	`sha256:51879283b59bbf7550f29b1852895bf1ce682355930eac74c558708b7b0b3642`  
		Last Modified: Sat, 16 Mar 2024 00:00:24 GMT  
		Size: 954.7 KB (954651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ca7c771f93b879035b00e696aa4217e4290dc2bea912ff3e963072c8f266da`  
		Last Modified: Sat, 16 Mar 2024 00:00:23 GMT  
		Size: 37.3 KB (37254 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:1c99f5986d2ecbecc8c7fd90113c6f2f32e962d71647f86fea394d518a8b7680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92619148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d154a33bbc1537e45d2f3d6ad2ab9b99b9acb87e8365b9e74d76dea4956277b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Thu, 09 May 2024 18:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b675d45afe983b29c7135f33138e534ba9aca9ca6d05d28e546e09d1e6bba8`  
		Last Modified: Thu, 09 May 2024 21:59:43 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4f6c09ac2d383e82b8fba12dd71c915fd20ddea25bd838ee27c29df1a0982d`  
		Last Modified: Thu, 09 May 2024 21:59:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ccf046d5309afd198d41c01bf756f744bf3022b453358cce769eb070cff97c`  
		Last Modified: Thu, 09 May 2024 22:26:13 GMT  
		Size: 89.4 MB (89437783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682aa7e26954d58bb6c85b7cf1f1f4fdb973f366cbaeb5a4c68e285e8390f9d`  
		Last Modified: Thu, 09 May 2024 22:26:09 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc0cd82c00b229f2ea635c385ad86228687bae19afd4802c9c1e4461c15041f`  
		Last Modified: Thu, 09 May 2024 22:26:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2665ed524da7706f12a924357525aff9d4672e083e0672f56180ae7eb791712e`  
		Last Modified: Thu, 09 May 2024 22:26:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f539fc6af990de49ae4b29663c134312a4b2b77c77cf522dc065502bd05d4c96`  
		Last Modified: Thu, 09 May 2024 22:26:11 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4ff6b07a1130ff62cfe58bed7fde21369f9fb3bc6871c397a3bc8dd261564`  
		Last Modified: Thu, 09 May 2024 22:26:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:486262ef801f36929cabc4fc0061de40614983deba552ef4ae93ab05b455e92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (37021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50864efa1309bc07349289cae2fa895cc0250a6c0cf37c7c80fecbab4924c139`

```dockerfile
```

-	Layers:
	-	`sha256:de78249d2cb52d43810f81d202908716999f017e76fdb320c42a370fb07e55fe`  
		Last Modified: Thu, 09 May 2024 22:26:09 GMT  
		Size: 37.0 KB (37021 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1f72a33c765aaa9a9eb0fa8570e326c5dc75c866c558b4a30158cd0f4ad62c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85404782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03de67603a5f1cb91bb055deddc80bca90f768b585a1f02dfcd5ee1d7073f926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34183be10276d5bf28456f8dfa0b74b7d3728c5cf15e6e32a1203d02c80f06ed`  
		Last Modified: Sat, 16 Mar 2024 16:21:42 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bfc51b527ab2c0a5829fb7c7ccd2555218ae3b9c54fce2f19c92a88f06ebe1`  
		Last Modified: Sat, 16 Mar 2024 16:21:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd75d9a75e08c82b6b9f96b283a4d9c6d648de69abe851873a666e3cda2ae650`  
		Last Modified: Sat, 16 Mar 2024 17:10:49 GMT  
		Size: 82.5 MB (82469910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3b93652fee2db70e4a8389cb72952dbc5397afec972775fa48e5f670ceeb9a`  
		Last Modified: Sat, 16 Mar 2024 17:10:47 GMT  
		Size: 8.7 KB (8691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b375c6e6401cb0cfbe59eacf1e7fc4f234eb8b4514a4f82f480a46dd2cf5bc3e`  
		Last Modified: Sat, 16 Mar 2024 17:10:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced22f64259bc4821a5e71239c555886a7fab1daf22d59ada9fc8afc02e00652`  
		Last Modified: Sat, 16 Mar 2024 17:10:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b2ff185dd1d4351622731b55dfcd39cf432ee707f6e7d83d838a47dfa2c8f9`  
		Last Modified: Sat, 16 Mar 2024 17:10:47 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c993f8f5a4670de2242b99535e28f8c28511f247104ecadd20f656fee5930ed6`  
		Last Modified: Sat, 16 Mar 2024 17:10:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:0bde692ee1b9ee0cfb26478666441dd6c8e6019046c86fdfc87a18fee2853d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.9 KB (991922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4590cdfd6377275bcf08eae65992a89d6725b8539147352beef88a0de383a893`

```dockerfile
```

-	Layers:
	-	`sha256:30eedcf4f70e49f5a486ae54a6c897a143067df83255de2710bcec2558252a73`  
		Last Modified: Sat, 16 Mar 2024 17:10:47 GMT  
		Size: 954.7 KB (954687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1487007fa2ba21961e3fca15bc63bb8b20e82df518f36b9756b1232dbe398248`  
		Last Modified: Sat, 16 Mar 2024 17:10:46 GMT  
		Size: 37.2 KB (37235 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:abda59bb390e8a089ac737e48ddec71e9ec8af1042c6b728e349eaeec099e409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90817415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d09df0b192e4a8ca02404740548070bd5f554874ff07f21ebff82bae9ba8e32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73755f5e6a3e2578f900066d181e75490b8bf689b8d0355238deaed61e3f05c4`  
		Last Modified: Sat, 16 Mar 2024 15:59:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a60b4a71875ce3dfc2287bf071788323b63279c8053af79546e71be4447ba4c`  
		Last Modified: Sat, 16 Mar 2024 15:59:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad5235aae3d6bccf875722d4b6b57659e6514f88135582bed80020cc1582fb4`  
		Last Modified: Sat, 16 Mar 2024 16:32:05 GMT  
		Size: 87.5 MB (87453732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdbf0d5e4dafa595b0ddf2a4127ac418c7706062816fe61fa915894bd08d8ff`  
		Last Modified: Sat, 16 Mar 2024 16:32:02 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c002d4e94eb510c2d4c165b0c6c77de2a2a07b5208edb214f980b4c954e04833`  
		Last Modified: Sat, 16 Mar 2024 16:32:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1135e040d70392b2841de0418bc92943f8d30d252ec14eeabfef264fb03b74`  
		Last Modified: Sat, 16 Mar 2024 16:32:02 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0debe6ba0bf5e070c2753007f7bd308afeff3ad88fe7e3c272505bafa5589ef1`  
		Last Modified: Sat, 16 Mar 2024 16:32:03 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e39c76ebcc73caba873f4d6b5660e6ee9e1d1c307d84632121d38c9ed557e30`  
		Last Modified: Sat, 16 Mar 2024 16:32:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:7847bfcd1ba8718ead9d60f351c5d9b6911c904a899c4b00b925045b906f9057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.8 KB (991760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d88e1855c76123cba1161d15e2f304edcc5122d23ce1e40e0e90c2d3040281f`

```dockerfile
```

-	Layers:
	-	`sha256:18fe0844d9e613b9ef34645c99ca6f22a12a43df7110beddcbcdad604ba7adc6`  
		Last Modified: Sat, 16 Mar 2024 16:32:02 GMT  
		Size: 954.7 KB (954662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e3acef4ee3fceef043b0b6df508560cb1563b0c456cd2077ac1782f4833274`  
		Last Modified: Sat, 16 Mar 2024 16:32:02 GMT  
		Size: 37.1 KB (37098 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:ecd603ed468954797d837021b80b76c5638a3f8a99794ff9d1269dddfeb75cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99082344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8502c9f0cb852abdeb06786cb9fe49192f76846fcb4c9431440aa381b853a9e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Thu, 09 May 2024 18:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe948037611bc6fcd1b197fd6f1b7b1851d1da8547d5aa85e6735eddee6b956f`  
		Last Modified: Thu, 09 May 2024 21:57:01 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9379064714b0d03265f80d9c907bdd8457cc755dd26b83478d52ff9032082b`  
		Last Modified: Thu, 09 May 2024 21:56:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb39310800ccb5b4336a849e015f0a72f38f4643dabc642c2660e7c4448971`  
		Last Modified: Thu, 09 May 2024 21:57:03 GMT  
		Size: 95.8 MB (95822285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b044d76b4b5d33218a8c4076e302daaa838c00de2db53352d5258ff359c45c80`  
		Last Modified: Thu, 09 May 2024 21:57:01 GMT  
		Size: 8.7 KB (8685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2416c4d649de332224dc04a216ffc48a8fc42cbaf0839f682c1c0750637416`  
		Last Modified: Thu, 09 May 2024 21:57:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2994c383d2a2ec5c7360ed09419a7cc8acbbef7cf12621496cd311c7883a5f`  
		Last Modified: Thu, 09 May 2024 21:57:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee27425618cbf27be11d411c5266a9600b9621f171ef67a4207c98054c9e905f`  
		Last Modified: Thu, 09 May 2024 21:57:02 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e365a4548cd846c0c8999e33232bcbbc4bd6910410f1a8414cfd4064f7f2f5`  
		Last Modified: Thu, 09 May 2024 21:57:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:f36b0132973a44a13b891b06888ee5c6f5f90361fc4bc128c14f59aa3e088863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.8 KB (991847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9165c09c5ae1e3cf7a174c5fac19f7d21d2c3e64787702e8b4f6a5315698191`

```dockerfile
```

-	Layers:
	-	`sha256:8f97bd93a9e61bd83e129ae825d3019c8e337e568ce5916c85edf119411b99c2`  
		Last Modified: Thu, 09 May 2024 21:57:01 GMT  
		Size: 954.6 KB (954630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8bd261395d4dc4542ef2c9a12439917006f9e1b4548c391b1d4daf879d38337`  
		Last Modified: Thu, 09 May 2024 21:57:00 GMT  
		Size: 37.2 KB (37217 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:c94bedf7b8f790a2c5039261995fb6cfc99fd324585403b0dbdc82b471e03dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96428757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ac38ddba45ad5f2933297d7612cf4fc615df9937e31d7c9e7363242e14a50c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79df8127be221428a326f357e04f1c6c7907b2ac1145408ba7f22a36fe89ce2`  
		Last Modified: Sat, 16 Mar 2024 10:37:24 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e0b43ea44af8adfb383299b0e1e2f4fdbb58b567f44792024513de6b0a73dd`  
		Last Modified: Sat, 16 Mar 2024 10:37:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8717216fafab9dd16c2463d76bafe2316d6ee8ef3e468cab3b2fb50b2d935b4`  
		Last Modified: Sat, 16 Mar 2024 11:15:45 GMT  
		Size: 93.1 MB (93054429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a22305976600b6a1c4324e46d4ed86b46a57303eb6275535201e321b86dace0`  
		Last Modified: Sat, 16 Mar 2024 11:15:43 GMT  
		Size: 8.7 KB (8690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa481bcae4c19a66bcecb969af1cca46f856cc5a6bb60a84b2e1fecea19dc4a`  
		Last Modified: Sat, 16 Mar 2024 11:15:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2474bd279bfff0087cab9a85cadbb2dc72f3199af392cc593da5d19aa026dc`  
		Last Modified: Sat, 16 Mar 2024 11:15:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f78e5776deb4221c47227e30470cdad12fbf9e6a60ca90680c0ca321c0afb3f`  
		Last Modified: Sat, 16 Mar 2024 11:15:43 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ecc7de8fe65f9676dce009f4f5ee456cfe6e6b5c08f4279567562b2edd1fea`  
		Last Modified: Sat, 16 Mar 2024 11:15:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:cb66ae498d11c018b213db1ea21d1c3ced32600948b473ab1ed416cc9379a851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.3 KB (988348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44195f8a4fea66a66c9e2f174b259e22e27a46bbb10c22072aa869a6514ddd83`

```dockerfile
```

-	Layers:
	-	`sha256:9581c1747a65c27ee0733577ce3b64c1c707c659a0132bdd3a452138a9500816`  
		Last Modified: Sat, 16 Mar 2024 11:15:42 GMT  
		Size: 951.2 KB (951210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428e332e06fe4f36fb7070cb6a8fe7711d4380013ee490ee3d563d7d130a59cb`  
		Last Modified: Sat, 16 Mar 2024 11:15:42 GMT  
		Size: 37.1 KB (37138 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:a737e5d14e96200c0e213120f47aa339d8bb657388c57e1d017a251a238d0570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100703868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440a334c2d7cd9e1da9750d3440e322a1d28909112cb7932068613b4fcaa6026`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b489054c2615f089cba89c06b37f54196a4126ea5a9cfb8effbc74830a1f4f`  
		Last Modified: Sat, 16 Mar 2024 10:31:09 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4eea410b978ff2de9eefa709d8a755a0f6d5fc0a75a1b81c0d491fd465717b`  
		Last Modified: Sat, 16 Mar 2024 10:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e777290ca7cdb62d82721f7eaf3e282b977b81e80a9f474f502b7b59038f0dd`  
		Last Modified: Sun, 17 Mar 2024 04:02:27 GMT  
		Size: 97.4 MB (97445260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8289715a1659bd3849fdbcf6dd58db589ed25dd2d145adcdd8abb8f8e9651dca`  
		Last Modified: Sun, 17 Mar 2024 04:02:26 GMT  
		Size: 8.7 KB (8693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4b109b8b7cd4fdd642d2e8e793ee369a7538ff5bf0f2deeab2a8487f6904eb`  
		Last Modified: Sun, 17 Mar 2024 04:02:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395e450e7fd32be818d9399571cb6550b44dfd9423f58161baea72c4251d9140`  
		Last Modified: Sun, 17 Mar 2024 04:02:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addbec9a3277fc2c5e0a000533f45f30d887ebfa8f0316c18ddd6bdaf959268a`  
		Last Modified: Sun, 17 Mar 2024 04:02:27 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5253db07997a171647044a4e20ff95ef4814c33709689d2c0f032d3c094bab2`  
		Last Modified: Sun, 17 Mar 2024 04:02:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:eaca29fa22689a1639c7b22f727f558910b8a27fd8b904732e95a87abbba5c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **989.8 KB (989785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413b417f4ae581e050bcc90d463c4fc97c68deb540d03d683eed7c34f614ad8e`

```dockerfile
```

-	Layers:
	-	`sha256:53d7f0825a4abd5838f912e1f9217e18a94beb261022f1b968c8e772b01075a4`  
		Last Modified: Sun, 17 Mar 2024 04:02:26 GMT  
		Size: 952.7 KB (952697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6970bfa83afb8f5bd5045ee7f8745e3414cb75182733680726a09d5cd82173e`  
		Last Modified: Sun, 17 Mar 2024 04:02:26 GMT  
		Size: 37.1 KB (37088 bytes)  
		MIME: application/vnd.in-toto+json
