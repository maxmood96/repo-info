## `postgres:17rc1-alpine3.19`

```console
$ docker pull postgres@sha256:351ee137a7c92e6b68bae3cfe1d61ece2ba43bbb32f6e93e18d75e810f110ffb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:17rc1-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:6eb9e3e15c54fd883a70507180c55b484b195b544286923006bb6629300ab895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98490703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f393fa228227613ca840b9907340576bc5baa1a215c2ac4ccadd7d70cece547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92880c2baf59ed2b2161ddbd42912f3c667f88b880b2bf7c544e35241839cc4`  
		Last Modified: Thu, 08 Aug 2024 19:10:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61abd44f0f6a377f52eb7c5307b260122a9190bc60a8ebc1db65d929f490cb8`  
		Last Modified: Thu, 08 Aug 2024 19:10:20 GMT  
		Size: 1.1 MB (1086692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21943bc7459562df4e4ae8e8ea69b3ff99c293c0116d815e0b7f530233d4ba1b`  
		Last Modified: Thu, 08 Aug 2024 19:10:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c4be6c4e356047b611748f8bfaa609e63017f7f3ad4ee3b57a7a1dd40bc061`  
		Last Modified: Fri, 06 Sep 2024 21:20:28 GMT  
		Size: 94.2 MB (94211173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0568004cc32c25d1381304e2d4a2988ec951bfd3491ff7dc3852bba64ada9778`  
		Last Modified: Fri, 06 Sep 2024 21:20:25 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf80f3bcd4b0412b9a6eddeee4cd74bc18500647f2aae8b6c3d5ece74b92f543`  
		Last Modified: Fri, 06 Sep 2024 21:20:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdc574f92caa9a72696a4c4af0e734258e7c8268ef699626dcdc41108178567`  
		Last Modified: Fri, 06 Sep 2024 21:20:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c632953d00188263af054667f0868e7e1a31a1c3d0e6a3c8fd186c045f89e41d`  
		Last Modified: Fri, 06 Sep 2024 21:20:26 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2ce21d3a02686e190d75c7634e6d9200ff16dcea8d26880dd2ad481cbd306`  
		Last Modified: Fri, 06 Sep 2024 21:20:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:1e0d5fe1384168e384cde6d40d4dee50e7b462fe6cfa36a5662ae8264d472ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c54b8f64878c53380ad5690fbb69805ef9af4c6a16743abb13d5a639166007`

```dockerfile
```

-	Layers:
	-	`sha256:076c17a61033ab9ba20036702e3a33a926a417726deaef0933487e013d91cd50`  
		Last Modified: Fri, 06 Sep 2024 21:20:25 GMT  
		Size: 42.0 KB (42002 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e1b589fa33566938ce272be6be3dd27ef4318261d441509fe641fccb8cfd88dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92768549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3c0cc4434b1464c00976166784c6532d82bf492cb77839825bc38d56417f6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0f39bb28afed2754cc957595093611971b8c831fa34bf2ac61f96975f1bfc`  
		Last Modified: Fri, 06 Sep 2024 21:41:47 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315e430038474520dff8f5e3a46f8b423ad49d18ab60a179724c9e60493e81b4`  
		Last Modified: Fri, 06 Sep 2024 21:41:47 GMT  
		Size: 1.1 MB (1086689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba783d429e7f00120af8501a3064f7934aad1c5be99e501a3bd87b834604ef63`  
		Last Modified: Fri, 06 Sep 2024 21:41:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4edc6643d5bb8bd0fc06ca020a25b2f543a9a7468927fc42ced2784855c8c4d`  
		Last Modified: Fri, 06 Sep 2024 21:41:50 GMT  
		Size: 88.7 MB (88737586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa22168b333e40b9ff68dcd9766afa39d133e5473ac48f2b87327f7f811e8dab`  
		Last Modified: Fri, 06 Sep 2024 21:41:48 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2657bc75d994ffb661c5163d24ae60b322d4883f236bc75f861c1d1c728f62bd`  
		Last Modified: Fri, 06 Sep 2024 21:41:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6017cada688f85916432bb69718fe523718b3002ea2caf26e69ffd660970f9`  
		Last Modified: Fri, 06 Sep 2024 21:41:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe49296b97bcb55fda26ad9a049c7520aa883c119e9ffd86d62579a2a75330cf`  
		Last Modified: Fri, 06 Sep 2024 21:41:49 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69e028a4cdef84e5b5b169fdad4b102e7ff527c7cfb598bc01e92d21d0cd829`  
		Last Modified: Fri, 06 Sep 2024 21:41:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:e7887e021e93146830e37fb9958e43fb526a79c3e5fb5832d0c03b1d793d9d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909350326068c1fe4ce42c47bbb001c13ab07da88c3711f670d5e84746122278`

```dockerfile
```

-	Layers:
	-	`sha256:8bf9ec713aceb2d19f04eea85141b0d76829dd4068a2cf585ce320485913bdb6`  
		Last Modified: Fri, 06 Sep 2024 21:41:47 GMT  
		Size: 968.4 KB (968381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c49d09eaac74291aea080f6f7e76e5c5adbd6c670469a464d0fb21e055f60d4f`  
		Last Modified: Fri, 06 Sep 2024 21:41:47 GMT  
		Size: 42.2 KB (42221 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:6c65fe828a5d9d82cf7840bcc9c9e555428b33ff764b44bc2de939fc6076c343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105292592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e894e03c01928cd94d48f7ebcc93bd202b3fc5d2e594129b33067941e9be83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf0bbd8bb5be10afbaffd340a659969549de57b4f6c298b532642660ff5ca3`  
		Last Modified: Fri, 06 Sep 2024 21:04:57 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d02c467704e8fdc33bf3d0c0920228f769e8550edf1531f8865063700a7ac4`  
		Last Modified: Fri, 06 Sep 2024 21:04:58 GMT  
		Size: 1.1 MB (1095464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9c74865efcc8bf932ca75d7a570a88f204b7d24a0a37d79ae6d0b335e20d3b`  
		Last Modified: Fri, 06 Sep 2024 21:04:57 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619f31821a6af148db3c8626cfabfe9253ea27f156c763f86f8f67cd737dc1d`  
		Last Modified: Fri, 06 Sep 2024 21:05:01 GMT  
		Size: 100.9 MB (100927373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50987e5a3579cb7ef5153ffb1bb77e143d1e5d0fcf7491f2fefe076d43ab269`  
		Last Modified: Fri, 06 Sep 2024 21:04:58 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9231bdf7e6857ae66f48bae06d2b763fcc08a20c14ebee04e8f76a93d2299a5`  
		Last Modified: Fri, 06 Sep 2024 21:04:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c134de2fba0732b7e8b40f953a2596121f0e25b54f9266f8c88eba612302e6b`  
		Last Modified: Fri, 06 Sep 2024 21:04:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673575447774b9040f1e1024089e60614be5b662783e8587989849441e7aaebe`  
		Last Modified: Fri, 06 Sep 2024 21:04:59 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fbacf5d7a8aa3155dd7cb2b0afb6a2662f0c05fe2a2759f967ce52269d3c82`  
		Last Modified: Fri, 06 Sep 2024 21:04:59 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:78415a4ed31a914b152a2b9942fe7df616e78b1ee15ed27e1e7e04ce1ce53ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc65d0a827216a8b1bb0890335d5ed3fb0a59cc6cc5feebdc8fba921ae078c6`

```dockerfile
```

-	Layers:
	-	`sha256:46699378af1ae31a0d8bdf6587a686a9c82f49d84159a569664d779529340b93`  
		Last Modified: Fri, 06 Sep 2024 21:04:58 GMT  
		Size: 968.4 KB (968359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbecddf2112713d4523281eb2529a6c845d59f88654a0ddee4f36eb95c4f213b`  
		Last Modified: Fri, 06 Sep 2024 21:04:57 GMT  
		Size: 42.1 KB (42062 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:07ee88565f288decc9590ec3ab95291f04d19cefa4d7f91d162018239978fcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104640872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa83b0c7e980f3e9c9607799f480bca6a71dfa1fa3743d03a584bcbe89f36789`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eba07a513bda5303f3c0fe041ed1e6984cf9766efc81c75a5ae849064172eca`  
		Last Modified: Fri, 06 Sep 2024 21:07:54 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca479aa90fdda752d23891f005652a316eba71338b7e8c250e0aa80689c68e6`  
		Last Modified: Fri, 06 Sep 2024 21:07:54 GMT  
		Size: 1.0 MB (1039685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5983a5e5c42994ae9b5cca06affd9b3ea5d234451eb1b01a1ce8f55b9836127`  
		Last Modified: Fri, 06 Sep 2024 21:07:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a6977b50bfb97867e9b65b95b195e10a4341802024cd34fe8bc66cf3935ea`  
		Last Modified: Fri, 06 Sep 2024 21:07:58 GMT  
		Size: 100.2 MB (100220925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58f6b5e6d0f0d5503fbc301165a21c942c4d8d4079ec1646d282428cc8d55bf`  
		Last Modified: Fri, 06 Sep 2024 21:07:55 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b2273f2c95071beb62109eb63d233fb6ab0cf11130fb5b3d0b85e6948ef44f`  
		Last Modified: Fri, 06 Sep 2024 21:07:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53845ef86bafbd7cb11ee362247c52875f2114d1675dddcebc07f02d91a8679a`  
		Last Modified: Fri, 06 Sep 2024 21:07:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c2ffa3f72381e85741773796cfb1fcd3ae8c849171708891d26a99c7940de3`  
		Last Modified: Fri, 06 Sep 2024 21:07:56 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7590352b0de849696282d187d09c48707135870493a737e33050781a5172358f`  
		Last Modified: Fri, 06 Sep 2024 21:07:56 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:ea8e04d4c2afa0ae8cd19e821db975630850eb3f2449c7bd68aee5b1ea8c23cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77c6ade69b218efdbe15f653ecb3f791a4ff8d5ff44c0de15808c1123c1c9e8`

```dockerfile
```

-	Layers:
	-	`sha256:135c60327479c9e0fd0ea4a7ce4481e8b327150e84747150b15b78c2200fad6a`  
		Last Modified: Fri, 06 Sep 2024 21:07:54 GMT  
		Size: 964.8 KB (964767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4cf6b9242635d394ff9e34c9784a5f871da2eba21fcd3427974c44ed07bfb7`  
		Last Modified: Fri, 06 Sep 2024 21:07:54 GMT  
		Size: 42.1 KB (42124 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:2b69772b7d432c73ba406398ce2ab4b7a73440aa7737abc404d6a33f4e34faba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108805776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699c1971e2b7358145b94cadde7c10b8a90745d126cd1c5005f16dbcde551b8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a43099caeafcca0da8c355720cb2ee834fe7ec4799e7cc8911826e927f4d8b`  
		Last Modified: Fri, 06 Sep 2024 21:07:43 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa02510b64b707625920ba2a89eaccdd2a3ae96698c85bd535175d9edf6bc50`  
		Last Modified: Fri, 06 Sep 2024 21:07:43 GMT  
		Size: 1.1 MB (1083896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9449788e21589d710b2d3ef2fc3dfd50d4ea7d7dd889d0e133ab63b292c1a33d`  
		Last Modified: Fri, 06 Sep 2024 21:07:43 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47b60d7cc635d7fa5863f428cd555ce8e697e5d68ec8ef9fd6ba8e1744c142d`  
		Last Modified: Fri, 06 Sep 2024 21:07:46 GMT  
		Size: 104.5 MB (104451651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361a26e1aab8119679c4eb704cdfecb601334187c39b44a3c8836f018b2913cc`  
		Last Modified: Fri, 06 Sep 2024 21:07:43 GMT  
		Size: 9.9 KB (9878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fc1e70deaca6cad5ea0b77fe238ea46a093465be62c9ee32341ffbcd1fb0f7`  
		Last Modified: Fri, 06 Sep 2024 21:07:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508792e0d56371a1f791b09cd26e47468e7b61b8527619d8e2e37b4465cd7f7`  
		Last Modified: Fri, 06 Sep 2024 21:07:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f88e3a1152b25017d66e6c4404e1c7f0611a5d4f82b3b5efc8e7089cb30f5f`  
		Last Modified: Fri, 06 Sep 2024 21:07:44 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bee9dcbb3d520bb70f033ee0a820bfacd900533f08b9f1c30bf54f44830ab9`  
		Last Modified: Fri, 06 Sep 2024 21:07:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:20e5be255ab3456cf82ed1293453f5c2dfb80d01007ce3375669ef1388713397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1008505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e21028b6a23c5c56791f6410749359c1a13e9d090c68c02bb3ffdce889bb13`

```dockerfile
```

-	Layers:
	-	`sha256:1fceba9a862fecb9bf8b3d82d0649906a5fe39482f0af9fb7484e261ba1a02d5`  
		Last Modified: Fri, 06 Sep 2024 21:07:43 GMT  
		Size: 966.4 KB (966415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f90ec218c1a803bcc3cb493190a4e22d90c76de4a34db4c7380580891dedbab3`  
		Last Modified: Fri, 06 Sep 2024 21:07:43 GMT  
		Size: 42.1 KB (42090 bytes)  
		MIME: application/vnd.in-toto+json
