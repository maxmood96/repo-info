## `postgres:15-alpine3.20`

```console
$ docker pull postgres@sha256:362404e4f27e4f477c6cd4a76c65f06d387b7fda2caf216e656b17bf00f9908f
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

### `postgres:15-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:219fb9d943f8fa1f07d425fee6d4e0c93c52c53bb4fb97cd311ec1a4d438089d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96010673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9156a9e8b840766922b608e7ea181f379894a5bb67d60f526b5e4a0040112a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_SHA256=4403515f9a69eeb3efebc98f30b8c696122bfdf895e92b3b23f5b8e769edcb6a
# Thu, 08 Aug 2024 17:06:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ab95764ea3d9d228d0364126c59ebeeac1c92e53c401f348ad7adcd93930b8`  
		Last Modified: Fri, 06 Sep 2024 23:20:30 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935316949c7f22d5d753b77ecd374e5bb24e1326b81b77a17f2940f2bdf7dc2d`  
		Last Modified: Fri, 06 Sep 2024 23:20:30 GMT  
		Size: 1.1 MB (1119774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675d717e7e293a9b3dd796197b7078bf2cfe81347b9e323261b7207025f78614`  
		Last Modified: Fri, 06 Sep 2024 23:20:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff953869449944092943e4d875e4870cfdcd03c3d8bda9078298bc21a91aad6`  
		Last Modified: Fri, 06 Sep 2024 23:20:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf370ec807c597038418e14bd3c6e9621378c39e79a84b98736fbdf412813e13`  
		Last Modified: Fri, 06 Sep 2024 23:20:33 GMT  
		Size: 91.3 MB (91250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a054d768ddb624815273c830a98dc86df6e76859a44a5da7c1da80cd91e7e5fd`  
		Last Modified: Fri, 06 Sep 2024 23:20:31 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577ac298767b85c0719008f921550f80203d182ceed621de4090f77ca63c3c4f`  
		Last Modified: Fri, 06 Sep 2024 23:20:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70ea69731cca5660a07370f8696e738ecbd045f60fb8a42f84dbeb8d78ff2a1`  
		Last Modified: Fri, 06 Sep 2024 23:20:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb1487c3b1daefe109648fa80ec3fe504109c0587501d3bc65d84f0130ecd1e`  
		Last Modified: Fri, 06 Sep 2024 23:20:31 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f588a0e40be05a8ad9471ee951f98dc2ad176956a066ab3e606466662c81b8`  
		Last Modified: Fri, 06 Sep 2024 23:20:32 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:1fd9e4bf02968932dcfc2c58b49645c0248af812328b862ce8864330421d5244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.4 KB (636407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ea7ea2dce4448f8c0470d1db22bfdf4b02783de0bd7ae2eb7fe1fb78fb4d73`

```dockerfile
```

-	Layers:
	-	`sha256:f776441293636fd04dae8f6f3ca5d14ace76eb5960d4025e1467a86f6c71915d`  
		Last Modified: Fri, 06 Sep 2024 23:20:30 GMT  
		Size: 590.7 KB (590697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7875031df9795556ab23a7d0b56f233b70a63fd18c7853fc09be827ca200fa2`  
		Last Modified: Fri, 06 Sep 2024 23:20:30 GMT  
		Size: 45.7 KB (45710 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:1b1eb3d4a8cccc88de32cf49281258cec42746c4973394d1196b07a008962ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94766106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f06f4b617971ca427da98d150e5fca846f694a400e06ad48defa38bffd4e918`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_SHA256=4403515f9a69eeb3efebc98f30b8c696122bfdf895e92b3b23f5b8e769edcb6a
# Thu, 08 Aug 2024 17:06:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1926ba8f8f62878b68875756f8686ff4fbac12ecedb3040e7fcdb795834f064`  
		Last Modified: Sat, 07 Sep 2024 08:42:22 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8999ec1aa34d37759a1bc9a1ab2364f588fa7168269d15b795fd1f59eb268fb`  
		Last Modified: Sat, 07 Sep 2024 08:42:22 GMT  
		Size: 1.1 MB (1086464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751d0a1b6a5f8acc091860ce9cefa33d4a4763f0a4d758cb02b7cdfb0ca5d2a0`  
		Last Modified: Sat, 07 Sep 2024 08:53:54 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970105bc24623b15b6694f85b81c01da170360a8ade161ecb48f80e2aed986ac`  
		Last Modified: Sat, 07 Sep 2024 08:53:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb4b15d2e1740a49a5b7a4ebef3563ec1627d10a4696f7bafd491e906b59b`  
		Last Modified: Sat, 07 Sep 2024 09:04:30 GMT  
		Size: 90.3 MB (90296503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7ffa97ec4b5cc6746ea375c9606a7591a3daf12e8305aba1df4cab658dbff3`  
		Last Modified: Sat, 07 Sep 2024 09:04:27 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b465ca08422a429cc5feae4bd634453ac100c54c3455e5cb9ac33de782db57e`  
		Last Modified: Sat, 07 Sep 2024 09:04:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc81190dddc0c334d10350bc1a55e99866bf923174227127829cbe473c0255dc`  
		Last Modified: Sat, 07 Sep 2024 09:04:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3420036a6985b612db98825fa01b6d887fcfa54cb7705a3586836c3e27c6279f`  
		Last Modified: Sat, 07 Sep 2024 09:04:28 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e8e881ab3fc49fb282fd0e1043d417501a097d9fc584ba914bc5ed0e540171`  
		Last Modified: Sat, 07 Sep 2024 09:04:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:93aed943afe7d26d2ab750698df7d1a722c452ead5fc9900daece3c39b71df19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 KB (45665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bf59aef495723ef2012425c165defbf70cfad14e95c3795c9442067db12355`

```dockerfile
```

-	Layers:
	-	`sha256:17be0606222cedc29495b44fefcba29e5da0e52a889c95996f9a0d7cf05327b7`  
		Last Modified: Sat, 07 Sep 2024 09:04:27 GMT  
		Size: 45.7 KB (45665 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1206b4fe71837a6c13730f4b97be07f58c1a4200a18b4c7e6dfec979aac0b095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89198175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce48f4c51853ec52cd61183555bb0d2511456871b88e92eb16968df56684c6cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_SHA256=4403515f9a69eeb3efebc98f30b8c696122bfdf895e92b3b23f5b8e769edcb6a
# Thu, 08 Aug 2024 17:06:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ac8e9d0c68b096b09818bfb20f42e953c3d9cd9df375198a3b549dd5ce5f63`  
		Last Modified: Sat, 07 Sep 2024 09:07:01 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea95758d71d5413b7fd57d98797bffda5c623934cbefc0067a635c1ff9f62e9`  
		Last Modified: Sat, 07 Sep 2024 09:07:02 GMT  
		Size: 1.1 MB (1086468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93540d99e99914202c8ed07dbb4762ba225d2c6061670c2fafc29c7af5b206`  
		Last Modified: Sat, 07 Sep 2024 09:15:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8913630691ba9994e15bc5ad692e83b0d35705f5db68d326926e420ae066c0e7`  
		Last Modified: Sat, 07 Sep 2024 09:15:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce55d211597f90dd12b2bb27e21c4b167a62beababef2e3061a8dc8c0f231f8f`  
		Last Modified: Sat, 07 Sep 2024 09:22:50 GMT  
		Size: 85.0 MB (84999579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4841f9177e273af6cb4b754d63ffcb2d59528e7c0e3b06e54d4e6217839610a2`  
		Last Modified: Sat, 07 Sep 2024 09:22:48 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adfa63ed403b3a697225aa0fab695baab70d08ddd9cfa29fa52e50f0fec39e6`  
		Last Modified: Sat, 07 Sep 2024 09:22:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c5910937cac85cdd0b8c907a478ed0ac2828f614fafa83599200da17959f44`  
		Last Modified: Sat, 07 Sep 2024 09:22:48 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffe0f19587772868b81717cc6b16e24e2570518fbdfec34730942b6c20631a9`  
		Last Modified: Sat, 07 Sep 2024 09:22:49 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcba1b3f981e40ef25e80175c711ae376a0db1d50d8244e29eb3ff091289d192`  
		Last Modified: Sat, 07 Sep 2024 09:22:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:8620345a5bb756523b610acb4cbede754d483fe9e5ac4d93fe7461b9adb4f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.6 KB (636617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54eb4ff0699678a3260c76caf567774ec57be753f1b44fe0c2ae67c4e86c27d`

```dockerfile
```

-	Layers:
	-	`sha256:b8f36916e41cd9ade917e25d716d83b8ec289a75b84eed30f1bf2ad4f3e498f1`  
		Last Modified: Sat, 07 Sep 2024 09:22:48 GMT  
		Size: 590.7 KB (590733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc99d47b334063befa0872dc3d7ce0f42452009a8228bb7a1110dc7f74b154e0`  
		Last Modified: Sat, 07 Sep 2024 09:22:48 GMT  
		Size: 45.9 KB (45884 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:319a6f261f6b620a97ab2fad6432d02cc410fac7c4a0ad0138404f935620065a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95233884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b82e155425ecc5b70ff071a5e532b649d83a07bf85b89123c8c02c895f89cb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_SHA256=4403515f9a69eeb3efebc98f30b8c696122bfdf895e92b3b23f5b8e769edcb6a
# Thu, 08 Aug 2024 17:06:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce02d10b61bf34aa182aa7cd3783def4d5bbd8176c97011032c1508b214ff88`  
		Last Modified: Sat, 07 Sep 2024 08:43:43 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc2a136d16381dd1cb44173056502b63f1221519780ccd6a68b144efc25d984`  
		Last Modified: Sat, 07 Sep 2024 08:43:43 GMT  
		Size: 1.0 MB (1047249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ca8946873e79c55e98d72c8e8199b4e5fa08d6d8c68ef8a6901d7c0300fd2`  
		Last Modified: Sat, 07 Sep 2024 08:49:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e732be064c163369f8060a02cdb4896b04c1cdb30b10c1a5bb161a03df18d9`  
		Last Modified: Sat, 07 Sep 2024 08:49:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c930377fd7a2f41d6636d60bd17b096686113e6f665807c8511e77d5de6e6e`  
		Last Modified: Sat, 07 Sep 2024 08:55:37 GMT  
		Size: 90.1 MB (90082364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34eb2e93aa286ec713607dd3d735869b4affa3aa5be3260fed0ea2cf001dc41`  
		Last Modified: Sat, 07 Sep 2024 08:55:34 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14965af90e8e434fb0738c04ba7f6856415ac0c52dd6366b82821ab610098982`  
		Last Modified: Sat, 07 Sep 2024 08:55:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188aec8a964d8ef27474bc71bc7ff5bf502fdc3315e8c6448fbbe9efd3b3cecd`  
		Last Modified: Sat, 07 Sep 2024 08:55:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eb370a0f818e835df6606aabfe11e6c18e3ece61499b165ad042ddac543ac4`  
		Last Modified: Sat, 07 Sep 2024 08:55:35 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647fdd00ceebe554fa7b2499edaf57300bbb0e57576d5869281adfe5cefc7f49`  
		Last Modified: Sat, 07 Sep 2024 08:55:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:867f4d597cd66392103b3f43e1f35265a0011597fca7cc120d5f2995dbed7126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932e60fd2fdf7d5345e14be96a7d63a63ea920401e4a80919af8e010dafa5259`

```dockerfile
```

-	Layers:
	-	`sha256:41e9a1476d0b7169c9d58c505565ba686f9474fdd8731bd1b5a2d6e59ca6785e`  
		Last Modified: Sat, 07 Sep 2024 08:55:34 GMT  
		Size: 590.8 KB (590753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a17e147752d353c4da53848f69a0e7c4d3ae163afcb9de31186ca856752bc20`  
		Last Modified: Sat, 07 Sep 2024 08:55:34 GMT  
		Size: 46.0 KB (46010 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:097966bb4804ef5f4adc6739753aefaa869aad36543d195f2c05304088a6a2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101344609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faf20dd0b7673a637317cb8b691be55f27f639d487f47ba5dd9ad337bff8c8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_SHA256=4403515f9a69eeb3efebc98f30b8c696122bfdf895e92b3b23f5b8e769edcb6a
# Thu, 08 Aug 2024 17:06:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5347f94af1180d28b95ced238d95ada5f341a47988f6b2978578e14a6fed53b1`  
		Last Modified: Fri, 06 Sep 2024 23:20:52 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb28d81fec4eaeec0bbece40cc27e067ce8348f7572073159e2d320818d3ef9`  
		Last Modified: Fri, 06 Sep 2024 23:20:49 GMT  
		Size: 1.1 MB (1094864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c526ec867ac2829aa79219a6643cab9b3cf9d7476c799d1a1ce7476ead7569`  
		Last Modified: Fri, 06 Sep 2024 23:20:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff953869449944092943e4d875e4870cfdcd03c3d8bda9078298bc21a91aad6`  
		Last Modified: Fri, 06 Sep 2024 23:20:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9ccb6c81c055fdfabc71512f44b270f7ece504f2d48fac1574b0781f2afd9f`  
		Last Modified: Fri, 06 Sep 2024 23:20:55 GMT  
		Size: 96.8 MB (96763969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf3ce6d236392c875ec93c6dc70c7313df8750889f0458e49ae0cb86c3debdc`  
		Last Modified: Fri, 06 Sep 2024 23:20:53 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f6deb1d68b2d2160317ba0ef1390d1a1190797eb06a22f7aed48f25ff9d95c`  
		Last Modified: Fri, 06 Sep 2024 23:20:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f46e67a3a9f9175ce837c9cb8a213e4d656b665e9b375009d8acabd317c117`  
		Last Modified: Fri, 06 Sep 2024 23:20:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87ff9d16ba65b29aabe084e93fd48d80e566527da02455c38a0c6b8cd5badaf`  
		Last Modified: Fri, 06 Sep 2024 23:20:54 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d24afcb274148b6657867f6521c92550c9ec628e4e42931c8b4707956ba3fa`  
		Last Modified: Fri, 06 Sep 2024 23:20:54 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:8587181346f284b76b62fc2be3ec1619e0ce771a5e308a8a4fb142876bba7874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b259809427d3d1254d2873a466002f663b4f5f03b80bcd8421bf30df6f2b8bb`

```dockerfile
```

-	Layers:
	-	`sha256:ddc81f34f06e3bcb878677a2e7995552ad4870506155ad87faf7cb513ba39abb`  
		Last Modified: Fri, 06 Sep 2024 23:20:52 GMT  
		Size: 590.7 KB (590672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e287ed13094128919c923f80368f3574a05df83a7a5005a3e6d9add45e4c02`  
		Last Modified: Fri, 06 Sep 2024 23:20:53 GMT  
		Size: 45.7 KB (45665 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:e66c1b770f54c1af001d3eb12813b5e4c1e86992e9a6e42a2fed9242ad78cc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100570283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea8de8bd03fe069fa3304dba1c2ca5634c4fd61fe3249b29663ae378f76cfa9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_SHA256=4403515f9a69eeb3efebc98f30b8c696122bfdf895e92b3b23f5b8e769edcb6a
# Thu, 08 Aug 2024 17:06:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09660e5b8bc5bd55341d07e7bcd5185688c061c64258a651b47cea587e00681`  
		Last Modified: Sat, 07 Sep 2024 08:12:00 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1554d2d2be5884f5ca5cba1185e70dc91ca57d033741832939409b096d44a`  
		Last Modified: Sat, 07 Sep 2024 08:12:00 GMT  
		Size: 1.0 MB (1037925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d6596d280a805aa5a8b65088be867ab8d3aa3da87cb4548b772bf00f63588d`  
		Last Modified: Sat, 07 Sep 2024 08:18:21 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30acef047ab3f799f45c92aeefb8ee0ee366c2748536be8afac3972a86409351`  
		Last Modified: Sat, 07 Sep 2024 08:18:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c6f789915769b06af23cacd8ca0a2185ba17b218f2cafffc3fdac419d09e0f`  
		Last Modified: Sat, 07 Sep 2024 08:24:29 GMT  
		Size: 95.9 MB (95943310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d56e4417ca44d9a8376d0300ad9ecd74f6e8b433a5815ac1d30fbd5b5836f7a`  
		Last Modified: Sat, 07 Sep 2024 08:24:26 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c3ac090f9699dc1b7b332fd4464b3c5d7a3cf20699ef51652fe6fc526a904`  
		Last Modified: Sat, 07 Sep 2024 08:24:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92167136dcdc52404f3484f996a8c271002a895e8902cddc7e44442eaa280ce4`  
		Last Modified: Sat, 07 Sep 2024 08:24:26 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707aea56129206e4644d0d3bde62ba7da8fc12bd1313ea34a95e0eb39232456a`  
		Last Modified: Sat, 07 Sep 2024 08:24:27 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031a9385a4a96b2eb434a4232f5825839c4e2cc7f63480baa4abfeeaf351266c`  
		Last Modified: Sat, 07 Sep 2024 08:24:27 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:5f7d58b61aa09cc889bfd84174411e630af33d698e4887cab88fa4ba686ab3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.9 KB (632877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406c09eb03ceba8c43becf309941f47438918febd83c1bfce2f3e1564146053d`

```dockerfile
```

-	Layers:
	-	`sha256:af3dc7b4c919a9ddbca08eaa446235c495ff248e176d5725bd5fc4669edf9605`  
		Last Modified: Sat, 07 Sep 2024 08:24:26 GMT  
		Size: 587.1 KB (587113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6ae41a2bcd501bde46b0e183f13a097cdf850ba7b5d37a3a418a7961d0605f`  
		Last Modified: Sat, 07 Sep 2024 08:24:26 GMT  
		Size: 45.8 KB (45764 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:73520ee92f97d08799e14b67313c9cfa670e27ac364257f02d28b45e1acb782b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96120782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f8b0573f01b2cbd52092e92b44c4e31f7cdd2a76bafd1abbc63f537b14e7f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_SHA256=4403515f9a69eeb3efebc98f30b8c696122bfdf895e92b3b23f5b8e769edcb6a
# Thu, 08 Aug 2024 17:06:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb1c65214fcacb9f32e742abec8b92bf683b2e7a7be27073b203cf9dc5d4574`  
		Last Modified: Thu, 08 Aug 2024 19:58:50 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a4e93ef12922da34742cb49015c46af1058cc89f480318d1346da5ee6f8f47`  
		Last Modified: Thu, 08 Aug 2024 19:58:50 GMT  
		Size: 1.1 MB (1087952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b325d1be0046ae9a0b3a10b1ffc701bb5de4aafe563d4ca18a51af14bb073`  
		Last Modified: Thu, 08 Aug 2024 20:46:43 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4709da855adf7450d0fcf456786c7a8cb1624a3c38c4a0bf6ebe1ef932e32e0`  
		Last Modified: Thu, 08 Aug 2024 20:46:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1516174482bdfabaabf8527cce2d23cea3e56dec6a624543a0094dae14cb570`  
		Last Modified: Thu, 08 Aug 2024 21:32:56 GMT  
		Size: 91.6 MB (91645519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245b4783315c84b124d4d1476aec813c0c6e2c0926ae76632aad53c9ed4f860`  
		Last Modified: Thu, 08 Aug 2024 21:32:43 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c097ae2f61e29f8486a377985e99e896b6e842b3027f88f33ec205d2f43fdd4`  
		Last Modified: Thu, 08 Aug 2024 21:32:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2911718ddeddacdf187c772894fd7c64a8ad9c476724d9ab2fbc0a8571fc7c13`  
		Last Modified: Thu, 08 Aug 2024 21:32:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41653c9105cb1e40c1a6058e266c84897cc49062643f27fd5cb087c69147812a`  
		Last Modified: Thu, 08 Aug 2024 21:32:44 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991874076887e0f35ac17d31041c67ec19c606b5a9eba5f9b0d823ba501e02d7`  
		Last Modified: Thu, 08 Aug 2024 21:32:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:f73bd24176698bec77e122dd6d0632dc0f026b3838f864ccff7c382e43570dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087924cffaf55380de94b5312ec0a9cee3d9f218d3a1cf0511c4f0168c8b8f30`

```dockerfile
```

-	Layers:
	-	`sha256:d8bd77f89b3f0e6a57fa437993bf8bd66a333e1e4040e2bdb73807cfb35b6be1`  
		Last Modified: Thu, 08 Aug 2024 21:32:43 GMT  
		Size: 588.8 KB (588773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad2c48ea6d4b6b1d3d8ff8dd43b95930bd47ecf922ee5d1b8865782d26b00e3e`  
		Last Modified: Thu, 08 Aug 2024 21:32:42 GMT  
		Size: 45.8 KB (45764 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:36f80f9b3ea2e0b8ab92a7e09a6ca2eec61da3a0bb6699abc8a8409b675d8b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104916386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31870bd925068ed782723955a063fa8a8d80456e3565803218b93526a004f6c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_SHA256=4403515f9a69eeb3efebc98f30b8c696122bfdf895e92b3b23f5b8e769edcb6a
# Thu, 08 Aug 2024 17:06:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bd51305a798a8f4a2548106c9ede18568dab62599f818ec4a568a640541969`  
		Last Modified: Sat, 07 Sep 2024 07:27:24 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77eb0b034a50a4f7c869cb4d64d60e371eca69a55c30006747fb3a91328aacc`  
		Last Modified: Sat, 07 Sep 2024 07:27:24 GMT  
		Size: 1.1 MB (1083302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae0cd9e3c227f9e874d4fac08c444e3ac40d3b959cd6a3d31351ff1594907a`  
		Last Modified: Sat, 07 Sep 2024 07:37:08 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf72d40b4fbebd98d7ab2aa3e1fabbb60f08d02688c85979de76e743727ddc9`  
		Last Modified: Sat, 07 Sep 2024 07:37:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6f66ad58d30a43c386fd08861a81c38696df6c29d86618f2da241fc2ac177e`  
		Last Modified: Sat, 07 Sep 2024 07:44:33 GMT  
		Size: 100.4 MB (100354856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f155a1f3205114c15984bcf21e51007c797157b2b6c75c23fb5923738b2c8faf`  
		Last Modified: Sat, 07 Sep 2024 07:44:31 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf222d83bbcf2a33a4fb0a4cb169b564ac72fb203d2dee0e33a463ff409074d`  
		Last Modified: Sat, 07 Sep 2024 07:44:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48873c7f704fd3613ec187df8ed2f65d56e31494cf1a83004e46ce056f6941c7`  
		Last Modified: Sat, 07 Sep 2024 07:44:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c6f7e792e0b237bead74651c041dcfa8edc48dfe2f879bed9e98a154e6036f`  
		Last Modified: Sat, 07 Sep 2024 07:44:32 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc867032a6bcab86ec17bb537042ede316ba21c313d360e156ada9bf343ff1c4`  
		Last Modified: Sat, 07 Sep 2024 07:44:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:824d245abb045856329f59381624b5b916487e1663abd9a78043b8e1e2c6ca05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de783858dcb66abc024999e5c899036994c812416c21c8e660fc6fe94d1596e`

```dockerfile
```

-	Layers:
	-	`sha256:8ed5625ad094efaca2843857f216705c2a10f546053a19059c8ba2fd810979c3`  
		Last Modified: Sat, 07 Sep 2024 07:44:31 GMT  
		Size: 588.7 KB (588743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aadd5ec368b5ecde859a876812e68cfa9ac239791f1dd89f6fb05101d7f38a9b`  
		Last Modified: Sat, 07 Sep 2024 07:44:31 GMT  
		Size: 45.7 KB (45716 bytes)  
		MIME: application/vnd.in-toto+json
