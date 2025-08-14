## `postgres:18beta3-alpine`

```console
$ docker pull postgres@sha256:f39005980b5b149f013141df138adc66f5c7ad25365f95d65eabda01cb77233e
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

### `postgres:18beta3-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:252a5815c3206a0246f069b7baa8361ed41d20c57e08420be62d15b1e20cfd51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111650185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c4a78b167c91543d41a4edf5ea02a8ecd25972434248c72b7f07669f124977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18beta3
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_SHA256=21d86e55eea11300c3a2212647dc3d48bd844b83017cf6ce5684639ad8f95278
# Thu, 14 Aug 2025 17:31:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b10d8ba47c2b4eb144fc9ab13f44379cce02c8d4f8c77fcbfc5d591d97489d`  
		Last Modified: Thu, 14 Aug 2025 18:24:45 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4139433d0410f21d40eb98b9c9eb9bc501147e9e18cadb33cb8f3e69d6d137f0`  
		Last Modified: Thu, 14 Aug 2025 18:24:46 GMT  
		Size: 1.1 MB (1115585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a032dd7e4d9c922845a919e1ac0f2a7869b23744f510e21e7a2b742ad2d1a`  
		Last Modified: Thu, 14 Aug 2025 18:24:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0a2d8830c20df813cf7bd15ed147c62212e5b525d152290c200954d99f7ed1`  
		Last Modified: Thu, 14 Aug 2025 20:35:18 GMT  
		Size: 106.7 MB (106708631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f15e5dbadf3c759734bf1229eedee293ec9cc7410eb0eadf133ffd2cfadbfdd`  
		Last Modified: Thu, 14 Aug 2025 18:24:47 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81c6395af5f3d1aba0d6ee2f39c7111e5d744300ec834c37ced49fef81641f6`  
		Last Modified: Thu, 14 Aug 2025 18:24:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feca9c6bff0da1b85649b6c1d0abf43c18a6eb4a22171c13f4d06365a2af5a97`  
		Last Modified: Thu, 14 Aug 2025 18:24:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191fc1f5039b0d651df0bebc7b77ee53a18c8ec691311e78f53448c6b58185da`  
		Last Modified: Thu, 14 Aug 2025 18:24:47 GMT  
		Size: 5.9 KB (5924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0e632b978eb39a43f5e72b8c2f2d147dc2557ebcd94f57cc1f1d9a1845b763`  
		Last Modified: Thu, 14 Aug 2025 18:24:47 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:fe64027c07c096005caaa4072b839f2d39c0b5a0b2b143e2862af5db1aeca809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.7 KB (637706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7233ee498d4571f54b192f2bb4aa0b6435d52550748ee8972a3b8afe84ae5dd`

```dockerfile
```

-	Layers:
	-	`sha256:30388a5163d5822f12c651529892e67458db0220d23155503307dbaf935d411f`  
		Last Modified: Thu, 14 Aug 2025 20:18:54 GMT  
		Size: 596.3 KB (596329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658e2d6dde2efe68bb11c577129452f424a0195d89f4269f4b5dfbd9a8042406`  
		Last Modified: Thu, 14 Aug 2025 20:18:55 GMT  
		Size: 41.4 KB (41377 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:a951aab9934b9c47fe90e4d2c73e526094bc30afbffceee49373c2bc782954f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91235221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100d2b1aadaf46174e37072d20731ac56db012a7e16ddc9604779316216d7275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18beta3
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_SHA256=21d86e55eea11300c3a2212647dc3d48bd844b83017cf6ce5684639ad8f95278
# Thu, 14 Aug 2025 17:31:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079a1c87b1e4afd06564bb4788685a8121d0bc8ee1c65f7d29bae031097a898c`  
		Last Modified: Tue, 15 Jul 2025 21:59:03 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e018b614d5cbf1a0d8a1b23f428d5cbbbe192798ac0751d81172993ca1dbc93`  
		Last Modified: Tue, 15 Jul 2025 21:59:05 GMT  
		Size: 1.1 MB (1083508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aebdb48dce72469d3bc8e6f100e27f0b1c674d0a7c8519656f5c74d79da67ac`  
		Last Modified: Tue, 15 Jul 2025 21:59:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc5a0a6e9dde8689b7477537c5fb35dbbbc20eb90540be17dde5859d7066902`  
		Last Modified: Thu, 14 Aug 2025 18:22:44 GMT  
		Size: 86.6 MB (86624518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a8d60435c89d2a3aabbc968b28ff05ea7d7a902ea0be00e0d75530ff4222a2`  
		Last Modified: Thu, 14 Aug 2025 18:22:32 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d464453cb9b58913dc3234ded40b87e529f2c169350407bbf7f4238c5b42080`  
		Last Modified: Thu, 14 Aug 2025 18:22:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6772d74d03adba2a00006606f5e3401865c9482ce887c51984c3d0eb78eaa6`  
		Last Modified: Thu, 14 Aug 2025 18:22:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32044a53f6f0ed4e49d737326b7618604361ab241d34b42dac45c1ecd99b4d2`  
		Last Modified: Thu, 14 Aug 2025 18:22:32 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8376e7e2e6f728e58f8a23b903e53f1cd7113b6aff42f577a618328da876d8b4`  
		Last Modified: Thu, 14 Aug 2025 18:22:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:e8c24e3441bd84a0ea5765449e66511ecfbbaa1d6f6f15d89580b15cc88b366f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d179a1ca0ce94a518398b39f0394b07168a057a82a3e959ea706be4e76d907f0`

```dockerfile
```

-	Layers:
	-	`sha256:8a1d1001899b61d3ad9cd0ba476230c47c46ba4241df53f7c8b18b498174c4af`  
		Last Modified: Thu, 14 Aug 2025 20:19:00 GMT  
		Size: 41.3 KB (41307 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:21f5e4c697bf16cb5648abda6d9855fd56d89163cb11c3bbeaff91992d8636bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86432065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52d2feab4be70c04f47d7cbdb612529686fd733281730b40139dbb4bf9f0566`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18beta3
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_SHA256=21d86e55eea11300c3a2212647dc3d48bd844b83017cf6ce5684639ad8f95278
# Thu, 14 Aug 2025 17:31:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d311585bee083aa9525f093872b6272f30fd05678140622cf8b253423af3dd`  
		Last Modified: Thu, 14 Aug 2025 18:50:36 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36a7751694a53e9a57d5356c38e15bbc8420fe128dc24f6b1156e5d65657148`  
		Last Modified: Thu, 14 Aug 2025 18:50:36 GMT  
		Size: 1.1 MB (1083514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316e9eecd02a521a3ae56f56f8c8424e494df30dcbb73367d000ee2612ca7ce3`  
		Last Modified: Thu, 14 Aug 2025 18:50:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e70f59a2c375f9aca073af3b40e9a55ac2f84b6fda3bce0bbe3598936037a6`  
		Last Modified: Thu, 14 Aug 2025 18:50:58 GMT  
		Size: 82.1 MB (82103220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77faaf2aa6d52e46b571ee6b62edfaa8f56c6c0ebc822dc333b44c17425efe95`  
		Last Modified: Thu, 14 Aug 2025 18:50:37 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda9d24ddda53f89bfdbd36dcb47789e339a0a44f66c51c7da0a36ecb56e18d2`  
		Last Modified: Thu, 14 Aug 2025 18:50:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd608f9d9553668e1b4a70dfbab5d229ffb3eb90819da4b0efdbdf35fefded0b`  
		Last Modified: Thu, 14 Aug 2025 18:50:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963f192d391a5fcd139436e61dd48a01a342ad11d2551aade76d6683a6671377`  
		Last Modified: Thu, 14 Aug 2025 18:50:37 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da273de0d1a4259ea27771a3b26cb1836000af7f1331b013002dbe6ca5ad9f6e`  
		Last Modified: Thu, 14 Aug 2025 18:50:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:36775a94418c2855478172096944dfb2f5bfe06856e4d42c3bed42b1bcdfb025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fa21e8c11e79f3c09fbb43ab90d5cce638d76abc32b77981d69e9eaf554e38`

```dockerfile
```

-	Layers:
	-	`sha256:cdbd0f350d23e10a27635054cb07fce6f727826dbbd3c6d5a36de624edf4f2b9`  
		Last Modified: Thu, 14 Aug 2025 20:19:06 GMT  
		Size: 596.3 KB (596349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed44c09bde60f3a5f92550dde8829432c933e7c9ceaa672f56a0ff5060d7069`  
		Last Modified: Thu, 14 Aug 2025 20:19:07 GMT  
		Size: 41.5 KB (41521 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:ee0bf7a076033972253f1fc05de6c7f7d1927a044aacc959e7847478bb0b7059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107564948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8df4cf5d42b653457bf053ed63a29c2e6772e6635c62ce295eb799d6c62c195`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18beta3
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_SHA256=21d86e55eea11300c3a2212647dc3d48bd844b83017cf6ce5684639ad8f95278
# Thu, 14 Aug 2025 17:31:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5c482840cf82de196008abc359484735770b13c9282408f1dca4d75164f7d5`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e157a09d862e13d8d0e716ab97e9d5a2c94438123a639c16e3eab984125883e`  
		Last Modified: Thu, 14 Aug 2025 18:54:32 GMT  
		Size: 1.0 MB (1042499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e8baf5ceef7de553a728a2b722a0c9dd8f8640b8e0595991a87034be1cd7c9`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d782398044f2454d8b93b50c768e0118424985ee9b4179a85a39e51accecea30`  
		Last Modified: Thu, 14 Aug 2025 18:54:48 GMT  
		Size: 102.4 MB (102365425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95ac8e9f25828e699b647233da8858b303c31e71db9ab1c94294b4fa394372c`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500d6370849c702ba393908b4c02d4e9585d4eea0957dc005078e74d85cd8bcd`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae329b5e19fcdabc967c8c396a2d7adc73e3a99e92d026bf5be878d2e0eeff07`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280ab2f459ea514aa3ab3f5043d5ab1ba1e5e6689f7520b8b0094e17c4bee2da`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 5.9 KB (5922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc39101afba360b9019c48928b1ce751ed0e691f852ef651b33b2e018e7340`  
		Last Modified: Thu, 14 Aug 2025 18:54:32 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:3c05741270725331048eee8ba01c4c20e1404d7a8df4f03105cbcb116e7499fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475d9eae13ed7917d7727d45eb90d016338504964f841598ba9884d83f9b7608`

```dockerfile
```

-	Layers:
	-	`sha256:ef97e57f4839c75fcc8df18705e2c580dce367184339875904485bc078c7ccfd`  
		Last Modified: Thu, 14 Aug 2025 20:19:11 GMT  
		Size: 596.4 KB (596361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4914b61be8a6666adf90db1d180eae0e45581ba7fac331542ad03642e1f0610f`  
		Last Modified: Thu, 14 Aug 2025 20:19:12 GMT  
		Size: 41.6 KB (41562 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-alpine` - linux; 386

```console
$ docker pull postgres@sha256:ac9bda108b06ee18bf255e79eb05698a04751d39b02aa6e911c7a388822eadaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (118023905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d5d2d9b87da618bea659d540bef2dbeaacf8280f1576ec86c728dbe7a83f20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18beta3
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_SHA256=21d86e55eea11300c3a2212647dc3d48bd844b83017cf6ce5684639ad8f95278
# Thu, 14 Aug 2025 17:31:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f925e90312964d3606f035c33829ea122a45e2a86bfb919d814b7c32346875`  
		Last Modified: Thu, 14 Aug 2025 18:33:45 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0184333588e1a004c253748bd641d8cd326df446ba596bdaf6524b08b24ad3`  
		Last Modified: Thu, 14 Aug 2025 18:33:50 GMT  
		Size: 1.1 MB (1091515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7960bd43e7e7093fc87228eaf9f132681666766f6fada680c0a498256ce300c7`  
		Last Modified: Thu, 14 Aug 2025 18:20:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b442c0d87cfb9cca3acf48ddd492ec049e1633edc9702de2f0396298a5222d`  
		Last Modified: Thu, 14 Aug 2025 18:42:37 GMT  
		Size: 113.3 MB (113291095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38919aaff432536fc04573117a0714e715866f98862793cb0819dbf0d06f3e9`  
		Last Modified: Thu, 14 Aug 2025 18:33:56 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54426dad0f6a4162f0315255ee92fb1f5d7155c1d0439766dfe9473f5ec326f1`  
		Last Modified: Thu, 14 Aug 2025 18:34:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3cf95368bd765124bb86f2cf2f1a8da2d8f7c35fcfb05161589e3efee3f109`  
		Last Modified: Thu, 14 Aug 2025 18:34:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe22c6076267bd76592dbfbee14b6d8d975eb4612f27a99439032a462089184`  
		Last Modified: Thu, 14 Aug 2025 18:34:13 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a33da41905a62fadd268150266d669bfa93d0d321da6f23672d93c9d33a18c`  
		Last Modified: Thu, 14 Aug 2025 18:34:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:5b3df92f5c482be5ef6d788a9384edcc1b4a65dc7af36aa5806c471713b9963b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.7 KB (637655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352aa5deeb2e54bf40aeb2864a799820e113d2a8b74d7d0f7450dc34b90db74d`

```dockerfile
```

-	Layers:
	-	`sha256:5f6da7a4368a6d2ef886a8f80389f09671d4e98d47296c3b54d5238bd0cf3ebe`  
		Last Modified: Thu, 14 Aug 2025 20:19:15 GMT  
		Size: 596.3 KB (596314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5790526ec2331a09fee155059248d106d875f6a9c955981ccda6d721fa866911`  
		Last Modified: Thu, 14 Aug 2025 20:19:16 GMT  
		Size: 41.3 KB (41341 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:2c2e5b055d892e5d05416fda930e652fd934e25994b4360f2656603019fb5b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95531430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb28ba45358b05ac318775f87cfc9a6e07616f1356d63c7fd17e6b1196e8bc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18beta3
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_SHA256=21d86e55eea11300c3a2212647dc3d48bd844b83017cf6ce5684639ad8f95278
# Thu, 14 Aug 2025 17:31:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5ee779caf31f6000861b5a827cc767777a7e523406271d594906edba47fb17`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39e84474c9e8b921b5d1f181c420c8539aaff375b40eaaf2fb3eaa645a3f1c3`  
		Last Modified: Thu, 14 Aug 2025 19:04:34 GMT  
		Size: 1.0 MB (1032220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e3db6901ab70acd1d995ed99e8573dea313f7a01c50aaf9406525d32cee2f7`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec44698b518bca4c9bf4b540da42b7d2f3b2447e9978f89c8cfb729028c2e625`  
		Last Modified: Thu, 14 Aug 2025 19:04:39 GMT  
		Size: 90.7 MB (90745800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce668044ae3f10bc977ec5ee7fc60bec2ea993b5784f01957bf7457092adc726`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 18.8 KB (18780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c71e2b318b4fbf460260ea7d410eec4e6d7ef67183d87a43e2bbe9b2ff9a4d`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525a16bdadc45858bcecfdb038a4a001dd07594aed5bb4e6a765304a5dac3986`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80eac2e294f32952718ddec33129865d638a56b47f88684dabd1003d711223e`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9481b17ebad7be1121bdbcd23a3023bdea0b71de2d7164a271ec9a3da16664fd`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:85155a71e1943cb2c434e91f5b8d0a92ca1ad94d564dcbe5f970caf9bc05f947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf57b0de51380ddfa18e10e36ecbc1b281ca9035c4c162117261be49f21bce3`

```dockerfile
```

-	Layers:
	-	`sha256:a9e196d4bfcb7ad42af12368e33e4f1d199f4ffb0700174cb043db8e8b192e6b`  
		Last Modified: Thu, 14 Aug 2025 20:19:21 GMT  
		Size: 592.7 KB (592738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:143855a6e7e3a3b660e46aab3ac21a103bfe22ac198a6129f4e24accaa36af90`  
		Last Modified: Thu, 14 Aug 2025 20:19:22 GMT  
		Size: 41.4 KB (41416 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:5176524abe7df754c429ede47496f7306caa99826c8f9c869642b2cdf0de3ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120417843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc4d0c0c0c89ebc8cb712388e74410d345d30ee2e9899fc297a713ce7514bc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18beta3
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_SHA256=21d86e55eea11300c3a2212647dc3d48bd844b83017cf6ce5684639ad8f95278
# Thu, 14 Aug 2025 17:31:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d38346a6df0fbebdd4778252bbd39ccc90b12f4fad75fe53f1e3c72e66c3a5`  
		Last Modified: Thu, 14 Aug 2025 19:23:02 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0825e8e3a340fc788e6927d6d834d1119ad7c294a2a2b22dae232cf44b292106`  
		Last Modified: Thu, 14 Aug 2025 19:23:03 GMT  
		Size: 1.1 MB (1081138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea3f727da024f1366d4f6c638daee81eb74edc322397336acd9044d9a59407e`  
		Last Modified: Thu, 14 Aug 2025 19:23:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee35545aedc9da438f94c4eb86db0178aa5532417f8af4166cff6d2717ea299c`  
		Last Modified: Thu, 14 Aug 2025 19:23:09 GMT  
		Size: 115.7 MB (115665437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f518fa4a23c01b3f8df60240ed0fee61905b9c21bd150617b4be4951383a0b`  
		Last Modified: Thu, 14 Aug 2025 19:23:04 GMT  
		Size: 18.8 KB (18782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d52539d9c06a5b82b40a3a327195b1dd8405470b2f1fe764c4df24a959efa0`  
		Last Modified: Thu, 14 Aug 2025 19:23:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76dab33a1d773ec3446918be879550eb6a752d9b54dd9e4b9453a4d597b1822`  
		Last Modified: Thu, 14 Aug 2025 19:23:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cfdf6281b3b752aaf4917c4c4bc35c594bc41a5b748d03ad158cda56fc2f11`  
		Last Modified: Thu, 14 Aug 2025 19:23:06 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1577d8a7590698f6eba0893569085e728205a1138048b0546be2bfb13e291ea`  
		Last Modified: Thu, 14 Aug 2025 19:23:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:77b59818f87990530c817f4f662bd0c67228a5dc616c3dce5fbbad60380ffb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.8 KB (635754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acda946161ef9ed36d4e1d3c3023d9e995110742f7e81bda6e553240bae6ff54`

```dockerfile
```

-	Layers:
	-	`sha256:0e534dad4f4257681fb2ef0862120a9eb422ed1fc4f43809ccf077392d041cf4`  
		Last Modified: Thu, 14 Aug 2025 20:19:26 GMT  
		Size: 594.4 KB (594378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f5b3be3aded9706d48a8e2e8f03c7cdc8dfbb4d5b397bb0f34f2b9c78315f62`  
		Last Modified: Thu, 14 Aug 2025 20:19:27 GMT  
		Size: 41.4 KB (41376 bytes)  
		MIME: application/vnd.in-toto+json
