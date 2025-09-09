## `postgres:13-alpine3.22`

```console
$ docker pull postgres@sha256:8788da36ce67f9ca979269600f7f92299e01cd0de58dcb34012a8ac2c7038f1e
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

### `postgres:13-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:af136f398def20b9cc79b4a464d72f9489ea1938f582d4b4d4bd003f792c432b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109216028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479196f38b243f430e8c4d897341fdfbede2ea49183e3b849789d81ae39037de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=13
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=13.22
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Mon, 08 Sep 2025 20:04:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21776b025dcb55138cf944f4f7dec351dac5453be8e781660613676cfc99c84d`  
		Last Modified: Mon, 08 Sep 2025 22:43:03 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb971df70ec716e8fa1f0b0ca7ed8db16a83a45053025a8e2ca88ebf98ba828`  
		Last Modified: Mon, 08 Sep 2025 22:43:03 GMT  
		Size: 914.8 KB (914828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7245e957aec1b5283937d187a902096cf70e68bf190f44852af9a084da27941`  
		Last Modified: Mon, 08 Sep 2025 22:43:03 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bff56721e6f1908cd6af55c58f7e6018880df3e60a2285916c9f3ea2c91fca`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1745a21ce40eab33effc16f34567cd4808e028133301e89ab228de49b2a6981a`  
		Last Modified: Mon, 08 Sep 2025 23:07:42 GMT  
		Size: 104.5 MB (104484827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae286444f5a3b202730930b81550724de2a478189e3c53645338958614e1f47`  
		Last Modified: Mon, 08 Sep 2025 22:43:03 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8b83913867063a4d294a407e6551706245b2dccea5676cd93858946f408788`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b882ef9c2195bc3f4fa85d13098f6ab63991477580f73774d83930ccecd40d68`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8840459915fb5f715d311e49be8b61cf3a4ebd1ee3893cce2cc0feac6a86d5`  
		Last Modified: Mon, 08 Sep 2025 22:43:03 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcc48ce1640be321a3904b0f039d2d34a36e5dde52522169d77295b87bea108`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:87a64373219a9da25680116cedf2badbb765455c3c9d55a75d8190d5280b3cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75ac9d29ea48d788645c566963024ac4e9e6df5ace477b29cc0f5b772b34a3d`

```dockerfile
```

-	Layers:
	-	`sha256:bd5a01880e61bd81e2ccc9105e1e4556dfc0b58afa1368a1279519bbdf656cd4`  
		Last Modified: Mon, 08 Sep 2025 23:09:14 GMT  
		Size: 593.8 KB (593802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3342ca4966de5f8631f9a2b3cd9b728850c0b634ae61bcfe423da18e670258a`  
		Last Modified: Mon, 08 Sep 2025 23:09:15 GMT  
		Size: 43.8 KB (43761 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:24d27c39222426c7891adc4fef97c1235b1b7af2ce7efcfd1428b54cba7f7ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86576090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58333d6c391365b65b3f1bd7fee7c3639f3e4d812d090fe6ac6e984007995b11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Thu, 14 Aug 2025 16:07:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
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
	-	`sha256:7112f2e184ceefef9eeff37dd72d2f7909f3a223202968b7606e35232a4f6866`  
		Last Modified: Tue, 15 Jul 2025 22:16:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a57156ff7ae7b2ba746fdc40a1ad960d3dfd641362dd61bc3ad15b940144230`  
		Last Modified: Tue, 15 Jul 2025 22:16:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dc0c4fc6be80570eba0fbc53f1fa60994eb1ff36cb101b17c4d9a61ca5c40b`  
		Last Modified: Thu, 14 Aug 2025 19:01:40 GMT  
		Size: 82.0 MB (81974991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ddf146786eb71b29d7ff565670a6b0bad2f1af525afc4b5665281853d9468`  
		Last Modified: Thu, 14 Aug 2025 19:01:33 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8631d8df6d6eb0fbc711446d278b446940089600c003fa6e184c3f019385d3fe`  
		Last Modified: Thu, 14 Aug 2025 19:01:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a49d4a45b98de72db079a82d4db8b31790c4a703b18e1a1869606847cd632da`  
		Last Modified: Thu, 14 Aug 2025 19:01:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9377399bf5b073fb4ef39f68a115c7a19b6aa6fcc8f02ea910b54261672be5b`  
		Last Modified: Thu, 14 Aug 2025 19:01:34 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e05c2008c31aee8fb3caaa6b67a282ce91d94c71a38866b667f6e647e55be`  
		Last Modified: Thu, 14 Aug 2025 19:01:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d62ab47d6a40f004b86c286b82ad78b0d3e07980ff97394794185fdddf2ef24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215936e0ef48e7f9326fc32b265f664184db6c158d268c221f6f37907a0e3c27`

```dockerfile
```

-	Layers:
	-	`sha256:2a103e5b96584c247eb2fa679b48fb2d13a981ab8375bccb9a82a252d6fa316d`  
		Last Modified: Thu, 14 Aug 2025 20:07:45 GMT  
		Size: 43.7 KB (43729 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c1bd277b1ff10e7a24ae71ff73895cdd23f98ca46600ed10bf31927734f6e0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81919221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395d84d8654b41398069fa5a6622f5c91bd7db735403b3328e62817c5941eab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Thu, 14 Aug 2025 16:07:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
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
	-	`sha256:1dbeb9513aa078b0eb8ce4bf6d95a7b7787beb9460a2af8d19a69c827e22729b`  
		Last Modified: Thu, 14 Aug 2025 20:10:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b458e6c32b35c52476942d750d16263a199db15b9a6e0c8c603fca6a5f8a2f1e`  
		Last Modified: Thu, 14 Aug 2025 20:10:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a008a68bcbb5aa5826a27deb169d3a7a793dc863943334da5b1366f007e94f41`  
		Last Modified: Thu, 14 Aug 2025 21:42:14 GMT  
		Size: 77.6 MB (77599973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb96aea44b1ea56dbf657d00ba76a308c3889b21106c0ee831acc48739a2256`  
		Last Modified: Thu, 14 Aug 2025 21:42:05 GMT  
		Size: 9.0 KB (9019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406e3bc4e10dd99051b528d3249865aa1153d2a15de38c6f9231032c7fa07e1f`  
		Last Modified: Thu, 14 Aug 2025 21:42:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333e3fc46f08075614e8388e9ad5797f44f35ab769d3abc3e8ed0d6677a69e11`  
		Last Modified: Thu, 14 Aug 2025 21:42:05 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682572af1c6cf45788e55892c95d966ed3a74e52ac02afc5b47da99d47aaacb1`  
		Last Modified: Thu, 14 Aug 2025 21:42:05 GMT  
		Size: 5.9 KB (5932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e06a1fdbea1f035d72fce49d5e6f33c05721abd9b7e9318e697d2bd5f41806`  
		Last Modified: Thu, 14 Aug 2025 21:42:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d0fcb6363a7216b8dd9d98be943217cf6f678a7c6585a1ba510bd5c1eca51f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73795b80aaea4bf82298fe3b956a0186b00909b8ba3812c754f35920e61c3f21`

```dockerfile
```

-	Layers:
	-	`sha256:9cbbe4eb186299460c6f8f5b3a0a2da2b56ce574add351329c5a1b6a4562856d`  
		Last Modified: Thu, 14 Aug 2025 23:08:05 GMT  
		Size: 593.8 KB (593842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d55df27c1b154353c1575aed51105a4c3767036a39a8c1ce46fdcfd20c440ea4`  
		Last Modified: Thu, 14 Aug 2025 23:08:06 GMT  
		Size: 43.9 KB (43943 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:219aca9e596daae0a568fb8cf09db03e3488b563939420849795e59a30778403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102877697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d42ccab9a0fdd53577c17e3d82a9d6520e476d2aba6d6e49b554e7c69b5bf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Thu, 14 Aug 2025 16:07:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
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
	-	`sha256:beeac069caed963f46280d25489c8441ffe149df80d1667eb2108c8069089456`  
		Last Modified: Thu, 14 Aug 2025 19:09:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fac8997d1dffe2a81af36fccbdaf990b3b0a3dd0146bb736836b02cfc6164dd`  
		Last Modified: Thu, 14 Aug 2025 19:09:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650aa58d9e5deab64c3246c98c5c8165dfc3dacddcf2adb51702eb525384233e`  
		Last Modified: Thu, 14 Aug 2025 19:31:42 GMT  
		Size: 97.7 MB (97687762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b222902230a44edf417489b71eb007805e94dd9ccde97a67775bd06b04a9acbf`  
		Last Modified: Thu, 14 Aug 2025 19:31:33 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5a2dbec041c64a8b65b307dbf74bad3ee4776fea66c48a440623b417d782ce`  
		Last Modified: Thu, 14 Aug 2025 19:31:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdf99bc50897d2beda52138903f2c65a7d94a90228a27882d6af234451a729c`  
		Last Modified: Thu, 14 Aug 2025 19:31:33 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d45492d29ab63534b7683b5cee72b114c34cb7ca9adcb0ca957436190205066`  
		Last Modified: Thu, 14 Aug 2025 19:31:33 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912135faa333f2de16690cdd25e4784dfaa7899399ca8c5e58d0bf187f510080`  
		Last Modified: Thu, 14 Aug 2025 19:31:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:75d121ab173a29d03b4d510a38fc4d273fa6b234db13ac5e3faa96822e8dc239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00caf4b83814ae2af46facf101fdcb24ecf04221cd99e971649f7c9fbcb011f1`

```dockerfile
```

-	Layers:
	-	`sha256:5d1f4e36088ef692f94e7b91ee607b457958b393db3516119a50721b3d49f6fd`  
		Last Modified: Thu, 14 Aug 2025 20:13:33 GMT  
		Size: 593.9 KB (593862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d859d1ccf464f640877697a27d40b80ab51276bf27c15d4ea474cfa6c72c3ad`  
		Last Modified: Thu, 14 Aug 2025 20:13:34 GMT  
		Size: 44.0 KB (43988 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:343086173ea590f2775cfc33c362ad85e30bed0bddd5fcbc42dd813eb95428d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115193318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4475fa5d5845c596c745d90b51bb2c37c28e16b7fc3c4f33667809ca01c72f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=13
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=13.22
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Mon, 08 Sep 2025 20:04:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a979e62e4d692e05350595c651f1c50301aca561ffb7c94ba7f6297902c5e12`  
		Last Modified: Mon, 08 Sep 2025 22:43:09 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb852dbe5c00815c1c9e196b3c0732abf1950855f90e16d642a38369d5178d5`  
		Last Modified: Mon, 08 Sep 2025 22:43:09 GMT  
		Size: 885.2 KB (885199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79366fa3949a4d02dc27da2355610fdbf94933c12d5a175adc26f5b7b5962640`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099a6794d5b8f403bf0477caefe86f4091a02a17a2991a6a8ae9a9198b14f9d3`  
		Last Modified: Mon, 08 Sep 2025 22:43:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954dc4b78347d6cb1e21a6d6420a66c71380b6c9d5de3cbffb5c5fcabbd75ca3`  
		Last Modified: Mon, 08 Sep 2025 23:11:22 GMT  
		Size: 110.7 MB (110676435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5bd635a0affffbd324ac4c9bcf4abfb9b6439a254ce2ab4d59b24c318de7a0`  
		Last Modified: Mon, 08 Sep 2025 22:43:09 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9914712f17f68ca42a90174a7f5384601574ec207e18206d8ecd260d85ffbed3`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfffbc70614913fa076129ed608f27295be82601b24a9c5a5132bf5626abe5e`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3fe047d28aae8b7194f34ddd8e2e7f167edad3bcc3c539ae45e4e2a204118e`  
		Last Modified: Mon, 08 Sep 2025 22:43:09 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ad6ce93264c63d985d3b0504a84c80664abb644b742fdba9c9fb16bf3f85b6`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:f988ea0028677f0a4e07ddec5b30ec824f99d727ddfef8a8fb94ebda2d165365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1096a2b90c047d0faf1f957038aeaf04569b5c799fbd75892eed6ed8610d41a`

```dockerfile
```

-	Layers:
	-	`sha256:7f48bde82a4f42c0199c71dc009f7e14c6b3bcf553885a68c121e3803b4047bd`  
		Last Modified: Mon, 08 Sep 2025 23:09:26 GMT  
		Size: 593.8 KB (593777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02849006ee441750e693c0b773fddd5a25640576b883eb1cce40da77226f8eb4`  
		Last Modified: Mon, 08 Sep 2025 23:09:27 GMT  
		Size: 43.7 KB (43713 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:0c7f3d5a494b0ecb69dd1c5aab09e9c60d6a20ebbe7a80755e1de23a14a83cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90452515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445fba602b0612dc1481043d04ef7324afc7f01000e57615fb787c7b0d59101`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Thu, 14 Aug 2025 16:07:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
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
	-	`sha256:3e94ccd247fc85b417afdbafd53b06d2487171dda880c5aa0bd753a507fa6bf9`  
		Last Modified: Thu, 14 Aug 2025 19:28:31 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e2935a77d21eae07c28aac1c8fc1cacc4234ba4c89db92756482884273dd1a`  
		Last Modified: Thu, 14 Aug 2025 19:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d65b2c8651dc77a20d6df3ecf70ec5583d470388c3645892752e2e65db437c`  
		Last Modified: Thu, 14 Aug 2025 20:03:02 GMT  
		Size: 85.7 MB (85676483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26072518abfcea6ca39e7e52cbd2a0b8b772aa78ac43aee68b12b4fea079484a`  
		Last Modified: Thu, 14 Aug 2025 20:02:56 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8791945f91d12d68483ed8f62707063e5d997b70bb793326ac3c12b49c7a4eab`  
		Last Modified: Thu, 14 Aug 2025 20:02:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1f96038225ff6826146d006943d53b309d0ab1a4feebc0d8452a993f77d5d3`  
		Last Modified: Thu, 14 Aug 2025 20:02:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f439e304356ac8d100fa600466686652cce6bf5ab327dadc2ae9c9b17bdab51`  
		Last Modified: Thu, 14 Aug 2025 20:02:56 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a37006f58b36b4022c80dd29b8173536a510f0e21e573117d3f43decd5609c`  
		Last Modified: Thu, 14 Aug 2025 20:02:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:27d59ab33333ec2dc9a43d4c39234b4286b7a4b1cc8702de39f3d86face7115c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.1 KB (634051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87204df8d7fe4365cfeada6797c00eae1c15555370e5ff10dd31ca0be14a3d0`

```dockerfile
```

-	Layers:
	-	`sha256:8ff8a3d360bc76bcf161680e37dc06c7f648882529c348ea074b474490584b1f`  
		Last Modified: Thu, 14 Aug 2025 20:08:34 GMT  
		Size: 590.2 KB (590227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a19a74af1be87c66010add6ad4f23a1fd0b3d1dc5b6fcbd62d48371f9c5791f`  
		Last Modified: Thu, 14 Aug 2025 20:08:35 GMT  
		Size: 43.8 KB (43824 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:b843ec0ba4560b90acd8d30f92a3babef284f449cac49bf98a586d1458125909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106350586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05882eddb7e02d624ec8f7ae7a2c1757b1ce9c1b7fd060fb9ad0adea5bfcc932`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Thu, 14 Aug 2025 16:07:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4bf5c01f5fd5d5c2b6c78d1d884c92b6fce072812c2b64d8f250b5d9d572a`  
		Last Modified: Thu, 17 Jul 2025 04:54:24 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac990c2f318af1f8860277d49db61df409ca94944240be61871dfc66778de791`  
		Last Modified: Thu, 17 Jul 2025 04:54:24 GMT  
		Size: 1.1 MB (1085426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b33213ad7c82c53f42dd029d8472109832ca58ee1b8dc61acb10fa01287ff8`  
		Last Modified: Sat, 16 Aug 2025 17:17:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dd99086a41070f08f3ae290b775e11d3c8145bd7206c29fac7870f2b6edab4`  
		Last Modified: Sat, 16 Aug 2025 17:17:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfa792b6ac2cf5bc00857f5a7b2171ce3cc380c79f0bbb46bc75cd3cbb45d37`  
		Last Modified: Sun, 17 Aug 2025 04:11:41 GMT  
		Size: 101.7 MB (101735657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17901eed64b682578dc4150abc9bbde3b20a1c6d24dee4a55d3b4ea01d086166`  
		Last Modified: Sun, 17 Aug 2025 04:11:32 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca4458d4316493c19694af4f4d17ac63cdc701d2056a99ba83a97ff6577228e`  
		Last Modified: Sun, 17 Aug 2025 04:11:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28ad578fb9ff18c5ed1912eb8a8946775b9c0d2b371e31776bc82bc4fc7726b`  
		Last Modified: Sun, 17 Aug 2025 04:11:33 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb5ae977b60bea899a2a3e3c5d0be4fe07cabc36aa6e43747d7d3cfb22b8ee`  
		Last Modified: Sun, 17 Aug 2025 04:11:32 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbe91d3965ac1dd6ae18fd3033c3328d3bbe1d86887fed7585667df3caec5d8`  
		Last Modified: Sun, 17 Aug 2025 04:11:33 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:931bb39f420009b8fda8c0590aa8a3a051381c65db3ea5857a7ee5c97ed418f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.7 KB (635715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1a5d71b403acd47938fa003009e60557c790d96623348f0073745539e06a18`

```dockerfile
```

-	Layers:
	-	`sha256:7ebd41f11e417fe15cb05ee041e1c3114b51ac3039716a204d4302933c055e18`  
		Last Modified: Sun, 17 Aug 2025 05:07:44 GMT  
		Size: 591.9 KB (591885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8198215139ce63cf5acda3d914a09c2fd350c74d8f8eb1f57a34e2d7f24aeb5a`  
		Last Modified: Sun, 17 Aug 2025 05:07:45 GMT  
		Size: 43.8 KB (43830 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:59a114e794de325d132d74c4b29f26b7bd3828550c6c773343f586b19c2c843f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115468851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dbeacf07ebe0a521e66cc026e657b818b176fc6f52d4dd47bdb7531d7b1ac4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Thu, 14 Aug 2025 16:07:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
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
	-	`sha256:0c48dde862abb0bf8c1f4d6d3973dcd647cdc3c112341269fc042560074724b1`  
		Last Modified: Thu, 14 Aug 2025 21:07:27 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212811b83d554e8223a575869c18d4bdcde2acb8bef094cc619b59440c3584f2`  
		Last Modified: Thu, 14 Aug 2025 21:07:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dad05332931f5a434d6ca0895309f2b8f55a285a6946a9617b3421df08bebd`  
		Last Modified: Fri, 15 Aug 2025 02:27:40 GMT  
		Size: 110.7 MB (110726055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa8de7fd2103f640c50f00917c3ac607c62aa29b4b4a68cab40bd38e04c6c25`  
		Last Modified: Thu, 14 Aug 2025 23:08:28 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceef41595fcd3958d86f7b20e6117056f7aed114f85ba021419bf52a3fcd8e5b`  
		Last Modified: Thu, 14 Aug 2025 23:08:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba061c06491b701c8903b23940f34a17216ff7a0163564643359fef0cd262a8`  
		Last Modified: Thu, 14 Aug 2025 23:08:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58a6bd04e7b4f6ecf87507b1ce85d2d6eb90593a995d55d78058161dc6174c`  
		Last Modified: Thu, 14 Aug 2025 23:08:29 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e816fcd439ee697b9894339d31399578866cd1a964db6bec0e9afd5154917f`  
		Last Modified: Thu, 14 Aug 2025 23:08:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:35837ebf2fdcc52acf10dabdf8a990d810d20f81a989ac36d161de74122222a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.6 KB (635625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad6871b7db6017ec0109e3704312a332d078f7d6d84258a274140d49e78a412`

```dockerfile
```

-	Layers:
	-	`sha256:cabe85077935654d93289fb8e47fdbfff412ea1a70e4d0633cb8041902d98a66`  
		Last Modified: Fri, 15 Aug 2025 02:07:42 GMT  
		Size: 591.9 KB (591855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d4a8e6861af8cf715bccc4ada68aaa1b04167541eddf14add1dbaa2bdb1702`  
		Last Modified: Fri, 15 Aug 2025 02:07:43 GMT  
		Size: 43.8 KB (43770 bytes)  
		MIME: application/vnd.in-toto+json
