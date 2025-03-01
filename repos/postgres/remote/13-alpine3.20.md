## `postgres:13-alpine3.20`

```console
$ docker pull postgres@sha256:6130d065306ebc6cb35cb4c1b63db837744a922744948fd4a5bd6be2ad4f090c
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

### `postgres:13-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:2c66342686deb399dc3e3d5c94d0c89b0daea600de1e8e6d899c19f49e8e4858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94000449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50884de9a826d0a5b87b8dbb9b56a7647645dccc8777128dbf898ad79e164df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=13
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=13.20
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_SHA256=8134b685724d15e60d93bea206fbe0f14c8295e84f1cc91d5a3928163e4fb288
# Thu, 27 Feb 2025 00:53:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b2c384b4bbefa6191f4d3e95c9649fd0d523a5727f16d4bfaf915708955ca8`  
		Last Modified: Fri, 28 Feb 2025 23:29:01 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce189ccf2c8f55ba2de173129c12d389f9fe79c1f98743083b6ce7c85c1e68d3`  
		Last Modified: Fri, 28 Feb 2025 23:29:01 GMT  
		Size: 1.1 MB (1120287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c9e0469b08d7c7505f52c2d6bd28fd09798c285c6f5769f6db8f686053f245`  
		Last Modified: Fri, 28 Feb 2025 23:29:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09acd1a8ea8b4b76580de7437694287c1ae563a9d59614a4bb46ef0d5517a5f3`  
		Last Modified: Fri, 28 Feb 2025 23:29:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2194fb2b544e83fd9e503a4f94813b56ac47a9abe418afa5767ccb8a24dfd86c`  
		Last Modified: Fri, 28 Feb 2025 23:29:03 GMT  
		Size: 89.2 MB (89237011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b180216ce326a54c4169e99cc0bd2f20ad6fabca7c7c5ac9fb799893457d7ab`  
		Last Modified: Fri, 28 Feb 2025 23:29:02 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f7be5b08f41d53fcc5b53773667f9aecac3db35a1d38ba33990ace8aaf65c6`  
		Last Modified: Fri, 28 Feb 2025 23:29:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96eab53bbfa627b500b38d154a24d9dd504cb609b51429e22045ca8a885f42f6`  
		Last Modified: Fri, 28 Feb 2025 23:29:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ea20e9be08670b5483dcde938256158e96fa7091a715ed110d4754df205485`  
		Last Modified: Fri, 28 Feb 2025 23:29:02 GMT  
		Size: 5.5 KB (5476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9368d55782c27975f740237865a2d6767eafa1312bc7181cbe2068b6aefb262e`  
		Last Modified: Fri, 28 Feb 2025 23:29:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:38765e5bc5e6704ccdd655102b69fd047a362fcfa6e957f8ecd7899a80f59d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.8 KB (630780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e688857a218a9f94831d9efbebc8cbc33da3466cb26a27454457da3b8fd1934d`

```dockerfile
```

-	Layers:
	-	`sha256:c770b6c50c5593269732593ddf6209644931d5c508c93ad680e6744207aa4ae6`  
		Last Modified: Fri, 28 Feb 2025 23:29:01 GMT  
		Size: 586.6 KB (586581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c354d99c54f21f12a9cd007076de5d736b2b99c19279bc25a63dee09f620deb0`  
		Last Modified: Fri, 28 Feb 2025 23:29:01 GMT  
		Size: 44.2 KB (44199 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:6381dd8037cbff412045c397301632fcf2ca74e18c6aea10acdda7624c91adf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92764847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3bcccbdd93346a0689b6efb29e0ea0a71ff4241f645543fd03e6d97e41c800`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=13
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=13.20
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_SHA256=8134b685724d15e60d93bea206fbe0f14c8295e84f1cc91d5a3928163e4fb288
# Thu, 27 Feb 2025 00:53:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f562bdeccc677affba17117a3e71eed437842fbd24407b2ce425aa5819d3dab5`  
		Last Modified: Fri, 14 Feb 2025 21:36:18 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c15f54b7c7b9df1d9b4f973855ca80d075a47a5343b27c0f6e4ae7774389b5`  
		Last Modified: Fri, 14 Feb 2025 21:36:19 GMT  
		Size: 1.1 MB (1086525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568e84a40aff368bdcb0f2c0209c899ecf6614f22d843f7855cc038d42ed61d`  
		Last Modified: Fri, 14 Feb 2025 21:44:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464e90337bafdf4dac44e92da85d96c873b18c4c579abd3dd0ee24ba0ae61dc9`  
		Last Modified: Fri, 14 Feb 2025 21:44:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47038ca44cc740e5d5ebbe92ca17f2175c3acd4de37c882792d81a8c326db189`  
		Last Modified: Sat, 22 Feb 2025 01:19:40 GMT  
		Size: 88.3 MB (88289542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8054383bb751e531d0bd6f5fa0174d549b7bf7fd8be4248ae4bceec592b35759`  
		Last Modified: Sat, 22 Feb 2025 01:19:37 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6e777c7b6ff27a94e91ba596f5385d5319b80885dd214c21c36afd67d2505d`  
		Last Modified: Sat, 22 Feb 2025 01:19:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fd3183ee7eb4f7d404d261f04dcf2b30f83316354465599b37e5b67d4ed4ef`  
		Last Modified: Sat, 22 Feb 2025 01:19:37 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df1f42f75ce910e29746cfd4172989a4e23b45dddb9950b9c8680cb9e6c6845`  
		Last Modified: Fri, 28 Feb 2025 23:26:03 GMT  
		Size: 5.5 KB (5476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0655ca6e0586810b749f92299e2efb276e7e1eb6af1edb2c553d3765111ec47`  
		Last Modified: Fri, 28 Feb 2025 23:26:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:1dfe0e820472d2b3946dbcd096fb47d47e5b6f6c754806f0ba7b3ddee8f0850a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 KB (44149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0ca2bd0dd59632b5067cb2ce2d9e4c356c5817489f684b24ff302b52c4537d`

```dockerfile
```

-	Layers:
	-	`sha256:aa7ab27e0eb7580683e26a5fbbc84a747c2e330d2d2be4fb381b25fb181a0531`  
		Last Modified: Fri, 28 Feb 2025 23:26:03 GMT  
		Size: 44.1 KB (44149 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c41a6a73c5afd9817526466e36ab1ba269da0066cbba2cbd6113fc576b968576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87227898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c2b9b744924448b9567d22887c6030eb4b83a9fc3aeabfeb345f04348ad244`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=13
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=13.20
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_SHA256=8134b685724d15e60d93bea206fbe0f14c8295e84f1cc91d5a3928163e4fb288
# Thu, 27 Feb 2025 00:53:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25896e659de9add0d4b908897850cbf64b7928b4104747d7d2f865d03c785b5e`  
		Last Modified: Fri, 14 Feb 2025 21:14:39 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f74483a18f569a1fa2c939344a028b1612c307bf93662a4fdaf02c3f961ae8e`  
		Last Modified: Fri, 14 Feb 2025 21:14:39 GMT  
		Size: 1.1 MB (1086514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eadf93718700a6ae0148ccbb835c2325930ee0d12ad9dac188ce36572109a18`  
		Last Modified: Fri, 14 Feb 2025 21:22:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b8c5e4ce7a3e3769bc68c603e910cda8c227d7c7644ade020fd071c0811efb`  
		Last Modified: Fri, 14 Feb 2025 21:22:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13da24fe7b5c2f9b59a97b439fcccbc96133ce8a4734bc4731ef9e430d8fb67`  
		Last Modified: Sat, 22 Feb 2025 04:25:14 GMT  
		Size: 83.0 MB (83029161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7bf9a56aa35ca30bd4718ac4ed605de9fb8405de612b6b208c7a0e615044ea`  
		Last Modified: Sat, 22 Feb 2025 04:25:11 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78de2181b1b7346c537063188cad860ba0263f4ac95e2174e6b63c64ba560207`  
		Last Modified: Sat, 22 Feb 2025 04:25:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab7f11ca9a1eff07d56ab6f8720443fc4215cc86d498c3f9724c5b79cc61213`  
		Last Modified: Sat, 22 Feb 2025 04:25:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3356885f579a30ce034dbad6fecced572570daf95fe64a8f9fbb94b49af07b`  
		Last Modified: Fri, 28 Feb 2025 23:31:57 GMT  
		Size: 5.5 KB (5475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5043f4f534f514699b575a343d908c79fefb0e7ee9f35883494df7a117144ada`  
		Last Modified: Fri, 28 Feb 2025 23:31:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:f0b4d61f58b57d316773555a5f0af739e8fd293c557e5615dfbfd09109f7862c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.0 KB (630965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd92140e14df26858f150785808faaa52748f9e086517ba82cece9a23a13149`

```dockerfile
```

-	Layers:
	-	`sha256:8dd96c2e20ba3115de165df27af9c8a3753f8281e411ec96a4adc82822f3c1e5`  
		Last Modified: Fri, 28 Feb 2025 23:31:57 GMT  
		Size: 586.6 KB (586601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbe64240b7a394ffa68e4d0a1f5eb4e55e78f6d8d259903021140dde0dc02ed`  
		Last Modified: Fri, 28 Feb 2025 23:31:56 GMT  
		Size: 44.4 KB (44364 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:ede098197621d80714d306f45cd3451e334f6078ab22fe84dbe6baec58459882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93256575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984799eeea37917674a2a713b3f8ccef4b1b11f15a32697f666aef45673f0a41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:02:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_MAJOR=13
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_VERSION=13.20
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_SHA256=8134b685724d15e60d93bea206fbe0f14c8295e84f1cc91d5a3928163e4fb288
# Thu, 20 Feb 2025 19:02:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:02:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:02:25 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:02:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc8827c16e8ec088d48c0b753a38f9b70fa76626b8e70929dbb63cf84cc89b5`  
		Last Modified: Fri, 14 Feb 2025 21:45:38 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0907d060ed36b58b8341b1b05e996014c48ca9a918bb7414420e2e27fa4bc054`  
		Last Modified: Fri, 14 Feb 2025 21:45:38 GMT  
		Size: 1.0 MB (1049755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36da590e94d03388333c8f90ebc9ff573b76757ec31fc8b18a031f6350a39911`  
		Last Modified: Fri, 14 Feb 2025 21:51:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba3a5783239b116fcb925eef91e91369b4580402ff73a02ffd413615c3afcf0`  
		Last Modified: Fri, 14 Feb 2025 21:51:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52f10f40ebfdf87211f12852264aecd759b73caad684faa8534d56a5c488c3`  
		Last Modified: Sat, 22 Feb 2025 02:33:28 GMT  
		Size: 88.1 MB (88099475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c334c6a5461da5965422f289134dfa5a5590f7f5cfcd2f5fdbed07810b398d`  
		Last Modified: Sat, 22 Feb 2025 02:33:25 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0f404242508005fef04847099a1f6a6d49d1d13890c7c597c526e848b5eef6`  
		Last Modified: Sat, 22 Feb 2025 02:33:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a953b58834a2435aef1f7cd5a36b657c9d03b309a728421cdefde61496f35a8b`  
		Last Modified: Sat, 22 Feb 2025 02:33:25 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aefb282536404c14e1e8ce09ce4cbd82765c226cc9d4e07e399183e807a09fa`  
		Last Modified: Sat, 22 Feb 2025 02:33:26 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a30215fc2dd1372b6f34af9fcd89bf2887a9629d45b40509b2729cdef354088`  
		Last Modified: Sat, 22 Feb 2025 02:33:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:e779c5dcd5a41466454a27e2ba34aa9fde17f0ad07cc8acc5d287e05e4e425d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.0 KB (631013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f42c11b243613fb0fe1a5007f1be81aef1f2fdd0adad2a3ff72f755687099e5`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3c6215954a17131134ab4a2d35e34aac2bbbf46536a0695d5cc7c661617e0`  
		Last Modified: Sat, 22 Feb 2025 02:33:25 GMT  
		Size: 586.6 KB (586613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35452c31e69653c7c610c3801c1dce50458f81ffa6841c7ca15dacf112789e9`  
		Last Modified: Sat, 22 Feb 2025 02:33:25 GMT  
		Size: 44.4 KB (44400 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:80e36254afacf6464df6140904cf44a106d58b0d1daa844401c585bf373d31fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99258688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd38f27945f847aa0eceb8fcb5a371da8cf305afe65ee4dcdf79c55c85906b63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:02:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_MAJOR=13
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_VERSION=13.20
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_SHA256=8134b685724d15e60d93bea206fbe0f14c8295e84f1cc91d5a3928163e4fb288
# Thu, 20 Feb 2025 19:02:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:02:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:02:25 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:02:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b18939edf1319d5129aa9e3ab7104d226f274aa8c6e26915a0c7057a5208b25`  
		Last Modified: Sat, 22 Feb 2025 00:32:38 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5081065ef7b6edbe83051a1485f1cddcd713c93b1fa04740e14bf244e454506d`  
		Last Modified: Sat, 22 Feb 2025 00:32:38 GMT  
		Size: 1.1 MB (1095377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62121d79d3fd53b9d03c43bcd61285ad62eb45543d17596e33e30a9eafbdb908`  
		Last Modified: Sat, 22 Feb 2025 00:32:38 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4efe6060b371b00b487f058e4712fe669dc72d3f0317c7b69de42c46d2ca9d`  
		Last Modified: Sat, 22 Feb 2025 00:32:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d498aec6ce98cc4816810e84a27aa9c5733e357d38447cca961017427736a667`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 94.7 MB (94675460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d9b48fb27f4d21091235dd8d947fe8910d0eb5c6eb5191b2537c60a1cfa5ec`  
		Last Modified: Sat, 22 Feb 2025 00:32:39 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc07dc343023b66824cff96273ce6b68bbaee2c154b73d8dacb5ba00fab1710`  
		Last Modified: Sat, 22 Feb 2025 00:32:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60acb0661d7ff723ebb0227b8c90905de64cec0b20c4ba040e58f63baddf144d`  
		Last Modified: Sat, 22 Feb 2025 00:32:39 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069c4bfc86505ca13c604ec1890371386dcaf8bf3e2aa89d86a9a8814acd70bd`  
		Last Modified: Sat, 22 Feb 2025 00:32:40 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3496c8d6b5b0f415e757405bec578ef1cbe706d78faf5e1a93bc3085bc85a6b0`  
		Last Modified: Sat, 22 Feb 2025 00:32:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:a39421dc913da27bff9687d139858f3109b579e04d45ce1d1eee13028cd6fe10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.7 KB (630728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd483b4f95f9f19c02bf978d4519fb8e7579744e3c2a92309bc512fe1afd969d`

```dockerfile
```

-	Layers:
	-	`sha256:708a18e0d4953057f1985ef5d6164b776c57b41755b3b55dbb92c086fd5ff07a`  
		Last Modified: Sat, 22 Feb 2025 00:32:38 GMT  
		Size: 586.6 KB (586566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62973fae56f227af72c51d2e6316a9592789623ff233d5d52538e9e8b90031c9`  
		Last Modified: Sat, 22 Feb 2025 00:32:38 GMT  
		Size: 44.2 KB (44162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:ec31f4f52b561b0ee76e814ef26fde71bfd0753d688681cf48bcfc4b83772580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98401270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c68e46df0cd22ae170e6253f0b42717dec5df72fff2a9d8c3761174d68d400`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:02:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_MAJOR=13
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_VERSION=13.20
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_SHA256=8134b685724d15e60d93bea206fbe0f14c8295e84f1cc91d5a3928163e4fb288
# Thu, 20 Feb 2025 19:02:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:02:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:02:25 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:02:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4560e6eaf6136fe9ed082dd565c5a37bb5ec3e433bd72a01116ae44bd04994e`  
		Last Modified: Fri, 14 Feb 2025 21:17:16 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a2d29dc8697219ebfcfe5e6e5c56b2549f8e69e4f3f0bdf9803dcbf630c294`  
		Last Modified: Fri, 14 Feb 2025 21:17:16 GMT  
		Size: 1.0 MB (1040018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db695e36d82284dfc46d1fed4f570d9a812b952a1abb41603b09ccb4565b2b1`  
		Last Modified: Fri, 14 Feb 2025 21:24:21 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120127792b9f26a99d1a9584a1747e461b88ea90bd0e37882e377a843cc7930d`  
		Last Modified: Fri, 14 Feb 2025 21:24:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e920d5e16f575273ddaaef1568b5d196047f6735d3b3705c28f4232514d8c3`  
		Last Modified: Sat, 22 Feb 2025 01:17:50 GMT  
		Size: 93.8 MB (93769381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0d4e59a86a84453ae145bc103a4f4e4fc1360b8db887ef43fe10405a266f41`  
		Last Modified: Sat, 22 Feb 2025 01:17:46 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6326c13079e5c680d26277d219c9d87423f56cfc72ae0837e1a4fdc28e171e8a`  
		Last Modified: Sat, 22 Feb 2025 01:17:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f8363baf78b17f68613afe708a78bea486437ed514f5e70b5c896d2c810f09`  
		Last Modified: Sat, 22 Feb 2025 01:17:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d7dd771c62c28ceed8833e2af2d7b357daca46e8eaed8eb22e274a4d248047`  
		Last Modified: Sat, 22 Feb 2025 01:17:47 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d355ee2ffacd978d03be0b4bff5b6d8fe8a08651b4516c36e9e7a78ba27c28`  
		Last Modified: Sat, 22 Feb 2025 01:17:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:9194a3b873292fb384da4a8249375ad125585c0ed13b5c887c210e7d7d2d4a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2083163c23c21019cee25627d79196c172d049baddfb2f9dadc18315af7413`

```dockerfile
```

-	Layers:
	-	`sha256:5ff2033118a61a61aa900b0bb75822c585593613406e25161a301f5ace2702d1`  
		Last Modified: Sat, 22 Feb 2025 01:17:47 GMT  
		Size: 583.0 KB (582990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df630188268d1351c3a4b042134dbcc85844a410b68b382335c357008d96ebe`  
		Last Modified: Sat, 22 Feb 2025 01:17:46 GMT  
		Size: 44.2 KB (44248 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:046684311d776dd08325723dcf9e3aa84e13804a113523d8862bb971a6ec83c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94142437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504d3f3d53112f054d36974c3de6bec594913b332e4b287cc79723bc58f4a36d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:02:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_MAJOR=13
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_VERSION=13.20
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_SHA256=8134b685724d15e60d93bea206fbe0f14c8295e84f1cc91d5a3928163e4fb288
# Thu, 20 Feb 2025 19:02:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:02:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:02:25 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:02:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a667969f118faf629e202aac4ad97cc21b7c3811a145f4275dbf42e59555a`  
		Last Modified: Sat, 15 Feb 2025 22:17:56 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebfd62b87648c7ac5476d245882fa59a55ae434a2214feefa5b371c5fd1aa34`  
		Last Modified: Sat, 15 Feb 2025 22:17:56 GMT  
		Size: 1.1 MB (1089587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffc75644aa9015c4524a4803b8c615bea6844883b9b28d09659887f6b8ac372`  
		Last Modified: Sat, 15 Feb 2025 23:59:16 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8547faef1dc20f0ac9c1e4a1a6905e277340905ae7669c32a1f72cdd475d64c`  
		Last Modified: Sat, 15 Feb 2025 23:59:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf003db6ccf596b429331a6833be328dee23150fa42890278da3d3738bd03d2a`  
		Last Modified: Sat, 22 Feb 2025 09:35:12 GMT  
		Size: 89.7 MB (89663406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7957a445ea9196fa108e763a4b2875626f42d6be79596d01c0158724087e1861`  
		Last Modified: Sat, 22 Feb 2025 09:34:58 GMT  
		Size: 9.0 KB (9026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c51048bc94fdd261804e2d35467e26d71c1b337a335237ea38230a6774c93b8`  
		Last Modified: Sat, 22 Feb 2025 09:34:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82216da7667f6a4e02a511beffff04fdb849d3dbd9dc47aeaca6f40e19b5c4a4`  
		Last Modified: Sat, 22 Feb 2025 09:34:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98310f1abb402b62d092c91a962c32b1d9c02ef61a905f39c1091282ea3996e4`  
		Last Modified: Sat, 22 Feb 2025 09:34:59 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfae07dd13e5423e057ea7656d319768c886ce034664726e587bd36c7fe2c95`  
		Last Modified: Sat, 22 Feb 2025 09:34:59 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:2cdd85e31971e9038cd8df0e99ff0c7aa53c19dbc5205353c67eae99587e3096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.9 KB (628896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc54ff1fb94f1e5cc742607db1488699ee90123ba86bb8a69e087d10aad9f70b`

```dockerfile
```

-	Layers:
	-	`sha256:e360c1a3c8eac6cd4836c038fa62c0e32a3dd8e1914f310498275f42b1b6a453`  
		Last Modified: Sat, 22 Feb 2025 09:34:58 GMT  
		Size: 584.6 KB (584648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed610f5016ba3876cf00e734c7f50094f0f2a68434cbd6546b08ced35e0c4438`  
		Last Modified: Sat, 22 Feb 2025 09:34:58 GMT  
		Size: 44.2 KB (44248 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:e2d83cbe514d5ff363a31653a9a51a3ca5dae0b53eba71c264d9289ffb214bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102812158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f14412918ec10c938519f88ae3883c1d88f45ae9f669fed15e8b979a1f3c22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:02:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_MAJOR=13
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_VERSION=13.20
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_SHA256=8134b685724d15e60d93bea206fbe0f14c8295e84f1cc91d5a3928163e4fb288
# Thu, 20 Feb 2025 19:02:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:02:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:02:25 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:02:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bd808fe0e001bd5a66a02c69406d4cdeb252f933c590cb4d320052ea3b3546`  
		Last Modified: Fri, 14 Feb 2025 21:44:47 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b626b09720dc73a31296f38e3ebe6c64e8a0f0170f1d84c424109e9cbbfb03`  
		Last Modified: Fri, 14 Feb 2025 21:44:47 GMT  
		Size: 1.1 MB (1084163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5bfd3e663523426c97298e108c7d05f57cc63e280ad958b0489b777f37f192`  
		Last Modified: Fri, 14 Feb 2025 21:44:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2ec1e1feb3ecea6aa9ce13b57efbf5c29523f7ac7d7955c245fbebb7d1741a`  
		Last Modified: Fri, 14 Feb 2025 21:44:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c83a3f995f60fa5494771aa29d75d4552110e558e946a5b88d4e06e30f6bd13`  
		Last Modified: Sat, 22 Feb 2025 01:20:40 GMT  
		Size: 98.2 MB (98247682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be4b296e01545454dbd57c896fcf41515dba634fa6ca830faa29b1f8de0a979`  
		Last Modified: Sat, 22 Feb 2025 01:20:38 GMT  
		Size: 9.0 KB (9019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7107e681c084e227dd99c89d90a76cafbaf4df8141701bdebbf3cf42081a787c`  
		Last Modified: Sat, 22 Feb 2025 01:20:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda13f3e090766d6ea3c83f86ef5dda54cc10c82e1f31a22719c3b0dd6e4fa1c`  
		Last Modified: Sat, 22 Feb 2025 01:20:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3681bc8c7ec2e82ffa7dc7ff3611e3f95887555f9568dd4b7440870739f039a4`  
		Last Modified: Sat, 22 Feb 2025 01:20:39 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acecd749aacff2b27dd16fc2f7a1886ea3b1a77b00ff1c87670f9239cbabe4e`  
		Last Modified: Sat, 22 Feb 2025 01:20:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:c0fca5c7b7126528ac554eb05aba0ed1dcc739cab8f1638fe51488f14f586ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.8 KB (628830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e20ba1f59cc2647469816137e5569244a42b1173c6e74b8834e5c20ad1662d`

```dockerfile
```

-	Layers:
	-	`sha256:2c879e5df177f2a9584dd52d843749f92b09d82d58ad3b8761ebfb374a48d41f`  
		Last Modified: Sat, 22 Feb 2025 01:20:38 GMT  
		Size: 584.6 KB (584630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6789b2a90b4511c564f4aefbfa0109c385f161eecc1c8e5c383fdc3596530ca`  
		Last Modified: Sat, 22 Feb 2025 01:20:38 GMT  
		Size: 44.2 KB (44200 bytes)  
		MIME: application/vnd.in-toto+json
