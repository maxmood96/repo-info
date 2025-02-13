## `postgres:13-alpine`

```console
$ docker pull postgres@sha256:2c692d47ba7074205129f25e663ee5840816bc24e9af878995ad33336d83332a
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

### `postgres:13-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:38bbdb37d54417be2ea3e18d3912000ee638d49b408c572aaa6e1ff28312a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106783245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c74beeec387f9d07e09390184a2098db9ab1c70942de983dca90fc8716733ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5209de74574ecabe7506a7d96455c5670617532a79724b798b855fe5fb1278a`  
		Last Modified: Wed, 05 Feb 2025 00:08:00 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a668b53d419566a070e4505fe7befdd398a77a9826e10f9909e52eb5652058`  
		Last Modified: Wed, 05 Feb 2025 00:08:00 GMT  
		Size: 1.1 MB (1120332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c470b858c7114723d259e54528a541292608eca888d4eaae31fa3f4faa5d1e`  
		Last Modified: Wed, 05 Feb 2025 00:07:59 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0670bc36d5ef6c09cd19f843608a2c7f65fb873d320f921b621ea3ceb3caa1e`  
		Last Modified: Wed, 05 Feb 2025 00:08:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8609768d9a92c11117801614e6f0549ce66044d62e8cbea83e22a3574a0cd795`  
		Last Modified: Wed, 05 Feb 2025 00:08:04 GMT  
		Size: 102.0 MB (102005016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9798c420fdb45981971c4c504e37debd85516a66ee1ff018213f2e06e1600de`  
		Last Modified: Wed, 05 Feb 2025 00:08:01 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04430f1b328eabe310bf47ee392b06108db96eb208eb77aaa967db937d25657c`  
		Last Modified: Wed, 05 Feb 2025 00:08:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c23be6bc7156adf561522f5616391cb9e25e24bccf10d119447497871b1556`  
		Last Modified: Wed, 05 Feb 2025 00:08:02 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2338436a505110558f2fc0300aaf3469cacd61724c37a569a7cdacbbe6895ee7`  
		Last Modified: Wed, 05 Feb 2025 00:08:01 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b38cbc4d410605cbe852e0070d15ba6409d4e590fa5154c4649c80f3782ae6`  
		Last Modified: Wed, 05 Feb 2025 00:08:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:2b74746bcd35656f91dd7c9418bb3158f08b0f9f9a73af166d7fcba5bdc0217e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.9 KB (636933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede4fcf3da854cb672fe2235a07d82e2a47c6f9c9d3214ab0db3f9f3120f75b1`

```dockerfile
```

-	Layers:
	-	`sha256:42adea2ac0d59368df976c8c851ef389d312f8304fa0b900d2c79f777c8d2c28`  
		Last Modified: Wed, 05 Feb 2025 02:01:27 GMT  
		Size: 592.1 KB (592105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06b6a71f8d54e61b98c4971556e3228afbbb172102225c81adc3db6feb37033`  
		Last Modified: Wed, 05 Feb 2025 12:07:50 GMT  
		Size: 44.8 KB (44828 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:e6f86e25a195f7f3f0bf1dd980b513cd760a1b51b505e09bc68abe5656cb3949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86459504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e139687e45f00c8902bfd1e91c6b94c7944160aab12d58d134be6a5980ab67ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a22c557d31caf1b269aa223bacac912676332abc4327c4fc6d8db2708f4b85`  
		Last Modified: Tue, 14 Jan 2025 23:02:12 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958deb370f8f34e49786548df7ccce1178adf3085f56572db7da1fa3bdcffb3c`  
		Last Modified: Tue, 14 Jan 2025 21:44:12 GMT  
		Size: 1.1 MB (1086612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5baf854ce9dcfb4a9c9035f65fda2ede7e4341458462f603a1a2e5470a9497f`  
		Last Modified: Tue, 14 Jan 2025 22:31:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e858c75599abdf33031fd4cf16af58c3e650f1e9a786e6a125088aa5ab788f8`  
		Last Modified: Tue, 14 Jan 2025 21:44:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2c42ecf2552471f5eddd1a5ff62f1727acd51af37206e1cde9af70b1ef932b`  
		Last Modified: Wed, 15 Jan 2025 16:14:41 GMT  
		Size: 82.0 MB (81992824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96502327c4a108554a68ed3a395676b34cad0a9efaf5c0ccae87c3289f5c96db`  
		Last Modified: Wed, 15 Jan 2025 16:14:18 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb56f3307b88c543761a57f0c4897f814819f6a8a5120062f22a757caab67b0a`  
		Last Modified: Wed, 15 Jan 2025 16:14:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654b3f93c358b40d0beee50c5a1d5bc1edde9f2d9912e28abb7928c685096396`  
		Last Modified: Wed, 15 Jan 2025 16:14:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18e2977b0707ff7b726551420cde760d92c5d5dd62966c83dad88e8d5f19c1d`  
		Last Modified: Wed, 05 Feb 2025 20:07:23 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb84cf4d85a2d92bbba3f6db82145550920dbc672beee17d42d7e598a55aa5c1`  
		Last Modified: Wed, 05 Feb 2025 01:01:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:1dcb548b6cd8fb4eb387fb688ead6ebcdcb9a9d148678cd90e80e7141ea85f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 KB (44787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b907f49c1dd40a0e3c766fc6224d2968e945fde7f42c20bed4c3937964f7ebd`

```dockerfile
```

-	Layers:
	-	`sha256:6fc5fe9c136d6ecad54d7a9373fcbe65d12aaf5a6b90ca6d178857d1df9d62f2`  
		Last Modified: Wed, 05 Feb 2025 01:01:10 GMT  
		Size: 44.8 KB (44787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:9c0ff66b06408b1590f34be853ee213decd86e1370f1778402e2ea789122be6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81757124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f8bbb1684c8b560b0abc6203e28b68ef9ea3ebb8cd3d24b68a4d4fe0a5f683`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb05567add68abef3b484f37aa5bf5731fe13ff929e5e9771adf36091ac003cb`  
		Last Modified: Wed, 05 Feb 2025 00:14:05 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54474578abde0ef4c2fd9521acf2401673783619c7536bdb4da90ff27ef2453`  
		Last Modified: Wed, 05 Feb 2025 00:14:05 GMT  
		Size: 1.1 MB (1086604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3720a05cdbcb135123c80645f89293a7d4a202fa142272d381f2e1289dfb1e`  
		Last Modified: Wed, 05 Feb 2025 03:03:02 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01033150115b824d062d4b717c707bca61d5c831145259972b7c78035a04e960`  
		Last Modified: Wed, 05 Feb 2025 01:29:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006b1959ef006806b8382c5a592e31189a8958d37d85cb1b05b50479d7a6fe5d`  
		Last Modified: Wed, 05 Feb 2025 03:51:45 GMT  
		Size: 77.6 MB (77557210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f206df76cc99ab5cb42623642ba7539225afc27a9e345d13d0fb5446c05d766`  
		Last Modified: Wed, 05 Feb 2025 04:00:59 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2827af080bcf5f2a826176dc6229054c7ff8f49127c3f1fa002e5096fc98d2c1`  
		Last Modified: Wed, 05 Feb 2025 03:51:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06aa385d5066f5eb0e83d1e1c97c1569a09939577ad6c35be6cb461c064a0f3`  
		Last Modified: Wed, 05 Feb 2025 20:00:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef05767c25a436f893bb6a89d3999ee843917d9b85ae317fe2ff29c8063413a`  
		Last Modified: Wed, 05 Feb 2025 05:16:50 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87457d70a1725f7ed8d00282604b87ee16db7063ba6c4142c3581206736113b2`  
		Last Modified: Wed, 05 Feb 2025 03:51:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:6cc28f61d8a05aef1e2aca6a4e148526788a7bb4383598139394dc4e5d2881fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.1 KB (637142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea33b0ed92017174a9826b1d2c0523a0deba507937b5c582f5312703c175c97`

```dockerfile
```

-	Layers:
	-	`sha256:d6ab13d6511569c558f03cb336eb6537e1de4af42a73f3d29f84b6f64075199a`  
		Last Modified: Wed, 05 Feb 2025 20:07:24 GMT  
		Size: 592.1 KB (592141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45aafd5c019811a276012111bfb8929c9c86bfda51a0aac9855b3061cd8b8595`  
		Last Modified: Wed, 05 Feb 2025 20:00:27 GMT  
		Size: 45.0 KB (45001 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6130358eac75267d1c1a60535f57e0e4e4d2d29e80779e134f77e41814951c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102691979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255510b25ed5aaa05b37444d547147fd8a6dc7321e61fa2b33c065125f85c362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992b9109aeaae74f5c47c852d266a21087868b3d59823c415cf47660a048712a`  
		Last Modified: Wed, 05 Feb 2025 03:01:00 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9293d9b0151377c754cdc3169946ddbaf0bddd7c586d8fdb349913743b3bb2`  
		Last Modified: Wed, 05 Feb 2025 03:08:28 GMT  
		Size: 1.1 MB (1050045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d0e6790c6b5379712518ef114f466bda510f0c88ca89c5896e1bf3f4653e37`  
		Last Modified: Wed, 05 Feb 2025 03:01:00 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c31f786a65552f0cea52bf6c67821e98c1e19741cc1ede745dcc5607bab2c0`  
		Last Modified: Wed, 05 Feb 2025 02:40:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57de168ffaa186451d73c5faa49c3f326ec2c66a7d7de2890ca741dc49acb1c`  
		Last Modified: Wed, 05 Feb 2025 03:09:16 GMT  
		Size: 97.6 MB (97633388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd888d7142948bb60d904020e36eccce66e38bc526ac46d816733ffb7ab3abe5`  
		Last Modified: Wed, 05 Feb 2025 03:22:37 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3661ce6131f5cf2c651204bba86967de34d467186cdd0bb783433e6f0c1daaee`  
		Last Modified: Wed, 05 Feb 2025 03:08:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871c2519ded0a7b57c6bcc067c584423ac27e0e498fc6a3e16e4f463f540a8e`  
		Last Modified: Wed, 05 Feb 2025 03:09:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9253599b4607d72e85126dc17b17df5e55d18c53bbaa797d1d7f8554ce5575`  
		Last Modified: Wed, 05 Feb 2025 03:13:26 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9a64d3622e363e8dd371d65ba179af4ce119b787f85aa25c6d811d47422637`  
		Last Modified: Wed, 05 Feb 2025 03:19:00 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:c9fcf4524f1a4d6fa9c4f3b4278fbfbdc2e02af29793bca3cdee67141f43e932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.2 KB (637205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa0ede2e92fe2e7f67a2397bc85c6e43e052c0efac249e03de9eeefcf37363d`

```dockerfile
```

-	Layers:
	-	`sha256:d9adb1e84aacd5950db16ae8f68844ea5181e51c6ee686d3b0e0be2596f5c553`  
		Last Modified: Wed, 05 Feb 2025 12:35:29 GMT  
		Size: 592.2 KB (592161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a66fb32e37a1f3877b12e549239bad9fded7af32b15402445d3acad0ad44ced`  
		Last Modified: Wed, 05 Feb 2025 12:35:29 GMT  
		Size: 45.0 KB (45044 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; 386

```console
$ docker pull postgres@sha256:415939f4205fa3ba4c79c74a3a62f014b593593f64a8d9ffa35e7e69049fe69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112864063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2102d659c347b177e0e1b1fd28eca4e498f81d3362d0324936f7d287b96e6b94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f9da3312e50098c6a1279495882202b7310de4e09a0dc5abc4ca69da0238b4`  
		Last Modified: Wed, 05 Feb 2025 20:00:41 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679380dec1b459d01eebb495b8bd12f1021a83407b9b6f72b7397018ffa47cd`  
		Last Modified: Wed, 05 Feb 2025 12:35:30 GMT  
		Size: 1.1 MB (1095275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a174b9275bd712b66c936dfa9436b463dd94cbd52368caf24cb1e53007d1bf13`  
		Last Modified: Wed, 05 Feb 2025 02:01:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e69ed0a0d9d7e22d218b6029a18d70017632a448ae7e4f5fc58831d5622f3a5`  
		Last Modified: Wed, 05 Feb 2025 01:01:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4526a086caca07529d8dacd427fa4b6d53632ffdbf2307f2e097ec651527fd0`  
		Last Modified: Wed, 05 Feb 2025 12:35:33 GMT  
		Size: 108.3 MB (108289488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962d54aebdb70e255124382b2896e03b9bebbafeb489350bf2283eb9b4b818f7`  
		Last Modified: Wed, 05 Feb 2025 02:01:50 GMT  
		Size: 9.0 KB (9011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608480d6a7b307a37b27282822d4de60607d311153a95e946fed394b43f94e5d`  
		Last Modified: Wed, 05 Feb 2025 00:18:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787d70a7d28b00fff8ccd0e7e1d6b24fbbb91d16643e994e28f1439a6f134895`  
		Last Modified: Wed, 05 Feb 2025 02:01:52 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058006a2255a51cd539347dd03cd3c3aa8f93eef8d786fdd5a814e24a9eb70b8`  
		Last Modified: Wed, 05 Feb 2025 01:01:54 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6d3f3feb9946373a7f32dbd0a60c104fbc4a897c80dbb7a64cda2d86e134e4`  
		Last Modified: Wed, 05 Feb 2025 13:37:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0064204df7843df618d45d8f7203e88116db503662250ca02b1c776b3a8e371e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.9 KB (636858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e7f06a072bf3d3fa14fef3d69c64d1f18e711c31fcd539ff821997919fc707`

```dockerfile
```

-	Layers:
	-	`sha256:ac71a0cae990b3d2124e24d88212a333ab8de25aa09ae9acdc4aadc0ea492638`  
		Last Modified: Wed, 05 Feb 2025 02:01:58 GMT  
		Size: 592.1 KB (592080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70571429ba0911b2793e06633259a227e3bc8e5f8853e6d3ff20541cc4513b39`  
		Last Modified: Wed, 05 Feb 2025 02:01:59 GMT  
		Size: 44.8 KB (44778 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:266a1d32075bd95af715ac43048ba2b8f16ed62daffffbec4d60642587d98fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90323993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f174324626950268506784ef27d6a7e1a2765539dd4ed34e038643ea907f33a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4de803835da75ae4f48f846b265f10fed54358c260b7dbb0f1bf1e98ed04943`  
		Last Modified: Wed, 05 Feb 2025 01:01:59 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e88bb7ce399fcbab123a0a9f8aa3b30e35ba5b27750c59aff36e4a681dc5c1`  
		Last Modified: Wed, 05 Feb 2025 01:02:00 GMT  
		Size: 1.0 MB (1040364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b752c49809654d9c49698e50bbd5df99153af5a326ca0bbc54a4203ce43ebb31`  
		Last Modified: Wed, 05 Feb 2025 02:02:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e2c352c662ba8f20316b983b960e9444231e8b4ef47c78123841ba5bfbad37`  
		Last Modified: Wed, 05 Feb 2025 01:07:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd22dc067cf60984640141dc509a911b5330fa901e2f1016b5fda345965e069`  
		Last Modified: Wed, 05 Feb 2025 02:02:11 GMT  
		Size: 85.7 MB (85693834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728b589687574e5c3bae0cb82223c7cb8553b9925868e1b3b712f839f56a43af`  
		Last Modified: Wed, 05 Feb 2025 01:02:30 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac85296f4dff4285829284ab9c0fc847e44cabdd152903a7915054ecd126a9e`  
		Last Modified: Wed, 05 Feb 2025 02:02:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b664df51b2765803f0a77c31906ef93e6a8ba537b8e07ee1758d2abe6932e29`  
		Last Modified: Wed, 05 Feb 2025 01:02:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa29e0e3f7d32a686789e456be2c51aa331a560298a417522d3d881633c370d`  
		Last Modified: Wed, 05 Feb 2025 02:02:17 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a6f3a3d8d29d77e154d1b5b3142f7f8cde11d10bfb97ae0b39e50dc886613a`  
		Last Modified: Wed, 05 Feb 2025 20:07:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:19c57e21feb45bfef477d2d5589765ef13fbbe81a2668cabb0ad84f47966e04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.4 KB (633407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3fe369aae3a94eb51b92ad560b6a095d12339a3426c68db51f2b15c7407322`

```dockerfile
```

-	Layers:
	-	`sha256:8985df53c1702ed58e6ca1d3a67e9e98004ea309ad595d6410c2ed4b652a0b9f`  
		Last Modified: Wed, 05 Feb 2025 18:03:28 GMT  
		Size: 588.5 KB (588526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188c8110cee6e758371f4727041966a06e969f0e5d73ff369d89aa4ffd901df8`  
		Last Modified: Wed, 05 Feb 2025 02:02:21 GMT  
		Size: 44.9 KB (44881 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:74dd01cdf3f98f02017192a77b6658b38eee5959de7c456e4bb5e0fa825c2ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106223553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef79cddb68f90f47318e9627d31d9ca7d0b16f11c06d17710ab2d89e3084a762`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa70428e43128e29ea85c02b9ad8867c57f3c57d80ee4c8367e06d1044bc81a`  
		Last Modified: Wed, 15 Jan 2025 02:15:04 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b30861d9a22965c9c8ab0e3148f19b31c48adac4184db37373b16aeb1836e26`  
		Last Modified: Wed, 15 Jan 2025 02:15:04 GMT  
		Size: 1.1 MB (1089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ee96017ef0ba8a5e5adc67c305a2bb47d5c776594a60202ef59765710d8a19`  
		Last Modified: Tue, 14 Jan 2025 23:03:24 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ecc705b39b2ca8d6e5ca7d9227c696d64688b012cc93494869f3a75ac26b68`  
		Last Modified: Tue, 14 Jan 2025 23:03:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474d123440db9342a681ae560c1936defc9ddf9249fb021ba0dc2733a04e226e`  
		Last Modified: Wed, 05 Feb 2025 13:37:34 GMT  
		Size: 101.8 MB (101767300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2b68f70b8aa8020b9cbce061bb683d8d15b11f4f31fb4ff61fadc48c16d0d2`  
		Last Modified: Wed, 05 Feb 2025 13:37:08 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820fdc1758cfdc9be262630f26904c5732370e4b35b9b341c8c0beed2205486d`  
		Last Modified: Wed, 05 Feb 2025 20:01:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f940d9462888a2d57f7e30a5e347bfadab5e320359b16af64fe129df8d3b3`  
		Last Modified: Wed, 05 Feb 2025 20:01:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a72f5a071f41c3fdf8c60b10f418bd35d1e055037e1edb208d369e9b3888c6b`  
		Last Modified: Wed, 05 Feb 2025 20:07:28 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccb15fd22aece71463dfeec76692bfb937be567c71afed8bd51f4db61ee94fe`  
		Last Modified: Wed, 05 Feb 2025 20:01:09 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:67019a5bca92d4acfa2d6e321d0befbac91fd33cb1ce028b82c57ec085d46b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.1 KB (635072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d294f6b85705bb920861b1392df04fa34c9eb393acb9d6527e96b552b250041c`

```dockerfile
```

-	Layers:
	-	`sha256:ef2a335ce4ebf96d8f8e9603fd60e481618ef312981232a72fdb7de0fb8b32de`  
		Last Modified: Wed, 05 Feb 2025 20:07:28 GMT  
		Size: 590.2 KB (590184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:523f2659367f485cfcfbfb5f1f87ecfaf4d70022b9094765f5a0d2dbf8b4e528`  
		Last Modified: Wed, 05 Feb 2025 20:01:10 GMT  
		Size: 44.9 KB (44888 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:9bb64d71e202d58a0679cbd83f211804b95d8a6096db36c9b426bb1696da460b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115207024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a14dd2ae2e4bc259f89bfc4dcdc7b96f23859955b89fa59457cf4d04970cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=ceea92abee2a8c19408d278b68de6a78b6bd3dbb4fa2d653fa7ca745d666aab1
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c56695c85edb37ce406b4667f090721587f7d2dc9452e0ec86dae6902585d0`  
		Last Modified: Wed, 05 Feb 2025 01:05:37 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4ac9ad3604d910dc8b794cb00cccd50d1a63d5ec97b3256b4a8d034e01945e`  
		Last Modified: Wed, 05 Feb 2025 01:30:57 GMT  
		Size: 1.1 MB (1084567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae6505784918dbcf00ac2a80ef08d1b47355616628edee04c6679dbab5f4083`  
		Last Modified: Wed, 05 Feb 2025 01:02:40 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b1780e171a060bacf653b2becb7b116054fcde6d16bdd688463bb751452d8`  
		Last Modified: Wed, 05 Feb 2025 02:02:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceb07b9a142d03307eaabb2ba1924d203b020e3a831ace2df4048046fe4214e`  
		Last Modified: Wed, 05 Feb 2025 08:29:07 GMT  
		Size: 110.6 MB (110639401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5382457503f28d81c279164463409fe6ac5078f29ee9944b044048af15c969`  
		Last Modified: Wed, 05 Feb 2025 02:02:34 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71170588ef892c44ca3cd87ea90c5d50bf810f7cbb98759dd717cc9c172946ea`  
		Last Modified: Wed, 05 Feb 2025 20:01:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf279c002a6019e5b0a3841942d34c992f2d40752f8430a701394b8b9c2d1e`  
		Last Modified: Wed, 05 Feb 2025 20:01:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f45e261510f755a74cc2f2453773938e76e51899fe53025cb67ab2d4cc3db4`  
		Last Modified: Wed, 05 Feb 2025 02:02:37 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550b3dbde863ef3c871d4be23676d919a9dd734e74ecb354676f020d834c4f03`  
		Last Modified: Wed, 05 Feb 2025 13:36:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:b2a7da84b381dd40669228edab1373b5e505d54daef007a84564c090045561f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.0 KB (634982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53edd4e59f3af1f6835508eabd6ba0b773b755b82ba9a28cea0af0bee35ec4e`

```dockerfile
```

-	Layers:
	-	`sha256:d3c8b09efdb14b736ad696d15ebab2dd354a4302195cd60fbd04e4849e6f1767`  
		Last Modified: Wed, 05 Feb 2025 02:02:42 GMT  
		Size: 590.2 KB (590154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfad0a9a35c555657063f2dd30a0a06fa916ac6d18f93d3136ab8cd4fd2aede2`  
		Last Modified: Wed, 05 Feb 2025 20:01:21 GMT  
		Size: 44.8 KB (44828 bytes)  
		MIME: application/vnd.in-toto+json
