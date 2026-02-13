## `postgres:16-alpine3.23`

```console
$ docker pull postgres@sha256:97ff59a4e30e08d1c11bdcd9455e7832368c0572b576c9092cde2df4ae5552a3
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

### `postgres:16-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:129fbfd388241accda7b15e38ada14b11c70698e01e5c8072265b0eaa03af010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109975665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e04d274d186c7331d0e13c7c90c8b9f63b0d7ae94476c98a229a94d62c9745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:04:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:51 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:04:51 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:51 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:04:51 GMT
ENV PG_VERSION=16.12
# Thu, 12 Feb 2026 21:04:51 GMT
ENV PG_SHA256=b253ee949303ef5df00e24002600da4fb37e5ccfafa78718c6ea6a936b4d97f1
# Thu, 12 Feb 2026 21:04:51 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:07:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:07:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:07:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:07:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:07:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:07:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:07:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:07:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:07:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:07:08 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:07:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:07:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffb427686b69a212d45ab3d395b74f935308942b1cdf14680441bd6cd8e77e4`  
		Last Modified: Thu, 12 Feb 2026 21:07:24 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630177b003522c8250821d96d1593e46fc8527aee7ae58bdb1dfc31af8635353`  
		Last Modified: Thu, 12 Feb 2026 21:07:24 GMT  
		Size: 922.9 KB (922942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c18ff1f33d0f0d0baa87fa31957beccd7e9fa54e39ef4179fe829c50dddf3a0`  
		Last Modified: Thu, 12 Feb 2026 21:07:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e46e455d3b6e2afda6cdabd64609577eee48201d09db8fc9e2f90a3c341e5d`  
		Last Modified: Thu, 12 Feb 2026 21:07:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4403f29458afcf99bd5624722cc365f4561c00d91aeaea21db1affad6cfef35`  
		Last Modified: Thu, 12 Feb 2026 21:07:28 GMT  
		Size: 105.2 MB (105173697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aaa75af6ced0dc2573c61db114b07d45f376984102021af3c3c1377c2209c0`  
		Last Modified: Thu, 12 Feb 2026 21:07:25 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162bdab1e0a7a1f23a9700c3bada28d5623ce00e739a8aa42417def18b3fefe9`  
		Last Modified: Thu, 12 Feb 2026 21:07:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebff7b0ec73e7b517ebf080c88be87fc682bc57c464ccc622f8137b621fc0341`  
		Last Modified: Thu, 12 Feb 2026 21:07:26 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02179436571639d24dc3588fee138a2e9dfe7a7d1dee608b1a1634f1d1016f8`  
		Last Modified: Thu, 12 Feb 2026 21:07:26 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8243369e98669b4b458faaf8a16603579ccb8f0ecb8eaa91255e6426294c3d68`  
		Last Modified: Thu, 12 Feb 2026 21:07:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:aa5a28c2a039d7a93176030b294ccde1e71927b3c0e04afbdd4511e142a5ea48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28c14b06776def659a57e9fee739b89b0945819950081613749e0683b67a692`

```dockerfile
```

-	Layers:
	-	`sha256:1eaa8a41a070d470eac0ab74b8eb184fd68f2f088d460a3eb9b554ff007c32a0`  
		Last Modified: Thu, 12 Feb 2026 21:07:24 GMT  
		Size: 598.1 KB (598080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c68e283f362d2703e4cb630d417b263f77535bad8e7bdb465a1b5ecc4f36b8e`  
		Last Modified: Thu, 12 Feb 2026 21:07:24 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:e20f49299d78e326200a6bcf41e3bc2abf390c364919139ac77cce569be3e9bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89405152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54392ef056d0b1cefc23d037a586f13224f3395d03eecf2d5bd1aac846edb49f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:19:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:19:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:19:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:23:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:23:02 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:23:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:23:02 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:23:02 GMT
ENV PG_VERSION=16.12
# Thu, 12 Feb 2026 21:23:02 GMT
ENV PG_SHA256=b253ee949303ef5df00e24002600da4fb37e5ccfafa78718c6ea6a936b4d97f1
# Thu, 12 Feb 2026 21:23:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:25:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:25:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:25:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:25:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:25:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:25:56 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:25:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:25:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:25:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:25:56 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:25:56 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:25:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbe5e121835e3f7c5b6dd5244d1bc0956a4f2b2eef40677906f8152b8951b72`  
		Last Modified: Thu, 12 Feb 2026 21:22:53 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b66aed209904f198e42bc4ec51044961dd9ca8c9af63dfc3b05132855b446`  
		Last Modified: Thu, 12 Feb 2026 21:22:53 GMT  
		Size: 889.5 KB (889473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac25b6f79f951f1b8f34046d5c0925cce1c16cc40218f55623b2be0b4ebfb77e`  
		Last Modified: Thu, 12 Feb 2026 21:26:07 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebd0e74ca8b9e5362855c2ebaad1ab72494ab9759cff8139360e4b3815127e0`  
		Last Modified: Thu, 12 Feb 2026 21:26:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b055e0a042f9b35ac94eaca65afc951aac21694a329a64362ad39818e4b1eeed`  
		Last Modified: Thu, 12 Feb 2026 21:26:09 GMT  
		Size: 84.9 MB (84928653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30949a8cb831002736b2cc9b900d457cd51fef1d9c241a6f8c885b3d714be54`  
		Last Modified: Thu, 12 Feb 2026 21:26:07 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912ace5155362ec2702dd807ed4c42d80b6d0cdc4c5ba3e64396c63c9384d391`  
		Last Modified: Thu, 12 Feb 2026 21:26:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e5214857d0722718a8cfad8cb1ab6f2299c829702b0f4cd3f35b41a61edf0`  
		Last Modified: Thu, 12 Feb 2026 21:26:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dc03265755764faba230f748d1c9d1e484199f4dd5f088bff8b8bc9885e4c7`  
		Last Modified: Thu, 12 Feb 2026 21:26:08 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe5eb0e0d3cd86d76845e5217f284e904e23451cdf32d238509ae67e7aa5f29`  
		Last Modified: Thu, 12 Feb 2026 21:26:09 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:23d3235c872ccd31bc1b282ade0b9e95ca7d731688cca5bb9034cdad46d6653c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 KB (44268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4468235a1482ad500868e94de8b7f98a7054d6130ed563bf4546e1714cbcedbe`

```dockerfile
```

-	Layers:
	-	`sha256:9e816b74ba1c9eea2a74a8e4d82e3466c691c41307d57068572ea3d0c2a1bdab`  
		Last Modified: Thu, 12 Feb 2026 21:26:07 GMT  
		Size: 44.3 KB (44268 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:280002dc07bd45fbb599420319ea96d91e19e6ba2b511ad633014a33645ee6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84639747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544158de73145231204bb0a5a30546b5e456efe0398e0a52069ed0b272a28b55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:25:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:25:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:25:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:25:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:25:52 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:25:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:25:52 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:25:52 GMT
ENV PG_VERSION=16.12
# Thu, 12 Feb 2026 21:25:52 GMT
ENV PG_SHA256=b253ee949303ef5df00e24002600da4fb37e5ccfafa78718c6ea6a936b4d97f1
# Thu, 12 Feb 2026 21:25:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:28:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:28:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:28:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:28:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:28:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:28:41 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:28:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:28:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:28:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:28:41 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:28:41 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:28:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fc1a155db6ff110355832a48ce41604c676d73b794d9e76f5f49f6f3c6ad`  
		Last Modified: Thu, 12 Feb 2026 21:28:53 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827aaa0135fd1dd4446d8acdf70b055373219c3732facb7447ffd2f85d15d77`  
		Last Modified: Thu, 12 Feb 2026 21:28:53 GMT  
		Size: 889.5 KB (889522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01296ca8d7f6db8b294b6549050fbf6be87f0d70d99779da299119046ed887b0`  
		Last Modified: Thu, 12 Feb 2026 21:28:53 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f90b6615f91d5ec814eda52bb40539fbaddc5cca33f80b556c09046c9b2227`  
		Last Modified: Thu, 12 Feb 2026 21:28:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153fbc932e1d5a75e350a8d653b1eb59e9131dd839e6b3f7d4587e740ca15f08`  
		Last Modified: Thu, 12 Feb 2026 21:28:56 GMT  
		Size: 80.5 MB (80451298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c144cad3da6385d7ddcac9580248205a15eae9a54201e8e35bc658ac576ff5c7`  
		Last Modified: Thu, 12 Feb 2026 21:28:54 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd77544cb28ba0bfab46a4c362825b5f75080161df8aca718614cb677a5bf3ef`  
		Last Modified: Thu, 12 Feb 2026 21:28:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b972260229b7ecac6189892af5c513692e9aba4a5598065a1073c41c0d7141db`  
		Last Modified: Thu, 12 Feb 2026 21:28:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6221e9770b9b949e629622f2a7a9dba4f3290005c80a1f9acafab5d15d30cb1`  
		Last Modified: Thu, 12 Feb 2026 21:28:55 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b66dbaebf2d4487f864bedaf90e93e1bb83813e1c4feaf2b16c0352a5baad5`  
		Last Modified: Thu, 12 Feb 2026 21:28:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:dc005c33c4398b26cb7022718c84afab9d50a6a0588333b95ad29e7298f7ad51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (641950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7bd666e17f509e657f459dcb74718b9420da843075c0246ade445f19958883`

```dockerfile
```

-	Layers:
	-	`sha256:13244dbf5eaa8b8ff02f76e017e5e044960e32be2c88ee0963a2f6e2e9a2ec53`  
		Last Modified: Thu, 12 Feb 2026 21:28:53 GMT  
		Size: 597.5 KB (597466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2712fdfd7979c06682c4b9839d3dac7bd6cdd88162f62c09c6a61ce1d987e621`  
		Last Modified: Thu, 12 Feb 2026 21:28:53 GMT  
		Size: 44.5 KB (44484 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6b61a2ed1f8931c6a4e76ae7af0e970e5e1d1d4094f14cdd776b6e2b642f3a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108167793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656ce000ee1e70a2049e29dc885ea0002c3d66b0e6148868c6253766f13cd481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:04:18 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:04:21 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:21 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:04:21 GMT
ENV PG_VERSION=16.12
# Thu, 12 Feb 2026 21:04:21 GMT
ENV PG_SHA256=b253ee949303ef5df00e24002600da4fb37e5ccfafa78718c6ea6a936b4d97f1
# Thu, 12 Feb 2026 21:04:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:06:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:06:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:06:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:06:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:06:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:06:33 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:06:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:06:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:06:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:06:34 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:06:34 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:06:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebf431205a8fdc25051420d950c9b1b4054f999864fc0a23ef68b3d5791a681`  
		Last Modified: Thu, 12 Feb 2026 21:06:48 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa795c98b4b1396a3ec1bdfb51a6a5dcfc2c5383dba6eab05c1b62a972ce493a`  
		Last Modified: Thu, 12 Feb 2026 21:06:49 GMT  
		Size: 876.5 KB (876490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcb855238511b8fce3b81da54e851b7e2b4cd5044392518531b4d8999ab22b`  
		Last Modified: Thu, 12 Feb 2026 21:06:48 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df763b93bdfc1a3d91b21217f206da148e08e97aa4b15c95d89727d65e7829e8`  
		Last Modified: Thu, 12 Feb 2026 21:06:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b13f4885c01cade7b64bfebdaee5ecd27334cf68b4df170a448a774cd57a1`  
		Last Modified: Thu, 12 Feb 2026 21:06:52 GMT  
		Size: 103.1 MB (103077008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc06bc5eb69cc57a2955e966e5c0a757949019e5a6645131c035a3ea82eb650`  
		Last Modified: Thu, 12 Feb 2026 21:06:50 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b397aa398d6807c9b2b964728694ca4b49eae909198aec36b342dd242c4ebde3`  
		Last Modified: Thu, 12 Feb 2026 21:06:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f6f0eb7fd1aa32b35012404c9c64295e2ab90c1943be129cb0692058710133`  
		Last Modified: Thu, 12 Feb 2026 21:06:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdb9f321db64200489c103540f7abde0b1609fd1e198b0595aafc074fbcb023`  
		Last Modified: Thu, 12 Feb 2026 21:06:51 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85793b37ace8cfa1f788ab77d201cbf8c3ab47833d2bab431addab1ea66815ff`  
		Last Modified: Thu, 12 Feb 2026 21:06:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:cf672d1f4f589a531b7d36bf8f5f96e26411b62ff5b7bd9d928f8d75cf9c7437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (642016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1adbf272dbd0866dac6974779c12fab6a96dc95d46f2c46e9e05f87f1a10966b`

```dockerfile
```

-	Layers:
	-	`sha256:d1bf1573f50a97afbb4caf1f366e71a06a7a49fa2b8d60b6ff71ddb132107898`  
		Last Modified: Thu, 12 Feb 2026 21:06:49 GMT  
		Size: 597.5 KB (597486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc537bd2b0aa1cb6fc7b2e1a7ba24bd9c91992aacb84c7efd0abc3720299c70`  
		Last Modified: Thu, 12 Feb 2026 21:06:48 GMT  
		Size: 44.5 KB (44530 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:7580f72dc65bd16887b9c4443feab19130d52371f6b8aceaf21e848ad9e951ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116003641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f890bd6525a270960af064b97de92f4a4153b13a5a3a6a08cd9e67d05da0126`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:04:21 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:07:34 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:07:34 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:07:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:07:34 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:07:34 GMT
ENV PG_VERSION=16.12
# Thu, 12 Feb 2026 21:07:34 GMT
ENV PG_SHA256=b253ee949303ef5df00e24002600da4fb37e5ccfafa78718c6ea6a936b4d97f1
# Thu, 12 Feb 2026 21:07:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:09:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:09:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:09:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:09:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:09:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:09:55 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:09:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:09:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:09:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:09:55 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:09:55 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:09:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b162e1781be1658aaf3b531e283e1d5db965949a8c81ebe713062231f58833`  
		Last Modified: Thu, 12 Feb 2026 21:07:23 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f67441b167b495755b60a871a4380cf47f86ab348e59ff5fcb40bf4d7afcb2`  
		Last Modified: Thu, 12 Feb 2026 21:07:23 GMT  
		Size: 893.2 KB (893249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4454be357c636158771724b6a0c6c331001cfc4e2cec83fcd65f52560c8e02b`  
		Last Modified: Thu, 12 Feb 2026 21:10:10 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6385c0a318ac2435dc9f529fdce891d75e0523276c38eaa05204b479aa19e0`  
		Last Modified: Thu, 12 Feb 2026 21:10:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c9c1a965fb2692d8740ae0a1a21866dbe2111dce4550a140f841bcd1d137a2`  
		Last Modified: Thu, 12 Feb 2026 21:10:12 GMT  
		Size: 111.4 MB (111406186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255ffe293e0432d8f3b6c87f4f9ca5a46bd268c2a0665de1e26a2e5b8b49275`  
		Last Modified: Thu, 12 Feb 2026 21:10:10 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52b057912d10f89098b1b989864c8207f0af5e37d1faf6c96274c5233cd3276`  
		Last Modified: Thu, 12 Feb 2026 21:10:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572eb8c2506c74f5d5a53b1a654bbced3da604a45000fad81309883eeb769ba5`  
		Last Modified: Thu, 12 Feb 2026 21:10:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3920f3edb47f0670bf5fe7c0581bc21cce7c56b7bda19e532b5af64b7996d620`  
		Last Modified: Thu, 12 Feb 2026 21:10:11 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438d80d38559be3d3d9bdb2e3e0e9311bda6f739ec6c0add596b0302ff531401`  
		Last Modified: Thu, 12 Feb 2026 21:10:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:c8bb65d642d0e0327053abd8787c5c74d9425c017de5346b1cd2dfcb64a5fd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8085cf3fe0c6256a05ca55f5835f962513dfeadf88fa5044e041e4680ab5c9`

```dockerfile
```

-	Layers:
	-	`sha256:69e3507d8743d7a155923fa79b4ab60df34cf7b9df8afa09efbb599876c951ae`  
		Last Modified: Thu, 12 Feb 2026 21:10:10 GMT  
		Size: 598.1 KB (598055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d8e61a3d1e391b76675887b63355684cc85c21b5bb5fa5f12ea479b18556f6`  
		Last Modified: Thu, 12 Feb 2026 21:10:10 GMT  
		Size: 44.3 KB (44258 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:948cbef54a0cf25ef435e5091b91ce92b242e369a4b7358f53a5f33ed99613bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94896351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229c790585fc63fb82fc2294f2379c797ff420a840f8b40e29236a99e7eceb12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:05:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:05:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:05:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:20:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:20:13 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:20:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:20:14 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:20:14 GMT
ENV PG_VERSION=16.12
# Thu, 12 Feb 2026 21:20:14 GMT
ENV PG_SHA256=b253ee949303ef5df00e24002600da4fb37e5ccfafa78718c6ea6a936b4d97f1
# Thu, 12 Feb 2026 21:20:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:23:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:23:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:24:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:24:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:24:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:24:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:24:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:24:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:24:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:24:02 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:24:02 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:24:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3303791000843bb87e4139ec69d0072bf49042341568a87e31e34fee9bb6b8d`  
		Last Modified: Thu, 12 Feb 2026 21:10:41 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b84c177f4fdd062892cae0bf053756f85b594952f273a772df42fab740e47f3`  
		Last Modified: Thu, 12 Feb 2026 21:10:41 GMT  
		Size: 881.5 KB (881516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5c2b538dfb06dace37986f411966827fb126b105e5c672fd572c190a045e4a`  
		Last Modified: Thu, 12 Feb 2026 21:24:34 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b16eb133bf59fc60bbad5078ca0631e836e2b7c82264e85a4dfb22de76ecc67`  
		Last Modified: Thu, 12 Feb 2026 21:24:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e2f161a890575fa221edd9bde96d21a2b6f3de6edc2a55896d4b53940fb049`  
		Last Modified: Thu, 12 Feb 2026 21:24:37 GMT  
		Size: 90.2 MB (90167972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03977ef5bfa064712f1ca5a07c80097e3a350c3bc6e5da2d9bf36e30c5338d65`  
		Last Modified: Thu, 12 Feb 2026 21:24:34 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0d085349a07e80e94f83d10c5cccb47fbabab4c6e6f6b265bd4772939e8ab0`  
		Last Modified: Thu, 12 Feb 2026 21:24:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d7037ceb6e182688a34d47dc77cff5b2132f92b755d31b2c0d3c4274e2cffc`  
		Last Modified: Thu, 12 Feb 2026 21:24:35 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f8e4488c5727b81835c467e95b43969d1d7d27ef6071ec583865fc033fc95`  
		Last Modified: Thu, 12 Feb 2026 21:24:35 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbadeb2622cf2fa9b4025ec8b856d0d3632061b9e8b704111af25acc360281fc`  
		Last Modified: Thu, 12 Feb 2026 21:24:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:64b497f04722a971145033939ff08e43a89c4832e056fb0459d0eef793605f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68148453bb3adb1e6ad4b62112277355b8fd1c900d3138305f2af512ecde452`

```dockerfile
```

-	Layers:
	-	`sha256:ac7716500a41f140b3ff3abfaa381244a2514c24c1e4b05a39f56502c4bb3ffc`  
		Last Modified: Thu, 12 Feb 2026 21:24:34 GMT  
		Size: 595.8 KB (595801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71aa00b685c7dabb6aa58b0ef7719000d22cbc3ff48afa8124bae1531a7e73b`  
		Last Modified: Thu, 12 Feb 2026 21:24:34 GMT  
		Size: 44.4 KB (44358 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:c6e796f56abda78fcc765158ee8ee8443503bcc1932b35fc19b4ea9bdb5fe5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111018688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a6c843c09e36cd4c2d9b8c6b5330ea36036ab2ad82ceaa84f278b683433b3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 23:08:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 23:09:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 23:09:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Feb 2026 07:06:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 13 Feb 2026 07:06:21 GMT
ENV LANG=en_US.utf8
# Fri, 13 Feb 2026 07:06:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 13 Feb 2026 07:06:21 GMT
ENV PG_MAJOR=16
# Fri, 13 Feb 2026 07:06:21 GMT
ENV PG_VERSION=16.12
# Fri, 13 Feb 2026 07:06:21 GMT
ENV PG_SHA256=b253ee949303ef5df00e24002600da4fb37e5ccfafa78718c6ea6a936b4d97f1
# Fri, 13 Feb 2026 07:06:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 13 Feb 2026 07:58:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 13 Feb 2026 07:58:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 13 Feb 2026 07:58:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 13 Feb 2026 07:58:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Feb 2026 07:58:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 13 Feb 2026 07:58:46 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Feb 2026 07:58:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 07:58:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 13 Feb 2026 07:58:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Feb 2026 07:58:47 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 07:58:47 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 13 Feb 2026 07:58:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4bf1089e3e4046b2263b0510bf148b29c663632753f3b12c015812638b3c1d`  
		Last Modified: Fri, 13 Feb 2026 00:02:06 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a22e9ae65cd8952ab5dcd13b337378c807b8c993fc757a882f6e64d9aa5fea`  
		Last Modified: Fri, 13 Feb 2026 00:02:06 GMT  
		Size: 868.9 KB (868941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c7e473c5c09f620cec1641eab266b62934fa5e0e6973c32870f53b87c923e8`  
		Last Modified: Fri, 13 Feb 2026 08:01:35 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd7750064e6edef205cbd62fcb323dcff28fb079e21fbe3b8d66424ff940a6`  
		Last Modified: Fri, 13 Feb 2026 08:01:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6ae66b6ea53fa052235ff582d7a5a3a7f9846108317ee07326644dbdd379ec`  
		Last Modified: Fri, 13 Feb 2026 08:01:51 GMT  
		Size: 106.5 MB (106547238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83d73aeb907f08779bb535826248db599ed2852629c0cabddd49e853873730a`  
		Last Modified: Fri, 13 Feb 2026 08:01:35 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71104233247d5554e1b86f7b973f3fe532b96aa70628b576324e4a6412dbf1c3`  
		Last Modified: Fri, 13 Feb 2026 08:01:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a5aa5c877f29e8cbbf16acbca2eccb9b0a60063608a3740aeb2c086287fd91`  
		Last Modified: Fri, 13 Feb 2026 08:01:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b25f395124a21481c99937f818fe2807265d59508e23ad85def2a37b3dac10`  
		Last Modified: Fri, 13 Feb 2026 08:01:37 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b46ccee0875ae5454c776ceee4fba7343f6465eaf069afaee546994b580c61`  
		Last Modified: Fri, 13 Feb 2026 08:01:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:fd126566579fa2e4f5dbaf978140906b4784dc6b2d13eba00d91d6687c4055a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a03c09b77238d49a2bbc1826190294534e7d69a382f3e4c0814c2bad26a58aa`

```dockerfile
```

-	Layers:
	-	`sha256:4bfe7415eac90915c0ff60854b2d28559e3369c0716a4ebdfdbc52a489ffcc74`  
		Last Modified: Fri, 13 Feb 2026 08:01:35 GMT  
		Size: 597.5 KB (597459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a674af3a4b2a964443243e71fd846d9d05c5ba6c41d0596acba65e60f6ebd38f`  
		Last Modified: Fri, 13 Feb 2026 08:01:35 GMT  
		Size: 44.4 KB (44366 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:0e955f7840f4d7f21d9e405c27591131d4b7f231f298b708af979f9f5174ada7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118095159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8358c46a5b05982b1a39240f045e99b88ef2207db28b84a52b01295dcb842446`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:02:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:02:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:02:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:21:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:21:43 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:21:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:21:43 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:21:43 GMT
ENV PG_VERSION=16.12
# Thu, 12 Feb 2026 21:21:43 GMT
ENV PG_SHA256=b253ee949303ef5df00e24002600da4fb37e5ccfafa78718c6ea6a936b4d97f1
# Thu, 12 Feb 2026 21:21:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:24:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:24:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:24:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:24:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:24:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:24:42 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:24:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:24:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:24:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:24:42 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:24:42 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:24:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915db86606c3965b2bbcb157bebba9a685fced6d53839f64dcad52d883bb9a6d`  
		Last Modified: Thu, 12 Feb 2026 21:06:20 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967549b827d64fe46392dafed3c7cf52feb9091d58940d9473a94dd9f775842`  
		Last Modified: Thu, 12 Feb 2026 21:06:20 GMT  
		Size: 897.4 KB (897423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145f8a61ea8834f701d64d1d04c6e297fbb7a9cb97a8169154908ce9d07fb7a6`  
		Last Modified: Thu, 12 Feb 2026 21:25:05 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53151d2ae8e3a6eeca5607c0502b531953c5c57328c68d263a541f6504700f10`  
		Last Modified: Thu, 12 Feb 2026 21:25:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60afe2ce4c0c5e2eca26ce293a51b80d784b2beac3d30822328801d141d87e3`  
		Last Modified: Thu, 12 Feb 2026 21:25:07 GMT  
		Size: 113.5 MB (113455193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b021e9c74b51ea0d48c5b46a5dbf2605cd3ba99f7c91f5120a9bc3f7114ca22`  
		Last Modified: Thu, 12 Feb 2026 21:25:05 GMT  
		Size: 9.6 KB (9618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf775b56b313726836ebbda35d96c50e751d91a3e9b3e9ffde9f9b0df76598`  
		Last Modified: Thu, 12 Feb 2026 21:25:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242f8a9a2bfc0bf5182ac7f01cb09f8c97d036a1d12cb1952223152fb8689faa`  
		Last Modified: Thu, 12 Feb 2026 21:25:06 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf9ed300241c85da840522fa01e1adefbb0bd9398ec8ab5740fd8ee83392cd5`  
		Last Modified: Thu, 12 Feb 2026 21:25:06 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7450c2ba6c8dd68ddc319cabdff7a3712ff2fc08c6e960b85b14ca557127e429`  
		Last Modified: Thu, 12 Feb 2026 21:25:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:b8e490c4c491fe9b7814f464b9dc5c24d4bda82143646bb2b46ac6d5bda8705e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.7 KB (641735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4490de3ac2eeebdb460b4cb4259bde59f07d7c8dfdecbd04f8dbd0c1871d67dd`

```dockerfile
```

-	Layers:
	-	`sha256:4ca2f06d402ab2b83ea27164bdbd85cd01c225fc95dd99190e9f46ffe8b2f2c1`  
		Last Modified: Thu, 12 Feb 2026 21:25:05 GMT  
		Size: 597.4 KB (597429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78f895e6463e239e57ce7d090339c5eb839fb0989abe0cd48a849add01ea759`  
		Last Modified: Thu, 12 Feb 2026 21:25:05 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json
