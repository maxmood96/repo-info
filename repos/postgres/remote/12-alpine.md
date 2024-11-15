## `postgres:12-alpine`

```console
$ docker pull postgres@sha256:ab3d275fff0d3848e46d7aa0e535eddca1f1d309a7af05af41e328c3986b51f7
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

### `postgres:12-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:c7711eb8c792e72e371b1d5822e902b3ac9143a272029a15e61cbe40d9b0ecd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95447290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d86977ae1c3df3483aae8d3b7dcfde62ecf27b6db8d54248fec75bb5ba7fbca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:38:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_MAJOR=12
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_VERSION=12.21
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_SHA256=6c711550ac1cc7828865e5823d9f457e3bdad6f4320177169f90e419be0c27f2
# Thu, 14 Nov 2024 18:38:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:38:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:38:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:38:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1354598a55bee20904544bfcb83e2131f1c868a6baa5bfd384c641a47280fa`  
		Last Modified: Thu, 14 Nov 2024 21:10:39 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2411e2b87be6bfb473edb79bb1e0b0e6bf23fb9aaa55701048d1d6b1d01994d9`  
		Last Modified: Thu, 14 Nov 2024 21:10:39 GMT  
		Size: 1.1 MB (1119772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4ef45323c238d0dc96ace5fc590931d6d976d70f48356bf578ef472e349374`  
		Last Modified: Thu, 14 Nov 2024 21:10:39 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2600f5a289b033fd32cb6ba20ca64b8a9d245ba1deb63e89ba8ae9b706f0006`  
		Last Modified: Thu, 14 Nov 2024 21:07:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6cba8bb4b6aa3098a88abc36b3a2995662b362fd1fa8454f8774a978195e65`  
		Last Modified: Thu, 14 Nov 2024 21:10:40 GMT  
		Size: 90.7 MB (90687758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c974e2f076f269fa8bfcd2fff8c4c0123259b92c91be54ad4de8166aa1384df`  
		Last Modified: Thu, 14 Nov 2024 21:10:39 GMT  
		Size: 8.7 KB (8682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208388a38fa46f68bf6def3f822d5a406877361ea23d07c763028280eab5374`  
		Last Modified: Thu, 14 Nov 2024 21:10:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f3a374432a176cf91241b403eb3524c7a12409c81e14b2ef9144354ce21553`  
		Last Modified: Thu, 14 Nov 2024 21:10:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4781242b63248d6a5d5623268555f0c104dc0c6bda8d2ecfdb41243ad10344e9`  
		Last Modified: Thu, 14 Nov 2024 21:10:40 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b9c4517dd398d6aa7ef734cc5fd84c384deb6cea72d81702d685df3ebaa751`  
		Last Modified: Thu, 14 Nov 2024 21:10:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0b1898d01c9d8adb8275877eee11a4d44877146084d2d91d6f28fc0f1c65883e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.4 KB (633383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6aae82ec1a43f583fcafc468a675b2d3793cea8baaf8a6987c1c49a5056f55`

```dockerfile
```

-	Layers:
	-	`sha256:ab1c38ddb2bd0638bf3192eaaff0c5ffb9a32018091ab609865fc8a2708ee1f5`  
		Last Modified: Thu, 14 Nov 2024 21:10:39 GMT  
		Size: 588.1 KB (588073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b505d59208d9e972e524df131a3bc09aae491ce1a5f63d0f4ae51f8f75440720`  
		Last Modified: Thu, 14 Nov 2024 21:10:39 GMT  
		Size: 45.3 KB (45310 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:3f15440accd7d41e629d26233b1a0b8db7d49ee9f71a4cfe8dd1f82c07501939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94004859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409680c06a20f70a47e9a79e66b608be317c5a8a6f718693a9f2c96ced1f52a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:38:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_MAJOR=12
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_VERSION=12.21
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_SHA256=6c711550ac1cc7828865e5823d9f457e3bdad6f4320177169f90e419be0c27f2
# Thu, 14 Nov 2024 18:38:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:38:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:38:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:38:07 GMT
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
	-	`sha256:fc73a47f5b9d8ce9596f97f66971f1bbea17ad10037021b00aade1a18f429fce`  
		Last Modified: Thu, 14 Nov 2024 21:49:24 GMT  
		Size: 89.5 MB (89535935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b741a8cd183d7c0b297eecce1d67b7c862867a3cb7d229ceea454493014f547`  
		Last Modified: Thu, 14 Nov 2024 21:49:21 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94687b7e4718cc8dbfe0c2de397b2eddedfd8d5b4af524c6d6cec1d76c1d4373`  
		Last Modified: Thu, 14 Nov 2024 21:49:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613538d9231ee9a9ab272550c5444fc0a84cd6b7cbed48e8899df176bd1056e1`  
		Last Modified: Thu, 14 Nov 2024 21:49:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0691a32d691592f9e4221db701fffeeea6fd9af299d48d551400de8ed344398b`  
		Last Modified: Thu, 14 Nov 2024 21:49:22 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503e855782903f569e0d237fa92e2c8997828d4f2696c6f61a9aa087a438f1f2`  
		Last Modified: Thu, 14 Nov 2024 21:49:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:bac9a9aac31303eed23db40075ffa5af199eafcb27a27eaffd01452b4db71a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 KB (45275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa058a0905e98f393637033d0a980f7683f657cb87a88ccf5a779fbd0d007576`

```dockerfile
```

-	Layers:
	-	`sha256:3ecd8d15cf67b7e8add6f1e0d3cccfe5d144020689755e1b1c9e4f13dfd242e3`  
		Last Modified: Thu, 14 Nov 2024 21:49:21 GMT  
		Size: 45.3 KB (45275 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:0d6ea3ca5b08c8379f4d94b0f5b1739d3f07f7d2db81902f222f9069839e9834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88353442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6275e43f05308bf6b823af6b57a4843a4ec954b9c78565c5ea5de41625d0e3f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:38:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_MAJOR=12
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_VERSION=12.21
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_SHA256=6c711550ac1cc7828865e5823d9f457e3bdad6f4320177169f90e419be0c27f2
# Thu, 14 Nov 2024 18:38:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:38:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:38:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:38:07 GMT
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
	-	`sha256:7c2d243da15f94f2ecfc8ff7acd757e788fd12a0f3814402c2fafa0d9782339e`  
		Last Modified: Fri, 15 Nov 2024 00:43:41 GMT  
		Size: 84.2 MB (84155623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271bfb92f31269b1c8ef94e52a75f8ee74ba7df55d78338373e688fb2570b7b6`  
		Last Modified: Fri, 15 Nov 2024 00:43:39 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceff697a97a1d78f3e8c7d77fd2fbab07c9d4ca67bed6cccbd07f8ce1bce74e`  
		Last Modified: Fri, 15 Nov 2024 00:43:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e397352e96b27c9418f68517342038b6e6a77b56751644feeb622113f10de322`  
		Last Modified: Fri, 15 Nov 2024 00:43:39 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e1d2113f40d130fb6be9c6b2ef8e425086fdb1f605e3caac6ae0335dd413b9`  
		Last Modified: Fri, 15 Nov 2024 00:43:40 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce509adba3def4c71407a0dba3dff972f72246d6732ff46ee738ce6fcae3da3`  
		Last Modified: Fri, 15 Nov 2024 00:43:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:9e3e0e7ef344812c45361531ca37e9b3002e8cf2d31be0bbb09e6b67ce746a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.6 KB (633599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7277f265edc49380d88b026bf310caa3ef23935a287240ee3c6667d3eff8b858`

```dockerfile
```

-	Layers:
	-	`sha256:6efc04c859a80fe8583a2b0d134711e37e046258f6545909cd0f0094a29a9ea1`  
		Last Modified: Fri, 15 Nov 2024 00:43:39 GMT  
		Size: 588.1 KB (588109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a293be83c29145a07494bc3523c2ad0a3df39242793e1127321534ac34f6d5`  
		Last Modified: Fri, 15 Nov 2024 00:43:38 GMT  
		Size: 45.5 KB (45490 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:990ad5c6e80f20c23a9b62e54b9f6b23b1f2b242006934415efdde92c46fff6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95172923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e00bad9446957f170ba995338f84fc05893ed5f3cd855500aa0a97e37f98602`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:38:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_MAJOR=12
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_VERSION=12.21
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_SHA256=6c711550ac1cc7828865e5823d9f457e3bdad6f4320177169f90e419be0c27f2
# Thu, 14 Nov 2024 18:38:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:38:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:38:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:38:07 GMT
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
	-	`sha256:f89d5118f895206d065363e623cf56a6ae27629622bad86dd59763acb2e2a48e`  
		Last Modified: Thu, 14 Nov 2024 21:51:22 GMT  
		Size: 90.0 MB (90022093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cab6f588da7b69408d3b333e8a149f5f84549182da3659483c7533a9a973de8`  
		Last Modified: Thu, 14 Nov 2024 21:51:20 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98ea548c7534d812c55d80734d69f94fc05e163423475ab2dba0f620bc074b5`  
		Last Modified: Thu, 14 Nov 2024 21:51:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15adb54096a3127b20c1cb490c7ad9e5a499f5252da0802d7ef20cb80e6a464f`  
		Last Modified: Thu, 14 Nov 2024 21:51:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56abd48c1b3f017c67fabb4713e229416305f4b6ba89c67282986f3c936fe156`  
		Last Modified: Thu, 14 Nov 2024 21:51:21 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba31f2dac7e5245a6bcdd547c7288a786ca3166c5d7c51447053fc1d43a35f4d`  
		Last Modified: Thu, 14 Nov 2024 21:51:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:3c4b2a013bfa67a4c3ebba1c7656158b3b1c6fd425018f6003957eb06b0504e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.7 KB (633663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bebad75e1585c2bf4494adbdda71aac7deb37ca0638c5f472355e8143ba2265`

```dockerfile
```

-	Layers:
	-	`sha256:74077b981e9fae4bfe7cd1e0fae7bdfcad0939705c8ffe185f4d341c32a4d54d`  
		Last Modified: Thu, 14 Nov 2024 21:51:20 GMT  
		Size: 588.1 KB (588129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c81d5f1ba73d28fde04df244260d93fc24fc0dee1ed7e867477e4735a786128`  
		Last Modified: Thu, 14 Nov 2024 21:51:20 GMT  
		Size: 45.5 KB (45534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; 386

```console
$ docker pull postgres@sha256:073be3e003e5f128405b36d6b8c22c37eda1d4bf7c5f66ae9a4e7481f0b7fb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100513389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500e26c06ee9d2cfe284ef1be9952e3c50c12b389ce81b62e2daf179f05ac0bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:38:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_MAJOR=12
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_VERSION=12.21
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_SHA256=6c711550ac1cc7828865e5823d9f457e3bdad6f4320177169f90e419be0c27f2
# Thu, 14 Nov 2024 18:38:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:38:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:38:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:38:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec00eb4e4f44e887ff638d95d98ec0080499d9badf36581b0178a3b44b5a2ae4`  
		Last Modified: Thu, 14 Nov 2024 21:11:15 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644189c66d59ca2216624557918d6e67167a5a8dbb18df3cddf09419cccd35b6`  
		Last Modified: Thu, 14 Nov 2024 21:11:15 GMT  
		Size: 1.1 MB (1094866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d24dc127241ccf68f46922afd2b5f239467fb9fe738a7b972bb622c502139d`  
		Last Modified: Thu, 14 Nov 2024 21:11:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ffb44ae9fd74ddece9486b02d06deed0a70714889a80c9828294e64bf339f4`  
		Last Modified: Thu, 14 Nov 2024 21:11:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0809187868aabf656acaedf3354379efded1ffec659f59d9b4a33debffe298`  
		Last Modified: Thu, 14 Nov 2024 21:11:19 GMT  
		Size: 95.9 MB (95933440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f389182189078b96956c3cfa1068db49dfdff85f412cedc313ab134f29cbf964`  
		Last Modified: Thu, 14 Nov 2024 21:11:16 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c529d3b1b5b543b7fa8f1365da01e1bdade8e83e1749ccf9b30ec0939ef81317`  
		Last Modified: Thu, 14 Nov 2024 21:11:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff457312f2d5d755cc6b4f76ec7b0d027f0b7e8949cd266d3c3ef005aeb86ce0`  
		Last Modified: Thu, 14 Nov 2024 21:11:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617e28146866a95d4811eecfdf049627d85c39c480154fa2a9e157a1b8d9155d`  
		Last Modified: Thu, 14 Nov 2024 21:11:17 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c9d8e7bd6aa6f0c6032d4bef1e277f4eec36c5a4cca517182688cb3469a25b`  
		Last Modified: Thu, 14 Nov 2024 21:11:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:18bd2c3d2c10a84ef2ba0cf8b5448bc8c7422db1197de9278c34d3de8f4e4832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.3 KB (633310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ece37507fbde0df9254b5a45adce310939a2e1f2a7001b6c59f7d9157a8f144`

```dockerfile
```

-	Layers:
	-	`sha256:30102e27f448feced3df9e0d2bb394406b9eeee8b4086825abe5c3f623bd7e2c`  
		Last Modified: Thu, 14 Nov 2024 21:11:15 GMT  
		Size: 588.0 KB (588048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98c2dbdf2ad11c207d34d80730ceadc8e217bb3fe4dea24037744f95ebd57b57`  
		Last Modified: Thu, 14 Nov 2024 21:11:15 GMT  
		Size: 45.3 KB (45262 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:bdac3d46a8b74eeec15899cb8203ed7381673e4c06da99b92ca764f2e7ec1d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99715682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3b5038c55c97b61ae8cd62f3323af30d8c9098b2db465ed0d4e5c3a5ffb0b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:38:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_MAJOR=12
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_VERSION=12.21
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_SHA256=6c711550ac1cc7828865e5823d9f457e3bdad6f4320177169f90e419be0c27f2
# Thu, 14 Nov 2024 18:38:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:38:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:38:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:38:07 GMT
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
	-	`sha256:97af536e008b426d44f6ca9248d65460cea1bc40ac4dc4e128afdb1ce7883f05`  
		Last Modified: Thu, 14 Nov 2024 21:58:38 GMT  
		Size: 95.1 MB (95089414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b580792007f865c33ae06db6f38f61152859245cbef1cae96b226c9f479f367`  
		Last Modified: Thu, 14 Nov 2024 21:58:36 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf111c9e59f4329119946dfa213434d316700ca19dae54de72ae26af5dff08`  
		Last Modified: Thu, 14 Nov 2024 21:58:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d71f6c12544f0a8dadb5f910a7786b266be4b10c06ef6c302a245918939e3b`  
		Last Modified: Thu, 14 Nov 2024 21:58:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77e57f07c0df8308109b9482a180807c17d89320dbd8bcb33644b9f4458ab89`  
		Last Modified: Thu, 14 Nov 2024 21:58:37 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaad2bf9250a58f627f14cf9e52e266a27117a3946a1adba0e7f188ecb5f832a`  
		Last Modified: Thu, 14 Nov 2024 21:58:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8583c382dd9a50cb1a042d25e857742ffc3ee2db5919f7b748ca6db7f055e678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.9 KB (629859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf27f71df67ed0ce149a25a4d2c7a35a0763b39bb403283887600433a8f21f03`

```dockerfile
```

-	Layers:
	-	`sha256:4d40ac2b97e51697a8f06ba8ca09d27a9ba3251d614f92b5ec70513d60a8a346`  
		Last Modified: Thu, 14 Nov 2024 21:58:36 GMT  
		Size: 584.5 KB (584489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0550ec9730ecad10109e5fe1872b169d80aad6c899cbd2b36a79ccc064756f5a`  
		Last Modified: Thu, 14 Nov 2024 21:58:35 GMT  
		Size: 45.4 KB (45370 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:a0489316d1551251c6f01e61f17d2e3b83fb9d78d948e549e909e7a3d4a8a5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95279621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665d6c250d3633dce4dc5754d489f1454e1533751cbc8d3fe82e070d9bb87aa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:38:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_MAJOR=12
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_VERSION=12.21
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_SHA256=6c711550ac1cc7828865e5823d9f457e3bdad6f4320177169f90e419be0c27f2
# Thu, 14 Nov 2024 18:38:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:38:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:38:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:38:07 GMT
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
	-	`sha256:6703a51ac5271b0d8e7921f232adef671ff4184659d1fbde5bab5a08c3807989`  
		Last Modified: Fri, 15 Nov 2024 01:38:09 GMT  
		Size: 90.8 MB (90804306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6891704c10005a8dd762e852aab35acb7ae1c84210a491600c7bbc39842b3a`  
		Last Modified: Fri, 15 Nov 2024 01:37:56 GMT  
		Size: 8.7 KB (8694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ffaea5f768da82f804fc703814deb3ef9bb4bd0510aab4a5a016064f9741d8`  
		Last Modified: Fri, 15 Nov 2024 01:37:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbd7f9f4e9f38f853bc074b756b2ff4542615edc3a0ab454644306dcade9152`  
		Last Modified: Fri, 15 Nov 2024 01:37:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69eb330fe4ca0dffd16434cdaccae49107f3175c047430f6b176372b7679a0`  
		Last Modified: Fri, 15 Nov 2024 01:37:57 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f6d4ab83d533a7f7e52675a0ea90865ab8d4fdfd628c354b74d15fa68a6e7c`  
		Last Modified: Fri, 15 Nov 2024 01:37:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:42f9eaecde5e456b08c4a5ad2b962115e92121b688c11d4cc8f3462eb9167b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.5 KB (631519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56167685755a2f21420631323d0dc0517f0cfb8e607143017c6ee4649efefbc`

```dockerfile
```

-	Layers:
	-	`sha256:057a426aa3fcf3727d336927079d67e4a69cfe30e0a7649de2b0e525ba028468`  
		Last Modified: Fri, 15 Nov 2024 01:37:56 GMT  
		Size: 586.1 KB (586149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e73b7b610f8fe9f8ffa7d3dfb13ce6b6a3c2b195bc4ecc4c67b3ebd2fc39e1`  
		Last Modified: Fri, 15 Nov 2024 01:37:56 GMT  
		Size: 45.4 KB (45370 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:e6c4649dce067cb7c7c7e2f7e7d646ae5a2e1e3ae2e9d81c800c10af7ccd28fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103921417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154f21c75af94182d7bd1c70f0cc6a39f27c850ec66974a9453818ff93f10ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:38:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_MAJOR=12
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_VERSION=12.21
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PG_SHA256=6c711550ac1cc7828865e5823d9f457e3bdad6f4320177169f90e419be0c27f2
# Thu, 14 Nov 2024 18:38:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:38:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:38:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:38:07 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:38:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:38:07 GMT
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
	-	`sha256:0b7e583e322dba9810b6985f9c272be2d3c27dfbd7d2f1ef2b57c847c3df80de`  
		Last Modified: Thu, 14 Nov 2024 22:35:47 GMT  
		Size: 99.4 MB (99360630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bdcca47bdc292d559e1ec2c7ec3a7fc819f3cb1bd5f43e48efa9b70814d9cf`  
		Last Modified: Thu, 14 Nov 2024 22:35:45 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74baa636896d535a1a775026899ad160084c993d9be4391c06bd1de48f4d15df`  
		Last Modified: Thu, 14 Nov 2024 22:35:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e884d16283034e318041225b858a0468bd0e6f9818c07ab470b1cfcc405f47`  
		Last Modified: Thu, 14 Nov 2024 22:35:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7322f862c0ff7b956cf776c84b285abbf9e6670acce18f21413583823f3ad566`  
		Last Modified: Thu, 14 Nov 2024 22:35:46 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0379cdecf01cf9b992c38b8baa4ebe2fc6f76ab2eea23f3356953720e12673f`  
		Last Modified: Thu, 14 Nov 2024 22:35:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:e6a40d41e990b51c12e9633b8c35f28d6d7d9132d3775ca308c8ce3fcb065fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.4 KB (631429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210b0161f9484387aa20e8a00c0beeb91edd518c377df8be4bc26329016a1a0a`

```dockerfile
```

-	Layers:
	-	`sha256:b9c8a3d65f27ed2f0d794724856032db4151ad6496b7aa9176ec0636341141b7`  
		Last Modified: Thu, 14 Nov 2024 22:35:45 GMT  
		Size: 586.1 KB (586119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae74840f73ca865afdf359e461b39697863df59668457fa6c763049ed29b646`  
		Last Modified: Thu, 14 Nov 2024 22:35:45 GMT  
		Size: 45.3 KB (45310 bytes)  
		MIME: application/vnd.in-toto+json
