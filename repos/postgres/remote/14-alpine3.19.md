## `postgres:14-alpine3.19`

```console
$ docker pull postgres@sha256:b1c2e7dbce2739e32a157ddabf67e81a19cb0d73474c36911c655d9bb2d4cdfd
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

### `postgres:14-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:ac4ca373551069f5cceb157bc4ba7fefc67069f3cf7dfb96fa3fbfece9888d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94186652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd1dccf8db78e3a4ecf5746a81a74e6dc1478bf57759091fe2ffed6c78d2f3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_MAJOR=14
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_VERSION=14.11
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_SHA256=a670bd7dce22dcad4297b261136b3b1d4a09a6f541719562aa14ca63bf2968a8
# Thu, 08 Feb 2024 19:28:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:28:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:28:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:28:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54d40fa3899a525bbb99c32ebce8c195e7b25c87abe156b8197f8e4ef6ad486`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bba88902c495619a79e90cd759e1e0787fcb2b941ae5afdfef06b2cc04470d`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895cde69c46d0fbbf1863c26dcdcabf2e83c648e6e1b46399cee57b8beed710d`  
		Last Modified: Sat, 16 Mar 2024 00:00:37 GMT  
		Size: 90.8 MB (90761441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f283b4aaa3dcaa969eba9c4a0ba028141757fd3497838a036e9e08fc4c78b562`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dfb80fbe96078085c608cb6142ae44d178f7cd02561afeb2896f728b27ecd4`  
		Last Modified: Sat, 16 Mar 2024 00:00:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab9af40886f4c0dd7e8ee4879a511d7fc5e2973e6772b5a3f01e8fb72f0d6af`  
		Last Modified: Sat, 16 Mar 2024 00:00:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0008d7ccfed1d634a28499fb861242579846ca925e577ccbb650ec3da7a9b5c0`  
		Last Modified: Sat, 16 Mar 2024 00:00:36 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f53a735edbf0fa3c8cd156ff886800fe0a6e218f2c8a47f07fa7d1e2aacac75`  
		Last Modified: Sat, 16 Mar 2024 00:00:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:efa53e1526dcc463d314a69bcb3e880fe3a8aff1f3228494929605a8d7e3e053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.8 KB (994847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca6347b0f43f71f8af17193f6795239048b673080ab6e8f25b8eabad20c7567`

```dockerfile
```

-	Layers:
	-	`sha256:8097c257d44a8e9979985f41b5048faa8a51cbc9d73f950bc146cfa3dafcd0c0`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 957.3 KB (957313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462900712394a61ed578fc1a343a62698d66e9dde5f5645313eb0afe9519cac1`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 37.5 KB (37534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:fa6bc9e76f6e7af9eb4bc877c44266f95ba872bd05ee70def806b6807a41fe80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92959659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e765043b828741b2b8039461b6ff0357ab2debb5c5b4e87f449cd62efb8b8bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_MAJOR=14
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_VERSION=14.11
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_SHA256=a670bd7dce22dcad4297b261136b3b1d4a09a6f541719562aa14ca63bf2968a8
# Thu, 08 Feb 2024 19:28:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:28:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:28:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:28:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ad518b0cf26aa61d9ca7c99a519c6a1e127fb2cec34a20ee0e078ffd31d40a`  
		Last Modified: Mon, 12 Feb 2024 22:17:21 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb22ad7323dc854410efedfb052711011a92b7f1dfad1d76944fcf85ddfa0e01`  
		Last Modified: Mon, 12 Feb 2024 22:17:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b000d0cb00a3045fbd37e1251544c5ed058dd04bbb07b436da30ebcc89e14e`  
		Last Modified: Mon, 12 Feb 2024 22:31:21 GMT  
		Size: 89.8 MB (89777783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a0598f0e0e8cd7b2e344f4ed4f487329acdf4616b14f123181ad1ee0cd3aba`  
		Last Modified: Mon, 12 Feb 2024 22:31:18 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984bc15dc561148bb7527342c05b595d99b8ace0da24d7aef36eba1482a415c9`  
		Last Modified: Mon, 12 Feb 2024 22:31:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82604cf8a3423fd348207f1683d8d41fcd537690ec6bd6de2701d044027bae8a`  
		Last Modified: Mon, 12 Feb 2024 22:31:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893fa9db76141ae25958470aad15e829ed01836688d870ed9e91f791cbe92aea`  
		Last Modified: Mon, 12 Feb 2024 22:31:19 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdc4386fda7d25e7d7f7e8b63899daaccc483068393fbd6c2c1678b0b58418c`  
		Last Modified: Mon, 12 Feb 2024 22:31:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:85f92f7d6b96a906bdb7150e157b34fc210186eabfaa524f955d82b05cd3a7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d458ab0dbee3a29174d2b54df143eb2cee072d0c3e2e4f737cc3dde1b5c56780`

```dockerfile
```

-	Layers:
	-	`sha256:4f7ac29c514ff31eb52decdd3a0797d28569f2685ca3ae94d9fe324c60a47070`  
		Last Modified: Mon, 12 Feb 2024 22:31:18 GMT  
		Size: 37.3 KB (37302 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:75ae237c76b4b3597802a81eb35d91fe2d69272b03c5c3bd19fa77e82de6c892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87425748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f2cd8a74d4954df49352ede19b30f9ca0e2c30f1a4fe6e02b84eee514cab5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_MAJOR=14
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_VERSION=14.11
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_SHA256=a670bd7dce22dcad4297b261136b3b1d4a09a6f541719562aa14ca63bf2968a8
# Thu, 08 Feb 2024 19:28:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:28:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:28:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:28:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04fac8f616621198f83a4989d82db0c9e941949e87e7f5c0b60b19218b49230`  
		Last Modified: Mon, 12 Feb 2024 23:52:42 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9fa50b5978ae8773362b63ed0f8d8a0a2136155bdc38ab7e05dfcebf9e9dab`  
		Last Modified: Mon, 12 Feb 2024 23:52:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15313c87087064d8aa388f8883ab6bc0ac93680b0dc41add9a9593efc6096705`  
		Last Modified: Tue, 13 Feb 2024 19:08:37 GMT  
		Size: 84.5 MB (84490370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1bc79b3cdca5e5695412222abc8451d763152ea1f3cea1b0396747500d40e5`  
		Last Modified: Tue, 13 Feb 2024 19:08:34 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3479ac9c44335e64b752eda2bfa1980934e72a1a78ac2bb50f7deaf4590fa22a`  
		Last Modified: Tue, 13 Feb 2024 19:08:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb655d29d16adc88897e35390e8cca6a9c98f7f04c4c44cb25353458c4e59cc5`  
		Last Modified: Tue, 13 Feb 2024 19:08:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afd905a33f5f4514d28769cc9c77e7875234cd9bb4111c96f16ad12d4481314`  
		Last Modified: Tue, 13 Feb 2024 19:08:35 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e78bb512485a6dc2fc29f80ffb8501d3ac8f9d7231656012f3757b7f653e8f`  
		Last Modified: Tue, 13 Feb 2024 19:08:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:a3903bfe5df1930d7262e65a6f1a798d911eb92046f3e98bbdb75d54026e71bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **844.9 KB (844876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a28108b6789b60fa2d863b7468661b656fdc9cf326359339b4edf3739004036`

```dockerfile
```

-	Layers:
	-	`sha256:4d83e950855760c702e6df6d4222fa655cffd61dabe1226f45f06b73b03f14f7`  
		Last Modified: Tue, 13 Feb 2024 19:08:34 GMT  
		Size: 807.4 KB (807359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653f0e4e368daeccf455c9b00665e98f87be4633b9bde0a8e4a6216c5dfaa437`  
		Last Modified: Tue, 13 Feb 2024 19:08:34 GMT  
		Size: 37.5 KB (37517 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0ef7db7e2af7003e658ccd7c3cd61773a4176b25b1e717bd08994cd2d89a6e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92940830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bbc20817bbc9056d458281827cc5cfd62856c2149e020a4eec39b2a99b8b5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_MAJOR=14
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_VERSION=14.11
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_SHA256=a670bd7dce22dcad4297b261136b3b1d4a09a6f541719562aa14ca63bf2968a8
# Thu, 08 Feb 2024 19:28:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:28:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:28:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:28:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9855befac3cb99a213f57d7cff6c01ac9bb63db6403f5b49c297b8e85b284362`  
		Last Modified: Tue, 13 Feb 2024 00:40:33 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45189928efa78a09b7a14fb5df6c6eff8ad7099cd14d8fa99c3ea75cbf347585`  
		Last Modified: Tue, 13 Feb 2024 00:40:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acceccb51d20ccd965d1c6965c5c2cec6e184a9df8a1e165a89d18f08ecccc88`  
		Last Modified: Tue, 13 Feb 2024 14:39:59 GMT  
		Size: 89.6 MB (89576633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a095d650a0a62d66b19a5c819b0218dd18c1bd5fd146b9c274128c44bf153329`  
		Last Modified: Tue, 13 Feb 2024 14:39:57 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9daceb05d25b7b8c66e27a70f828ad8660da8b0d865ce44b803775957ec4a77`  
		Last Modified: Tue, 13 Feb 2024 14:39:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21ea99abf5af23976698e053c44a461715e5e8b8f305afe782de37bb40dac2`  
		Last Modified: Tue, 13 Feb 2024 14:39:57 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6565253e1fceed98cac1bcc4ae25a1e3360cd502cbddab64045bbc0d5394a205`  
		Last Modified: Tue, 13 Feb 2024 14:39:58 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14153b0119d0c858089ae747da7b82681c49c6b4eefbeecad6d3cc32e37e898c`  
		Last Modified: Tue, 13 Feb 2024 14:39:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:e7a453aac18ba60d2b7f39eaa4501a796564e1165b1748f40ae38c91e9e39587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **844.7 KB (844713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481c204fa6324130cabba83be1c3546264569459c523a63f17a11d221c30d8d7`

```dockerfile
```

-	Layers:
	-	`sha256:f82790826903a86084b4bbd8e98b742e9103d3903e3a2b8243f1ae0cf82f8276`  
		Last Modified: Tue, 13 Feb 2024 14:39:57 GMT  
		Size: 807.3 KB (807334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e373257412d463ee561c034cbd02dea5b6dcd7b785df8a0d262431881fb1c7fb`  
		Last Modified: Tue, 13 Feb 2024 14:39:57 GMT  
		Size: 37.4 KB (37379 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:311bc1afb9e23792ea0d5a55b0d5ff5e5e752401f523078252a668849f029957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99465188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a667a8afb941b6e7926d90c927d3922633b7999f3a3c0f38f4463530503ee77c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_MAJOR=14
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_VERSION=14.11
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_SHA256=a670bd7dce22dcad4297b261136b3b1d4a09a6f541719562aa14ca63bf2968a8
# Thu, 08 Feb 2024 19:28:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:28:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:28:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:28:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778435e3156be38decfd358c19ad0ded29d9fa7725a9444682c8891734dc3d3c`  
		Last Modified: Sat, 16 Mar 2024 00:01:05 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec102136b127f8195c5f22d8a0ced131459389c4199e2c510e89b1046cb21a17`  
		Last Modified: Sat, 16 Mar 2024 00:00:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479b2a17d05920880d267d7b0b94dd161df6bd7bdb8c89f0b11ea54bebaf3873`  
		Last Modified: Sat, 16 Mar 2024 00:01:08 GMT  
		Size: 96.2 MB (96204621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ed85e2b2af21ba311b494342bc6fb4eb0a759834dc1f5838329c5a0711d3ab`  
		Last Modified: Sat, 16 Mar 2024 00:01:06 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a17a8181970e956b0462d73c98c260b07725774c13d682f2156a2accaa84798`  
		Last Modified: Sat, 16 Mar 2024 00:01:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3aa963ab95fc09f75f283b5e6686a4802b61cbbf01f1b021a5a3ef966bb05f`  
		Last Modified: Sat, 16 Mar 2024 00:01:06 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2be81daa295ec611a03b1800d613c68a34210b68c657b6dd487a6ae965b271`  
		Last Modified: Sat, 16 Mar 2024 00:01:07 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2e1f2bf343c91ea70a16c484fccd098e203bee0353c971dcea2fbf930fb72e`  
		Last Modified: Sat, 16 Mar 2024 00:01:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:c6d4bac63c0eb83ec787755db1b7ed786dfa2f603df2f88532f9ea85004cf284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.8 KB (994782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b75a1b33c6fefbe7655f5a021014472527df973a8f1726f7f8139faae460ed3`

```dockerfile
```

-	Layers:
	-	`sha256:b485b4b7517ad36577b1d1dffc556142ad7753e44ac0032a97bd457600c4b348`  
		Last Modified: Sat, 16 Mar 2024 00:01:06 GMT  
		Size: 957.3 KB (957288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3699fd9aaac959d4e22895b7725f7eef319b015b20a5d12b7da796226878ae9d`  
		Last Modified: Sat, 16 Mar 2024 00:01:05 GMT  
		Size: 37.5 KB (37494 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:dc36f6633a8a0706205793cba7d71cb4be7eaa01f6b2e74a7db9a776282c69dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98737599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cab40f6a1cbb31b7502c3d68087f13b94f7251b20e898c300adde078d52641`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_MAJOR=14
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_VERSION=14.11
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_SHA256=a670bd7dce22dcad4297b261136b3b1d4a09a6f541719562aa14ca63bf2968a8
# Thu, 08 Feb 2024 19:28:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:28:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:28:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:28:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad450287b1da6731acbc30aae17fcadfa786da2babc8ce51fc6eca315000e31`  
		Last Modified: Mon, 12 Feb 2024 23:24:16 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a37cd9eb8f983e054e3ac505f5623aff726d75841ce8d158ba1e6913077100`  
		Last Modified: Mon, 12 Feb 2024 23:24:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16793221097d95a4551954ae0828abc0e91f1713a64d70b91f58c7c88678642f`  
		Last Modified: Mon, 12 Feb 2024 23:44:37 GMT  
		Size: 95.4 MB (95362752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749058777ffb364556c885532c15af2c84e1f26818744100f749ddcf663cf460`  
		Last Modified: Mon, 12 Feb 2024 23:44:34 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69ebe7d3d5581dd547dd41051389036816c4151681426bb10d58b388dd8f644`  
		Last Modified: Mon, 12 Feb 2024 23:44:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d296e0404a3ab0e3f68e700cf145fda90c9a0ab84ff6b91a4e1f9db2fb4e7c36`  
		Last Modified: Mon, 12 Feb 2024 23:44:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a0c1d7ac0b0ca87119872449c60ea57c3135bd9358aa4f433e62cf341a3864`  
		Last Modified: Mon, 12 Feb 2024 23:44:35 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25a018cbdc817216e30d4cdba41315935446cdc041e2c609f79076f39b79a09`  
		Last Modified: Mon, 12 Feb 2024 23:44:35 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:d4acd0f5585c70e0887e93a43190461ff6e2af921ea6808ff9e0532f69e3822f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.7 KB (841725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee62c372dc50058265dcb6231c55bf1031bb8550f7f1376143de22f1ef4da1e`

```dockerfile
```

-	Layers:
	-	`sha256:8d84368e8d67e57b284523a15c159d994b44ddee8205785dc24f3a8912bdf57c`  
		Last Modified: Mon, 12 Feb 2024 23:44:34 GMT  
		Size: 804.3 KB (804306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c11ee143b7f95f8f0a5088114dff202f3a5b25938e3aea8cc9618bddea8f3d8d`  
		Last Modified: Mon, 12 Feb 2024 23:44:33 GMT  
		Size: 37.4 KB (37419 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:42a3457b0270f77b31eb35de1b04286553c36eaeef7a4807d94e30baf67d065f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103074966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31bf73baeed9f4401c39224e40ff3f344491b55cc621ce6fc748f9d64c3d224f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_MAJOR=14
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_VERSION=14.11
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_SHA256=a670bd7dce22dcad4297b261136b3b1d4a09a6f541719562aa14ca63bf2968a8
# Thu, 08 Feb 2024 19:28:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:28:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:28:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:28:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b574fb7062f656c15df3e24f10aa7c2933845cca8a9782da63d431d96397af`  
		Last Modified: Tue, 13 Feb 2024 21:23:54 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e10a6d15ccba05f4410b4adddd3cd30b817458b98b69829386bb79c0badb04`  
		Last Modified: Tue, 13 Feb 2024 21:23:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92793b04a8e071c650c1be3b200ee183b5ac4435fbccea39b70d6068368167ed`  
		Last Modified: Tue, 13 Feb 2024 22:30:22 GMT  
		Size: 99.8 MB (99815847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc758f71c4d21a42490d9f7507d36de9d9403268fe2d1059b1f46fd4c42a5cef`  
		Last Modified: Tue, 13 Feb 2024 22:30:18 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad8a40a6dd351c0361ddf3ad4eb7ca7036a1c6a1a1bab0dcf0b42829fb997f9`  
		Last Modified: Tue, 13 Feb 2024 22:30:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a9c620f027c708f145381372b29c5fd82b4d450509f8905be37f4943a3326`  
		Last Modified: Tue, 13 Feb 2024 22:30:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4084189f622ad0eecf33e96bb4c9afd4785c974d3119519075bab3827fc5d326`  
		Last Modified: Tue, 13 Feb 2024 22:30:19 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d1f1540b023d1247d095551c8d5a5a8c5b5bf2f195c526677053d1d25c960e`  
		Last Modified: Tue, 13 Feb 2024 22:30:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:f5121522472f9006346515b33ae77cc78cf24217683881d3aa909d57fe02ec54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.1 KB (843056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd567b2cc265e1657c350b81c83c76b536b6b49127d93c4a24e29a27fe59b04`

```dockerfile
```

-	Layers:
	-	`sha256:7bfbf184ed571cfba009b6c8681532fc86c6a9b9129019676a3825f0be79786d`  
		Last Modified: Tue, 13 Feb 2024 22:30:18 GMT  
		Size: 805.7 KB (805687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:866b2382f36eda03dee5c7f2027838414224ce813f0bad80aae4dcc842d4ed0a`  
		Last Modified: Tue, 13 Feb 2024 22:30:18 GMT  
		Size: 37.4 KB (37369 bytes)  
		MIME: application/vnd.in-toto+json
