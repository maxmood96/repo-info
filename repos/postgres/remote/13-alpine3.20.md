## `postgres:13-alpine3.20`

```console
$ docker pull postgres@sha256:f452d54d7b408263dffba5eeaea2dc8c33b08cceb73f199889a56ebf46fbf3ab
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
$ docker pull postgres@sha256:2ea71d602b67a6a1724920897be288ed56b17f98fb000e20069cd0806bc64d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96146409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39be8b34de52e698dfeccf1a6f280080e1c23293c0277c06e018d49c41832055`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f82968a792128109d31ce33bc3ab9d88acbf686e9e6887ae89c66b4601432d`  
		Last Modified: Thu, 14 Nov 2024 21:10:44 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1ef36505382ab7d41a0006cf67861bcb7ded961a6b4d5fa4c8a1318ccd9e73`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 1.1 MB (1119769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fffdb170ac3a00755294dfc80103db663f81b7d19e56fcb030f3c41fd194aa`  
		Last Modified: Thu, 14 Nov 2024 21:10:44 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31d39284f7b33fda4009709db4acd3b4055b5a6100ab64ec9346a6db74a9ce0`  
		Last Modified: Thu, 14 Nov 2024 21:07:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143ae3cf545d29f4ccaee45faa0a374924aab5ec6c9d74fe870851f720e38769`  
		Last Modified: Thu, 14 Nov 2024 21:10:47 GMT  
		Size: 91.4 MB (91386537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363b606bf97dca7aa5490de7ded3302e652f827697de39d145168d2fd8e0f3cf`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d67d994f27cefbd647b600fa60873936a3751743633a157f42e9cb07f3f905`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e194bd5bbd8d238857a0457c9bd4a4d23e7dcca33ce1bafbaa146755cfc7f4f`  
		Last Modified: Thu, 14 Nov 2024 21:10:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd02afe87118f39b51dff33a2192b9e301f1eebe03fa0ccd4847e5f65dc27c6`  
		Last Modified: Thu, 14 Nov 2024 21:10:46 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaf8eec13c7f270d3c5a8dc18bb62f33a3bbe5ad92e6f2051458b5f6f86c5e2`  
		Last Modified: Thu, 14 Nov 2024 21:10:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:e8fab57d2a11e869fb2b7c3bbdf559dd5e14794ebe67b0f48131d0d86c127dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.4 KB (633383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab16436172f5fd32d01d68c9d70f446bdbc20156fc39307f08053c7f334dfaa2`

```dockerfile
```

-	Layers:
	-	`sha256:f022f6f1a34617b5e9c32f6fdcceae45f832fde78ca31ac316f2eeb13f7eee62`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 588.1 KB (588073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78981e639a2a600fd8251cd7ed79ff2a9680e787be816ee329744979c36140ae`  
		Last Modified: Thu, 14 Nov 2024 21:10:44 GMT  
		Size: 45.3 KB (45310 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:b9ff4689be5ded9324ea5b77fed2c9da1d54aad6d03da56f0086d32de0d77b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94603496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc13160a8d50a0b4160696ed2402588a89fffabcd4c6d7a18feb8bd74ad885e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c571936168ff49222fc45202f5453daceaaad85841344e7a56766ac0c06bcc0b`  
		Last Modified: Tue, 12 Nov 2024 05:37:05 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd27d05dad1bb8227f4e72ddcbdcd2601f74b55f8b2929cff613d173bc82672`  
		Last Modified: Tue, 12 Nov 2024 05:37:05 GMT  
		Size: 1.1 MB (1086464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300102007bc93827d658bcc2e3930a994d78385553143780dadcc3f284915a`  
		Last Modified: Tue, 12 Nov 2024 05:45:35 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef5933ae7af9d77048b5e8ce8dc6807af55c837feaeaecb0fac68b44b61199d`  
		Last Modified: Tue, 12 Nov 2024 05:45:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d71fd911459278d62b27523e77ed6dd71814d390a0ca442f3a09be09d0bade`  
		Last Modified: Thu, 14 Nov 2024 21:40:14 GMT  
		Size: 90.1 MB (90134249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acd1ff1c280789ac04c742e907558300c5df3a9d314479c988844ab58e4acc2`  
		Last Modified: Thu, 14 Nov 2024 21:40:11 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bdf27f2e855adce79cc0c9fb89238f494bceed89e54bf42a519512c44e3b34`  
		Last Modified: Thu, 14 Nov 2024 21:40:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe1671970e90ee897253218ebaa0c61f49771ac50a6a85cff4c00c9c9dc745f`  
		Last Modified: Thu, 14 Nov 2024 21:40:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b731bdbe604efafdd54d6e5903b0ebd37cd09ea0eef492c9afc4d3b9e7fa0c7`  
		Last Modified: Thu, 14 Nov 2024 21:40:12 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37a97aca3a764dff80d6f215a0404398ef74f9a79c60791f0da060eb0560084`  
		Last Modified: Thu, 14 Nov 2024 21:40:12 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:7450f64617f0bfd6d509eaf8dec7cb9119d74dddc1e09b050b65ea607cf9aff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 KB (45275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e5346ded466d595c66a2b7464efb3ef82cc98e94d9ae47eeec5508e4958426`

```dockerfile
```

-	Layers:
	-	`sha256:26a422f6d4bcc1957bb56d0eff4b9085d815445b9c7361ad80062e7bb113fc73`  
		Last Modified: Thu, 14 Nov 2024 21:40:11 GMT  
		Size: 45.3 KB (45275 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:dd710c54ea888aabb6371c298133b987cabbdd48385a1274e6a6357b771da3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88937021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcd5325cad640f6912368808e05100a5474bcf2f60154c062e994de0be2da99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c21ecb73dc55fd83632acacd41b321b4eaec1e1713eebdb34dd26505cb4f6a9`  
		Last Modified: Tue, 12 Nov 2024 11:43:52 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da6f24cb862024156e04c8278ef84e0343ffffefc262f30e35f293bb46a8cd8`  
		Last Modified: Tue, 12 Nov 2024 11:43:53 GMT  
		Size: 1.1 MB (1086467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d888b7309f123d800f8af6145d64abed32e528f1a44db6bf5788f93a4b0a5a`  
		Last Modified: Tue, 12 Nov 2024 12:31:58 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d840479dd2ab0d81f2a5784be112c99207d6d7c0a4ab7332367973bacf1ed7b0`  
		Last Modified: Tue, 12 Nov 2024 12:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4dfd825dcd24ed969dfd1f44625c06b517c2c603378049b421dfd9a5ddb9a8`  
		Last Modified: Fri, 15 Nov 2024 00:10:38 GMT  
		Size: 84.7 MB (84738870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd65ba3dc9a3308750f9d6aacac4a04aa7163dfd36e4ca6870cbeab172e5c003`  
		Last Modified: Fri, 15 Nov 2024 00:10:35 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6389e0ecdb0417846c2d1918f1cdc89e62f7aff3954ffb2cadbbae783d8aea6f`  
		Last Modified: Fri, 15 Nov 2024 00:10:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cd8d8f84e581fadcf5ab78a0c4bf4ee04cccaff0c06b760a2338f55be4f20e`  
		Last Modified: Fri, 15 Nov 2024 00:10:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ec13b848fb13a623c1ca3371ea46ed70d6d0539696eb92e94a5e5e4eea5524`  
		Last Modified: Fri, 15 Nov 2024 00:10:36 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c72051dfd0ec676dcaecf93b27a0c48c5cd5b5dada8bea5f8ff59241f83538`  
		Last Modified: Fri, 15 Nov 2024 00:10:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:f4fa6f726123a9d46ac011bd788c7ab53f49d954920e743539c6d57470509222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.6 KB (633599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c45a4b7b0f5c00e90c91e477c40f8f2fdfefd46618aa751c6afc9d61e561470`

```dockerfile
```

-	Layers:
	-	`sha256:0ed41ad8b9757ca2c775f7001c3c605b5023e78f4aa6b0415c5102b8fd4f0a7a`  
		Last Modified: Fri, 15 Nov 2024 00:10:35 GMT  
		Size: 588.1 KB (588109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e2b47695826ac35ebfc8dc2724ee202506425d6878782d99824578847d96c0`  
		Last Modified: Fri, 15 Nov 2024 00:10:35 GMT  
		Size: 45.5 KB (45490 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:909beb9212883a2c4b9ae35ce695e93300b59cbc65294914c0038a388dfae292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95823553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4fd33784bbfeac6aac111686d3bb2bc1c079cf1c05f2bcd0418be541cad15b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282ccaec3303c52912b806dcadd0d5ff9ee884124945b8476220f8b85d0a3df9`  
		Last Modified: Tue, 12 Nov 2024 09:14:16 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896d994e2a0b432bc3a247e0ad5db617f8492c21a01b2e825af2145fdffbff0e`  
		Last Modified: Tue, 12 Nov 2024 09:14:16 GMT  
		Size: 1.0 MB (1047243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c58df13c5baa9c763950aba342771a95955ad465cd88771a853f00336eaa1e6`  
		Last Modified: Tue, 12 Nov 2024 09:22:37 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d7aa59458e719e08cbb7e9364d8c40a3fb8ba9a2e5307fd7434f47633ccec4`  
		Last Modified: Tue, 12 Nov 2024 09:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e235cde3c754d8585a919c8eeb6ecd79ac2f81dd06d54aa4f03c51b65cc334a6`  
		Last Modified: Thu, 14 Nov 2024 21:43:39 GMT  
		Size: 90.7 MB (90672397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbce38085d26a58d426ad15c72f8a24eff55c07d5c847595e1296ee37de3484`  
		Last Modified: Thu, 14 Nov 2024 21:43:36 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc184cae83c57127e76b8efecc87602136dbfd6f4411e3f4ee13cdb019df351e`  
		Last Modified: Thu, 14 Nov 2024 21:43:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d661e1423166641bea16a11511be2de944de3e9433fbb96fc679e63c8d30018`  
		Last Modified: Thu, 14 Nov 2024 21:43:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0edd9c643d39132a4e59146a20dc08997e566bcf7a5f15baf63cbd7f3bd0b6`  
		Last Modified: Thu, 14 Nov 2024 21:43:37 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af42c9102014adf922c66a24a9ecf54d84c1dcc7b7f5afbc878fbc8a512ecc4b`  
		Last Modified: Thu, 14 Nov 2024 21:43:37 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:9acecb8f7992397b28698b59ae817a4130887582bfe10bb4352800036a42d986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.7 KB (633663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef009bda0826b5ff02b972419236211fe47d6208ed96244e27c347125a4aa202`

```dockerfile
```

-	Layers:
	-	`sha256:0adbd21e4f642f0c4ef0444ae28ef4d8d149009961b7c1c50d3db428cd8d0812`  
		Last Modified: Thu, 14 Nov 2024 21:43:36 GMT  
		Size: 588.1 KB (588129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac709c959169d4392b84f6558fa428875d98991759ac3b4fc30787af05d1b20`  
		Last Modified: Thu, 14 Nov 2024 21:43:36 GMT  
		Size: 45.5 KB (45534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:232b90f6fe40e485d35eef16051a9192ea4b9da28f71fa944a8a3680536acac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101232109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412ab682977e7528bf7bdc02ad93b909f55175bce3dc80bf524c2cb3b669caa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e3430bc433a006c754a46e486fb74f5db4deb5fb629ca0c09969783d313929`  
		Last Modified: Thu, 14 Nov 2024 21:11:27 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402458f215eaded55d4042a2a9043c2af616bd9fb808fbf224e28d5727884a6d`  
		Last Modified: Thu, 14 Nov 2024 21:11:27 GMT  
		Size: 1.1 MB (1094865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c70afdddee7d3dec4fe2c4b57aef2505e70e3a505b7f3f6263f3b3a95481ba5`  
		Last Modified: Thu, 14 Nov 2024 21:11:27 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc292b111350836465a7c7d8f1b8dfb34ad39b5e4f18016ed284ab473e3fd89`  
		Last Modified: Thu, 14 Nov 2024 21:07:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d422dedce511191acb2372933334174272eb3ce0d65b78bdb05116ecd9a3f705`  
		Last Modified: Thu, 14 Nov 2024 21:11:31 GMT  
		Size: 96.7 MB (96651831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1827374c6d97921ab0438d4dfa20fdba5f8be8e95bfe5c332ab64791340393`  
		Last Modified: Thu, 14 Nov 2024 21:11:28 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4625eb3cc01a71247633ac581ff7a6361104b78e60d0a048bd39119003d299d5`  
		Last Modified: Thu, 14 Nov 2024 21:11:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef91fb3c0d960455578ed4689e0accbdfee6cf47853f2f985bbf486ab9f5b95`  
		Last Modified: Thu, 14 Nov 2024 21:11:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b152ffc774b80d292c02c5df3a16a9cf3e703828380d377d62b4a44dae6b9`  
		Last Modified: Thu, 14 Nov 2024 21:11:28 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64efa20c94b4043b1ac10ad21999cff191dd6e380c12404d3b8c4d27c4ec40b8`  
		Last Modified: Thu, 14 Nov 2024 21:11:28 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:62ecfdc6bf4133ed598e70ad5fe378be96037bffa85bf6b7576f0e3bc37354e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.3 KB (633310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441dd8c1935180f9d2f34ff2d15b421bdc95c9b01f26837ecc23b19e34a1b13a`

```dockerfile
```

-	Layers:
	-	`sha256:568c1fe586df1a8a400bc8fdeccb6dc0bf1b71cb2227749e15e2ee5d258ebb2a`  
		Last Modified: Thu, 14 Nov 2024 21:11:27 GMT  
		Size: 588.0 KB (588048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96420f7a118e41a290e51a46afa7580f45f732098665e2430b25244cd9054252`  
		Last Modified: Thu, 14 Nov 2024 21:11:27 GMT  
		Size: 45.3 KB (45262 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:a330af99bffffa40fd343b1d295457b38a9387b6642d9fc50150ff585b06c157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100402230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447e2e91de76ec68d14603c077e2be0fccc1ee2e4f9b1a943480343b67f753fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19a7a1f04747157cc38c8ea66a5ff6b25a502c971bf6b56995e5fefa252c706`  
		Last Modified: Tue, 12 Nov 2024 07:00:20 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1f73e281b372894f9fde9cf8b361dac11c7e4a99a9be8741f261633ef51c5c`  
		Last Modified: Tue, 12 Nov 2024 07:00:20 GMT  
		Size: 1.0 MB (1037936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eacc863115d916c7f14fdb7956d45a06cd56072bfcb39abee699970ca8aff`  
		Last Modified: Tue, 12 Nov 2024 07:09:39 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f4827aec3ef0953d51b1267885e898aa3f3f28676e7230bb67120dd71f28c2`  
		Last Modified: Tue, 12 Nov 2024 07:09:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4a4ecc824ba9508fa8bddca3d810369d0f6d0600a785efe44f15b6eebb125e`  
		Last Modified: Thu, 14 Nov 2024 21:49:28 GMT  
		Size: 95.8 MB (95775634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d676aad2f62251abacc11eb6bc984f14c324763a91579a957df83d820c0f1091`  
		Last Modified: Thu, 14 Nov 2024 21:49:24 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da03487e747bec9bbb18a435790c08706f116a9c5da694c3bc8d7d7350da0fce`  
		Last Modified: Thu, 14 Nov 2024 21:49:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecd9035912dd077b578e4c9fe8ae9ab7e8e4c1d47c05bd707045492b3680193`  
		Last Modified: Thu, 14 Nov 2024 21:49:24 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb20932babcee49f8fe5253b07d98ded1e2ed2bae708b0ad4c1cd7b28e89481`  
		Last Modified: Thu, 14 Nov 2024 21:49:25 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b76541f44c166d16f7107f93f488a981db059e81c0af23824e5b6ae1add7abe`  
		Last Modified: Thu, 14 Nov 2024 21:49:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:eccace225de64d3a942d8d1f9876ea2ece7e648a1b1d6c9d10ad9dd15d34993d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.9 KB (629859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a5c24345979aed223d85533a4a0afea5ffe85a13a778c4618a1fd277ec44c0`

```dockerfile
```

-	Layers:
	-	`sha256:36752856e9a1ee4f3563f89d9a45114a9cf360d470d4b37ace2e0f205c11628d`  
		Last Modified: Thu, 14 Nov 2024 21:49:24 GMT  
		Size: 584.5 KB (584489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70bf1a252c478d500496017ee88346db9cabe3941e0da8a206a4791bc9b3cb64`  
		Last Modified: Thu, 14 Nov 2024 21:49:24 GMT  
		Size: 45.4 KB (45370 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:939e02c2061f0aa2c56acaca02872da9bb15e49b373950f85a863a3359ccc2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95965616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fc3d71dfba29124edb468bdcc4756e545e66baed9eefa27ddf8c9c799e59ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8f6d509c68c45b1fdf0a1a4ab907f53741b31f985f51c20dc23cd8a8d6f8c6`  
		Last Modified: Tue, 12 Nov 2024 20:47:45 GMT  
		Size: 989.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38504f2cb255ba8a48a6b356aaff81feb5626bcddc945bbd59e7de7b2cbad90a`  
		Last Modified: Tue, 12 Nov 2024 20:47:45 GMT  
		Size: 1.1 MB (1087949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e6b162445bb1f4714c82ba5ee78e748e64dab99e6d2b388464c3cc9685b39d`  
		Last Modified: Tue, 12 Nov 2024 21:35:14 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71780435e839b7381f0d933d50d5f447819a9afaac78fd20e751316b070c6534`  
		Last Modified: Tue, 12 Nov 2024 21:35:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27367bba320c727b58d716c987ba5f0d24b4a403b0db66bb9cb9965702221fbd`  
		Last Modified: Fri, 15 Nov 2024 00:57:01 GMT  
		Size: 91.5 MB (91489974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d23d5a77a395d5d52132dc7b3f5c1f568e04f091bdd55275798daacbc2dddc`  
		Last Modified: Fri, 15 Nov 2024 00:56:46 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7b368627f3852406d545fa1b797e69a39190211d65e695f85f0b6ccb35ac1`  
		Last Modified: Fri, 15 Nov 2024 00:56:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d4e41c3603ccf921572b14e3968c9c7775661444bcf072535e2c520a907b36`  
		Last Modified: Fri, 15 Nov 2024 00:56:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea811edd7c0cb8fba0e1ee006b695c6cc0f392ad25c679cac0cd1a48d22650b`  
		Last Modified: Fri, 15 Nov 2024 00:56:47 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5222f13e4b5b58a9ab210e8bf9bf4d9bea1237e0cec3ab9176e40fddf10e37e8`  
		Last Modified: Fri, 15 Nov 2024 00:56:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:828aef25ff4c4da641c32a57644c683c02cc9c84b72c0564b5f3dfe836554feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.5 KB (631516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71ff726215561f3ad4d8b091602f4d6dd60bdf50398d59843bcc33b9dc936d5`

```dockerfile
```

-	Layers:
	-	`sha256:9f57e7611ba71a9b9904203d1a0392fb0e3def0a1ecb19b9112ed52e5dccf1ce`  
		Last Modified: Fri, 15 Nov 2024 00:56:46 GMT  
		Size: 586.1 KB (586149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13dd3407f545b4919b681ecacc5efed9487d0d3c6c5263c5d110d842e87f1849`  
		Last Modified: Fri, 15 Nov 2024 00:56:46 GMT  
		Size: 45.4 KB (45367 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:6e66f602102c85866b705ca9d246af45a3cf4cf5aa27d53b99388702e73befb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104696728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc2cc3b0ba583225911e52c7468c0312e600651d63d6eaf119494651adcef31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cfe172c7a286e8204df6e52175624b09a8eac0323a0ca93d64bb47b1e1d2ea`  
		Last Modified: Tue, 12 Nov 2024 07:35:14 GMT  
		Size: 989.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd3aae594b33f2c3d620dfd8f818b5fa3f522b0ebd8fa55dc50df0de8cb9062`  
		Last Modified: Tue, 12 Nov 2024 07:35:14 GMT  
		Size: 1.1 MB (1083302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fe6b14f6ff1c0c299e08d8735b27df365d66f54f2df01a42eebe9fdd7d36e8`  
		Last Modified: Tue, 12 Nov 2024 07:45:10 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475d6ddd0abdc1a91a6d685920d91fb766349ac3cc95c6ec4c29882d02db1665`  
		Last Modified: Tue, 12 Nov 2024 07:45:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b1725dfee34e9db5d00b8fc0213d6d05b4cf7ba5e8cdbb821a8e2e27d53580`  
		Last Modified: Thu, 14 Nov 2024 22:19:24 GMT  
		Size: 100.1 MB (100135610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6521d9c65938340b8f2767fbd76df86da736ad07aabb2a6e6444b0e40e10a60`  
		Last Modified: Thu, 14 Nov 2024 22:19:22 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834c9108b5e414ca10fc8d5aebdc064e2953edb8e5a02eae1d37a7a8d91aacbb`  
		Last Modified: Thu, 14 Nov 2024 22:19:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db0389180677fe7c757ba02409c1b3e43a25550e2f3e3b0b18a8456857ac6ac`  
		Last Modified: Thu, 14 Nov 2024 22:19:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31906ed39d4e6d3e1a19a41e921fd42a1bf58d2b9863f508208ac1a5756a71f`  
		Last Modified: Thu, 14 Nov 2024 22:19:23 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b072daef83f8ff8779d066bf0b7d3e6793dd7b87295a2bba3dd9c7adadf406`  
		Last Modified: Thu, 14 Nov 2024 22:19:23 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:13b865d2a6cc6ee581584a84f0b133cfffaf1b1a0711770cca034e43dc2f2f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.4 KB (631434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf91c573273ba932aacd2610150e359ddfb4cf0ad81ed2d27422e29a4f0aa207`

```dockerfile
```

-	Layers:
	-	`sha256:15c0ff898450bccfc26c849679275ab7f747f4a96bb120e320cdcb31e4a0bef4`  
		Last Modified: Thu, 14 Nov 2024 22:19:22 GMT  
		Size: 586.1 KB (586119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45eca909b0fe735b1fed08a7a35f8a97fe98caac20fd679d7a033944c5c2d4ca`  
		Last Modified: Thu, 14 Nov 2024 22:19:21 GMT  
		Size: 45.3 KB (45315 bytes)  
		MIME: application/vnd.in-toto+json
