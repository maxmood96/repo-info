## `postgres:16-alpine`

```console
$ docker pull postgres@sha256:08b3440235369fa352bbf7f9837a15c942c9ee0bea0bc8ebac6fb58158175266
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

### `postgres:16-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:d5810fcd118740b09a85e23f39646943d7bf8c74d2aca8a20a4c2025c7e87d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109973127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0001755f47e38bfd163788ccc543387b7f3da35a01b38a7c2ca1cd0277f06b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:21:46 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:21:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:21:46 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 20:21:46 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:21:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:21:46 GMT
ENV PG_MAJOR=16
# Wed, 15 Apr 2026 20:21:46 GMT
ENV PG_VERSION=16.13
# Wed, 15 Apr 2026 20:21:46 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Wed, 15 Apr 2026 20:21:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:24:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:24:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:24:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:24:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:24:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:24:03 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:24:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:24:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:24:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:24:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:24:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7cc510979317321af64404f9c44266a876a6a44d61172de31ff6a399802921`  
		Last Modified: Wed, 15 Apr 2026 20:24:19 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a112421d2742763f1a101bff2408f413c0b85f680db79236c3d17158347b03`  
		Last Modified: Wed, 15 Apr 2026 20:24:19 GMT  
		Size: 919.1 KB (919054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3109855d82fe0fb322ec7810fe7066d93b7ae6ed6ddfab74cfe67c4a181f90b`  
		Last Modified: Wed, 15 Apr 2026 20:24:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c9d01ff4048f9305df05dcd1b1e80671f790970d8c5cde3ee7253eac7de9a6`  
		Last Modified: Wed, 15 Apr 2026 20:24:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0042064f4cbb32d43df8f08c182d201ec39fbd4fff34369c5891e536076ba39`  
		Last Modified: Wed, 15 Apr 2026 20:24:23 GMT  
		Size: 105.2 MB (105172685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ef37ef383e49ddd9f95757a12a723882619bf6e8b93096d5cdf7f67d072746`  
		Last Modified: Wed, 15 Apr 2026 20:24:20 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a634b722d2531ae287dbaff6e7018a5edd6874b744ff51e2cddef77c8f11dd`  
		Last Modified: Wed, 15 Apr 2026 20:24:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c923cc956373f8ef6468c5810809c8a72d05c4a555674815d1afa3e0014c1b5`  
		Last Modified: Wed, 15 Apr 2026 20:24:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa92df9afbed653da4714e359fdd1cace68b733101e87a53222c59711aeee04`  
		Last Modified: Wed, 15 Apr 2026 20:24:21 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b519d0178fc68dc74f0dc3298993dd6abff91f110927df94262487a0affe92cb`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8d169ac41f8caaf44c8674143aaf94bb3684832ae78c831f15d6968a4ba03b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56ca64cbfee2eb7dea4b543348292ada67de8626c60783b98994cda09fc42e1`

```dockerfile
```

-	Layers:
	-	`sha256:ed859c99cf72c5646719bd933b97277eac4119e1d22c454ce482a1ec8cfbe8e5`  
		Last Modified: Wed, 15 Apr 2026 20:24:19 GMT  
		Size: 598.1 KB (598108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7be5c1a2bea8e98db7941eee55469bd1eb9331e4ad3dfee53f540daaa8e2450`  
		Last Modified: Wed, 15 Apr 2026 20:24:19 GMT  
		Size: 44.3 KB (44304 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:caa06f830755d9466cecc92c697433bc48182ef47d261275d6d960755a227dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89404089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1aed0a34d9869530cbac4e20995955c7314db52ac1d9a7255d3fd7efa96d412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:29:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:29:05 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:29:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:29:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 20:29:05 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:29:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:29:05 GMT
ENV PG_MAJOR=16
# Wed, 15 Apr 2026 20:29:05 GMT
ENV PG_VERSION=16.13
# Wed, 15 Apr 2026 20:29:05 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Wed, 15 Apr 2026 20:29:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:32:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:32:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:32:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:32:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:32:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:32:04 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:32:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:32:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:32:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:32:04 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:32:04 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:32:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dbd25d21483d5e3166fcccc4ab211ecb9eac68116ae5eeaa0ff2036a520938`  
		Last Modified: Wed, 15 Apr 2026 20:32:15 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f896879e2f4e11d3985aaa2bab82babece91d3cd72273d089bb1f64911004da`  
		Last Modified: Wed, 15 Apr 2026 20:32:15 GMT  
		Size: 887.1 KB (887115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e698f2eb498ad48079ada46cf9947ce0b17e20b8782033653a2216aee532ea91`  
		Last Modified: Wed, 15 Apr 2026 20:32:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cce0246552f535d1d2d51fbe6c0c3d3b623588ff2a20d22cfd78eca5c648db`  
		Last Modified: Wed, 15 Apr 2026 20:32:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48011f3a76cab0b09a2ac2a496cc0c7886ae1ea98bcaa99a7aae5d127e44c6fa`  
		Last Modified: Wed, 15 Apr 2026 20:32:18 GMT  
		Size: 84.9 MB (84927933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301e5d6a025b28e66f214609d0990acb3c5c866d57b020f124ad7e2ea3d9a728`  
		Last Modified: Wed, 15 Apr 2026 20:32:16 GMT  
		Size: 9.6 KB (9616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547891ef762659d96191c69cd928f78ee9fbef2fdcc39ed6eae2f73ff54cfae9`  
		Last Modified: Wed, 15 Apr 2026 20:32:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515ef35cf6ba511da6f8a0e728d27f6d8692a007d619eb0223442c1908ae81de`  
		Last Modified: Wed, 15 Apr 2026 20:32:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c298c4917263d040f26b98c44d3907df313875aba896e9107ebde4e5278237f1`  
		Last Modified: Wed, 15 Apr 2026 20:32:17 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17166f23b1000fe6fc557b09ed69b4bc5fd4b6fefae13342a1443655c6aff959`  
		Last Modified: Wed, 15 Apr 2026 20:32:17 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:de928bb041713375354276149f029f9c85e1bba081ab66cd188d31277d0634b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 KB (44269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40c66733193dd76cdd94f18b07eb5283fcf12fc1ed5b759f465633fd1b8d4a`

```dockerfile
```

-	Layers:
	-	`sha256:d92bbf004618196dd2c606948be7b33b22ef947aae81a9182f6316ac79539e57`  
		Last Modified: Wed, 15 Apr 2026 20:32:14 GMT  
		Size: 44.3 KB (44269 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8eea4975c734f1554e38e20f3af1af15bbc4d6d537943943dfb85114d80ca85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84640189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb40ea249f20c25d5a460ae267a9dc1a4cfef530fe4dbc4aa8a5b4e2ecc018e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:28:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:28:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:28:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 20:28:16 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:28:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:28:16 GMT
ENV PG_MAJOR=16
# Wed, 15 Apr 2026 20:28:16 GMT
ENV PG_VERSION=16.13
# Wed, 15 Apr 2026 20:28:16 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Wed, 15 Apr 2026 20:28:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:31:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:31:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:31:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:31:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:31:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:31:03 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:31:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:31:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:31:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:31:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:31:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:31:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44377cc98bdfa17c5cb4db5f9deda3efc02990507fa4ee7a084eebf2635d93ce`  
		Last Modified: Wed, 15 Apr 2026 20:31:14 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466576b951307bf878c61517669e0d063dd828d3707132c27a1ad1b8bbf1aa65`  
		Last Modified: Wed, 15 Apr 2026 20:31:15 GMT  
		Size: 887.1 KB (887108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4812fa0f6deef0735b62ed3504b2dcd81d3a8ee7947529e1f8217c97e177bf2`  
		Last Modified: Wed, 15 Apr 2026 20:31:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc180de10cbb943e053bc0a6032979d3d4f8148c2c46177e7f1a7d71e8382e`  
		Last Modified: Wed, 15 Apr 2026 20:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b719968276d46a3222fa157191e21132317f464f1c5e29ffd2fbb2a745b3ae40`  
		Last Modified: Wed, 15 Apr 2026 20:31:18 GMT  
		Size: 80.5 MB (80452760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792d45d4a4d179e5f14d8f2caab0526ed6af23fc4820381c133c3936330816c9`  
		Last Modified: Wed, 15 Apr 2026 20:31:16 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d170f8b491c98d39227a8c8ca45142e3c1729f351fda23a52cada1b1ebbc1a2`  
		Last Modified: Wed, 15 Apr 2026 20:31:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d205a3c8d9fb6c032cd798c19e5a199531e5b057c55521c16d91c433d0cfb9e`  
		Last Modified: Wed, 15 Apr 2026 20:31:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180dee358adf77a915b11681021083f4fefdedfe29c1bbc01f53675536a5454c`  
		Last Modified: Wed, 15 Apr 2026 20:31:17 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ed511d57e9632f9414e797a3de330679e1c33ecda46e11bc4e0eca6ca2ba35`  
		Last Modified: Wed, 15 Apr 2026 20:31:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:b31170d6e338bc729500fc7906e62d7e2500bdc780b2bc8e0cc972107b288ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (641978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c950596b0fcf527012f2836147c980993edaa8f5db205ea40ee18b2a3102d16`

```dockerfile
```

-	Layers:
	-	`sha256:51ccb10d0738853974126acea8c431b2180302c5775651c263d819e0d8d87883`  
		Last Modified: Wed, 15 Apr 2026 20:31:15 GMT  
		Size: 597.5 KB (597494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14756b226600e6435b046fd8efdf589708b9dda95df7d98efec63633aa397eb`  
		Last Modified: Wed, 15 Apr 2026 20:31:14 GMT  
		Size: 44.5 KB (44484 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d4e7bbd53503d420c248ad3039898876b7971bf5e51a6eb2f0b8c00ae8e718d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108168779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7a666480d0a8efb29f3c7876fc612147be6a37f071b74a3131248d3818ae3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:21:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:21:38 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:25:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:25:39 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:25:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:25:39 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:25:39 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:25:39 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:25:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:27:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:27:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:27:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:27:51 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:27:51 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:27:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79adb56125dd8f7feb6afc78fc07ede4c98caa32fd4e6b41f47600828da1bfc9`  
		Last Modified: Thu, 26 Feb 2026 19:24:19 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916f1ad40c1291c13adbbc451c47990f7743902c9e8899400d33a2d3ec383074`  
		Last Modified: Thu, 26 Feb 2026 19:24:19 GMT  
		Size: 876.5 KB (876493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d85c14803ffc130e481a585ec92b28b8afcfeeacf79c91ffd9bd44a007caf1e`  
		Last Modified: Thu, 26 Feb 2026 19:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58563aacf9ee3a728efadf3a3ae88bf7c6ecceb5276c67e10f84605286ec3dac`  
		Last Modified: Thu, 26 Feb 2026 19:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8f3437ce1b0dcaaa3c94cd468884c9b02d24b2b564a251c6c28772423d3b6c`  
		Last Modified: Thu, 26 Feb 2026 19:28:09 GMT  
		Size: 103.1 MB (103077994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7419a9c52e02a7b996ee048069ec4de899c6131d97d8faf405ce63ab3b50d0a4`  
		Last Modified: Thu, 26 Feb 2026 19:28:05 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b582240ca8c784720f7dd45d917ca72b857546316bf2b420ebb9dd1bf4c297`  
		Last Modified: Thu, 26 Feb 2026 19:28:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4328d592a54b7e382f9b78b8f56d44b686ab1b761c68abdcd01f6975aa14020f`  
		Last Modified: Thu, 26 Feb 2026 19:28:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bb20b6ce3efe64e83ecec646adb794188d7698295946e29fe2b6765176dd5f`  
		Last Modified: Thu, 26 Feb 2026 19:28:07 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06d9135182e824407f477c02bc039c7eb6845080abefdda56aa464b3ecbba96`  
		Last Modified: Thu, 26 Feb 2026 19:28:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:cd266d39f50002ff3287145fdee6d0d803eabd703fa1f178c11565d2ec9f5e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (642016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739c192ca50becf84f76587c585c6034c72daa25167c57661298a764b3e4c567`

```dockerfile
```

-	Layers:
	-	`sha256:7efa8dcabfcab7300245d0bebeb67cb87ff0a75c50b9486339026910f68a8d49`  
		Last Modified: Thu, 26 Feb 2026 19:28:06 GMT  
		Size: 597.5 KB (597486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e8f55ae2fa0afc6507795f52a00afbf36f02a965268870bbb05d390a489b55`  
		Last Modified: Thu, 26 Feb 2026 19:28:05 GMT  
		Size: 44.5 KB (44530 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; 386

```console
$ docker pull postgres@sha256:1f1bd3075d7d5bab1a72d24ce18dee7196c0072785de6915d1d13344faf76f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116004567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c4de9e8b8889ad2de3d760652a659557285d7058cc107ec8ccc73d14c41d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:19:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:19:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:19:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:19:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:19:45 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:19:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:19:45 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:19:45 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:19:45 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:19:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:22:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:22:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:22:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:22:04 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:22:04 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:22:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca3f36e628194c5db212861a0456aa02929490f2a8fccda365622dbb55114f7`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80279213af2ed085d7c6bea433f20529bdbe95e9a409ffd805fb8e8de6fed5f`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 893.3 KB (893259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2b21d0d4515ea3aaf3f3c42ed1cdef13f035d4101b98317f62577213f9e73e`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9273fdea5edb21fed72de1e7e7a42ff4795df5ce241e74e05da03e3c83e6a104`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b77884bea3e26045465a25f71b1d0dbadfbec4cedc1ad477a3522cd5d35cf59`  
		Last Modified: Thu, 26 Feb 2026 19:22:23 GMT  
		Size: 111.4 MB (111407107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0c9825e6779af77c27686c81d935999f458fd4f68254a1de0afee82b240d95`  
		Last Modified: Thu, 26 Feb 2026 19:22:20 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c4b2756a68bfbdf1acb2edec0c26512b2ccb11336a60f77d0ee6a2b6ad5ef`  
		Last Modified: Thu, 26 Feb 2026 19:22:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f606bea02009e32db3024790ec03e21019958476821ecb9ca929b015cc5beb`  
		Last Modified: Thu, 26 Feb 2026 19:22:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a1776431e81e5d911c89e4d1f5cb878ae1528cfb852e744b1775033ed3782c`  
		Last Modified: Thu, 26 Feb 2026 19:22:21 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a821b84ea01bfe387119b0c38aa899a229511d7ac8e3cc338d626c3b88fd4a76`  
		Last Modified: Thu, 26 Feb 2026 19:22:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:44461570478576cc29b9dad93a0fc0b24f9cae4268e8c53816e032605fff6292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d276b4d723b41a70dc557488b82773d6e02d8665d3da9c7b65739c91e1a5bfd`

```dockerfile
```

-	Layers:
	-	`sha256:1230df64794b55b7dc3f858a5e50c97f917498cc03e185030e8858084a76dbb2`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 598.1 KB (598055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9a1b2aa066a474cd3ccda625a5642cd8275708afec69995d3880694aeef4c1`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 44.3 KB (44257 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:bcb890f1768964563187faead81b8278a42ab5d6ba7dd2c3dd4da9348f9468a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94898944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c72ef70cd85de833895c5b9dfa8001e88f01fa5719eca2b0521775f8b6cf963`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:55:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:55:24 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:55:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 21:00:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_MAJOR=16
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_VERSION=16.13
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Wed, 15 Apr 2026 21:00:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 21:03:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 21:03:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 21:03:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 21:03:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 21:03:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 21:03:57 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 21:03:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:03:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 21:03:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:03:58 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 21:03:58 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 21:03:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9504179c89581170cbe497b214c2f97f01eae1cac5905e1d1fafdcf5bc01926d`  
		Last Modified: Wed, 15 Apr 2026 20:59:59 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a284924cfe2e8e2e82ff8309f349edbdfa04cfaa5de86e49b14e6cb75225a`  
		Last Modified: Wed, 15 Apr 2026 20:59:59 GMT  
		Size: 880.1 KB (880126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdbf69e74f8065c17f9aae6946c699680b19b0f5dac3b0eb9d86c6b4d150805`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40505d0bc2ac480cc189bc63f3786b58510be6cd3ab7577555a65b6258920690`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fcdc4d4295eb206a115eecf49d0bd96c0e585865a68b31bc9a9e86d73052a`  
		Last Modified: Wed, 15 Apr 2026 21:04:28 GMT  
		Size: 90.2 MB (90170679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff579539fc0e728acb4e22036cbcef630fa1cb8e6b84d4a78414b8bc672b3eb0`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0e64b0c272d793df731648ee22203c42262ef83563fe60ffb932fee89f9629`  
		Last Modified: Wed, 15 Apr 2026 21:04:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f633988446af22ccdd54fe32f778bd992ab430611d4c5c0f0541906cae465f9`  
		Last Modified: Wed, 15 Apr 2026 21:04:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f78aec0fed5e421cb35d8b95e14689330104a88191d330f5748eeecf6079f`  
		Last Modified: Wed, 15 Apr 2026 21:04:27 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb368ed9e833abfbcee4eecd1e76210daa0c41ed16cb4f1b2ee2bc8b0513b7b`  
		Last Modified: Wed, 15 Apr 2026 21:04:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:e7f2ce441c2ecbc0d0193524fd53db9b96a59269eb0be586590163b8ccf0e0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3552fd34f768e41f521bbe52273ce2dedef39e49093cf658c11c7221742fa7d1`

```dockerfile
```

-	Layers:
	-	`sha256:37b5d07602f0322b0d0d11b75efacb1ff151333bebdcfc35821e8179e7c77f77`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 595.8 KB (595829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4ef7744b37f1ad683f5d3b757f0e4e50de499d55d3a2470a28890bb626b91ed`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 44.4 KB (44359 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:437dfc1c8c319922729dd85e2c48b1b6a2763b7adeabcb7f79de3244e2c8b1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111018162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c89a60f5adcc058ddddc710ab11c90e01caa65a15059d1e306e757c44999619`
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
# Sat, 28 Feb 2026 10:27:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 28 Feb 2026 10:27:04 GMT
ENV PG_MAJOR=16
# Sat, 28 Feb 2026 10:27:04 GMT
ENV PG_VERSION=16.13
# Sat, 28 Feb 2026 10:27:04 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Sat, 28 Feb 2026 10:27:04 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 03 Mar 2026 04:22:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 03 Mar 2026 04:22:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Mar 2026 04:22:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Mar 2026 04:22:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Mar 2026 04:22:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Mar 2026 04:22:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Mar 2026 04:22:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Mar 2026 04:22:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Mar 2026 04:22:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Mar 2026 04:22:02 GMT
STOPSIGNAL SIGINT
# Tue, 03 Mar 2026 04:22:02 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Mar 2026 04:22:02 GMT
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
	-	`sha256:fd835550f29aa3e2cc22fe0488590a735c8fad8d8c9e2bf4946cd72ff8ecd187`  
		Last Modified: Sat, 28 Feb 2026 12:49:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c302a724c93a58fed484a94cf943e24c3eccb85b973ef2597212298595f69300`  
		Last Modified: Tue, 03 Mar 2026 04:25:07 GMT  
		Size: 106.5 MB (106546710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41af98d837b7cfe7aa7a4fd215352c5543066ea889e4fc8bdef897777e9f3fe`  
		Last Modified: Tue, 03 Mar 2026 04:24:51 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04f3c14cac1b028bded2d6b06e6fb85b3bca5546c6f924128cc78411fca6507`  
		Last Modified: Tue, 03 Mar 2026 04:24:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96136a01532946bad18a831dae339502e1ccc84c76dff4c65e6eaad111e0c0cb`  
		Last Modified: Tue, 03 Mar 2026 04:24:51 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8a9c5ed4889de20223b8f43efdd7332f30bdd348f8185920cdb8d5a05a208e`  
		Last Modified: Tue, 03 Mar 2026 04:24:53 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422c7c77ae325a82993d7028a1daf7dcd5914e243bff0ee1983a90fbe1885de`  
		Last Modified: Tue, 03 Mar 2026 04:24:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:49d8aeef45513ecd0d6cb8e5cc8e00340ca545d2d3493ec05f75d3ccf1959f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36e5bbe1cfd052c7d2e1b0eba69e5a7b0417e9c64f5d9d74443c37ab844f3f9`

```dockerfile
```

-	Layers:
	-	`sha256:2a74a7bc838d683e8febdc74511d7cbbd2c3254dda5dca0d0ec1955ea6ef1c90`  
		Last Modified: Tue, 03 Mar 2026 04:24:52 GMT  
		Size: 597.5 KB (597459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51de3d6de14cd64e0b0fdf06364a4952dbafffdf9c8fa76687646e84d3af2278`  
		Last Modified: Tue, 03 Mar 2026 04:24:51 GMT  
		Size: 44.4 KB (44366 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:f49c8fa7cf587f02f40ee99b2c9acaca76453dfce86dbd733ea7a2213fff358e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118095048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9552ba436e9377b26d1d25b694429f20d804cf84baa6c7445c11b67b743dabcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:34:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:40:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:40:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:40:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:40:26 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:40:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:40:27 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:40:27 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:40:27 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:40:27 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:44:29 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:44:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:44:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:44:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:44:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:44:33 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:44:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:44:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:44:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:44:36 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:44:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:44:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32e9b7742fe584659e12027c33c400a4177f291e191753d48596ef84ac6ec61`  
		Last Modified: Wed, 18 Feb 2026 23:39:16 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb3bc9055ac62b0b138d240b97e4cfb0d0656a56953b9cf1c00d287a697bad2`  
		Last Modified: Thu, 26 Feb 2026 19:45:19 GMT  
		Size: 897.4 KB (897426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17785b0e67ca21a84f365ecae8b55dc3fa0bb71f95e5d4ca3476229ee869e67c`  
		Last Modified: Thu, 26 Feb 2026 19:45:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6f63b4d999cd25657ca03f69a8292f4c5c9d5233a327cd1df29148c43820a9`  
		Last Modified: Thu, 26 Feb 2026 19:45:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03458acedf88f38f5379b9ad09c9b6b6524f5b966ad93ffa9d8e4e8defde806e`  
		Last Modified: Thu, 26 Feb 2026 19:45:24 GMT  
		Size: 113.5 MB (113455083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70884288a5259b1dbda59bd9f404015a8c355c1517680a6c4ef80957dc96adf`  
		Last Modified: Thu, 26 Feb 2026 19:45:21 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7893c3ff90e437da82ffaf4e96df3eacdfc88f78756495a888a45fb31e2970`  
		Last Modified: Thu, 26 Feb 2026 19:45:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6b53a5d1eae986c64283d3371329760662ea2263efb8a462fd0e6859c328b4`  
		Last Modified: Thu, 26 Feb 2026 19:45:21 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43ccbcfe32a3c78004d2469d16382c34c43816a7a5198b8192b23d85bb1a3d7`  
		Last Modified: Thu, 26 Feb 2026 19:45:22 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ce9f1f99c4ec9d30e8408f46006c61ff9a7d6b16c6daac35a5805903dfccf3`  
		Last Modified: Thu, 26 Feb 2026 19:45:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:187ff538ff38c958900f080fae6e75df8196e9a81f285d40c9f060534366e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.7 KB (641734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9823c5c75857cff14a914de0ec905f26a6c5e708270440fc81b37d866f34bba`

```dockerfile
```

-	Layers:
	-	`sha256:be46a9387b237d188043d207a648edd44f1710856ac276a74dff6913e253597d`  
		Last Modified: Thu, 26 Feb 2026 19:45:19 GMT  
		Size: 597.4 KB (597429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b2cb2bd8d85be0343f2147231bde9a481651ab6ae44938095046d9a795c67a`  
		Last Modified: Thu, 26 Feb 2026 19:45:19 GMT  
		Size: 44.3 KB (44305 bytes)  
		MIME: application/vnd.in-toto+json
