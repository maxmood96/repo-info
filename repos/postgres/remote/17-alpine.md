## `postgres:17-alpine`

```console
$ docker pull postgres@sha256:5ee0fc820fadd46a3c9ce6e3e768664cdbb1b0b763e05f7140974cf73b23f84a
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

### `postgres:17-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:08693671787a11fadf8d313e687c5f5a43de631c298bc2f2e0520f432ff1eb0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111086124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543fd794d2d9f63d895fe05cd707fb042604fe7d593d66147d86ede6152f429b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:21:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:21:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:21:43 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:21:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:21:43 GMT
ENV PG_MAJOR=17
# Wed, 15 Apr 2026 20:21:43 GMT
ENV PG_VERSION=17.9
# Wed, 15 Apr 2026 20:21:43 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Wed, 15 Apr 2026 20:21:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:24:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:24:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:24:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:24:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:24:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:24:17 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:24:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:24:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:24:17 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:24:17 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:24:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cac0301e7aac5f8acbeb4b5674588e9f0b394c310d59d39b47b0267989fd4b1`  
		Last Modified: Wed, 15 Apr 2026 20:24:33 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c3f0175d109dde71f92996494be2a6c773b9f005a67c5b5d9a8cc3719f171a`  
		Last Modified: Wed, 15 Apr 2026 20:24:33 GMT  
		Size: 919.1 KB (919053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf2ac5d71105bf4fde91039a9849acdcaf7f4d4ccef160d9a76b560534a9d8b`  
		Last Modified: Wed, 15 Apr 2026 20:24:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08afa86b00c39c8d4892364391b05747fcb8613e121ef11aa682da629896238`  
		Last Modified: Wed, 15 Apr 2026 20:24:36 GMT  
		Size: 106.3 MB (106285523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b40982aaf2fce1ff2e8d609d7a3a3f6c128b5503709df2a3b112e2af54f48a`  
		Last Modified: Wed, 15 Apr 2026 20:24:35 GMT  
		Size: 10.0 KB (9955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09a889cfcbc7f5f6c7168d2dd13eb5c7f19f8f4a65c9b48138c5e164a83b99e`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79e7253fcfa19013d16b1f3b8c4a10c9f16a8f3df01279decbc60f826b72be1`  
		Last Modified: Wed, 15 Apr 2026 20:24:35 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18eff2fcb9269e6ff11f3dee960f6d3ea48754c174f4bffa4f1dc6ee5bc99041`  
		Last Modified: Wed, 15 Apr 2026 20:24:36 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59bfad940ee6292ada747cc69bea4552ca450032cc2ec480db2b6243d56f96f`  
		Last Modified: Wed, 15 Apr 2026 20:24:36 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:712d484654ef62f6fc375aa0ed471d0c13a906388383e23978baa7e6957188a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 KB (639780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6acf846c136af4e095eb8d931043e6b153ce512bd89bdfcedd561950a5121e`

```dockerfile
```

-	Layers:
	-	`sha256:63f8214b5da46766ca40580f35f5119e6982d9c96ffb2b16c7192c5f571dcc2a`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 598.1 KB (598102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e1596fb78a575be1d8236dd17d30e530c4d7df9c29b0a7ac1ac396ad5e1ac7`  
		Last Modified: Wed, 15 Apr 2026 20:24:33 GMT  
		Size: 41.7 KB (41678 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:786323856dbee67dfef234dd538c62acf76585a065724b7125b564a36f2fe9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90486360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1924a533d874246e249c0edb98dec69b6114ba9ae35801b8f7c54ab0ce8a0af9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:27:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:27:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:27:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:27:50 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:27:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:27:50 GMT
ENV PG_MAJOR=17
# Wed, 15 Apr 2026 20:27:50 GMT
ENV PG_VERSION=17.9
# Wed, 15 Apr 2026 20:27:50 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Wed, 15 Apr 2026 20:27:50 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:31:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:31:00 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:31:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:31:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:31:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:31:00 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:31:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:31:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:31:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:31:01 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:31:01 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:31:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf183a66a538c40a8df864decf86704bcf2d338bb1b3505942a7533ee6b1170`  
		Last Modified: Wed, 15 Apr 2026 20:31:11 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56826359e47514629acd3db06bd37de4b1856edfb8416baa73724315c36a8cb`  
		Last Modified: Wed, 15 Apr 2026 20:31:11 GMT  
		Size: 887.1 KB (887110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9360c3a4bff3feddeda1d83c3487fc40e224d7b47e2c265ce9caefc20cc39d72`  
		Last Modified: Wed, 15 Apr 2026 20:31:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98db5cf7b1403ef4173e5e2a05a5f8fbc7d328adbd5799eabf31469afba04410`  
		Last Modified: Wed, 15 Apr 2026 20:31:13 GMT  
		Size: 86.0 MB (86010030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741fa1ba6bd2a212e72520b740f0998314bccaad438f90331ac85880c14c5935`  
		Last Modified: Wed, 15 Apr 2026 20:31:12 GMT  
		Size: 10.0 KB (9953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baab6c9446222aca55e129d0aa9c37e24b7cc2f5177a060da6c34190fce2b9c`  
		Last Modified: Wed, 15 Apr 2026 20:31:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c575e8bfddae854091b435339f52254211c906faab32fb938ef01bd0b38aa5c`  
		Last Modified: Wed, 15 Apr 2026 20:31:12 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6672595cb78d971dc0f8483675a2bf194926d3f7efcc67169f1c019a7063ce7a`  
		Last Modified: Wed, 15 Apr 2026 20:31:13 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b70c7d7baf3dcf0caebcd7cee4e65baf35f6644bd19a61557edfbce6933626`  
		Last Modified: Wed, 15 Apr 2026 20:31:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:2e23834cb66b80656c022f7fa2351dec9bd8d3e2e180c8527cda590aa3939a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 KB (41628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3159946df6c2f482fc5de5df03848567d096ad48c9e9fd5f64169a928ed328d9`

```dockerfile
```

-	Layers:
	-	`sha256:a830b495f3c301e566ef0e10b9506e9ac2f0b7e1eaddc9a838afdf72055ab62e`  
		Last Modified: Wed, 15 Apr 2026 20:31:11 GMT  
		Size: 41.6 KB (41628 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ec4492e81b7a6a2bc224e3a4d6760e59597db64ca1c8d2e9a20710a978e674b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85681849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c141f2bcbcfff144ae691a995c18a4bd033d1b2afb2bcf532434f6fb98dacd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:25:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:25:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:25:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:25:59 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:25:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:59 GMT
ENV PG_MAJOR=17
# Wed, 15 Apr 2026 20:25:59 GMT
ENV PG_VERSION=17.9
# Wed, 15 Apr 2026 20:25:59 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Wed, 15 Apr 2026 20:25:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:29:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:29:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:29:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:29:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:29:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:29:06 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:29:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:29:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:29:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:29:06 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:29:06 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:29:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a087f7c958a0ce33cf96ecbbe5a0eea01301a30389d46b6081657bb2a859c7b`  
		Last Modified: Wed, 15 Apr 2026 20:29:18 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13261cacaeb57d155f21931ce69b546e20124d8bf1a27e56eaea4072fde65e84`  
		Last Modified: Wed, 15 Apr 2026 20:29:18 GMT  
		Size: 887.1 KB (887105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7029178bd125ea29b1086b4458c9759ba7c811bb36da7f82f815112450c0ad0f`  
		Last Modified: Wed, 15 Apr 2026 20:29:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0699c675237fa0caba359af7c4589697ecd6cfbc98e6adc35a6b687fb781839`  
		Last Modified: Wed, 15 Apr 2026 20:29:20 GMT  
		Size: 81.5 MB (81494268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bfa706c5110a8ae1381a410b1968353ac0e9f9873d3c36c6d4c37a763d0429`  
		Last Modified: Wed, 15 Apr 2026 20:29:19 GMT  
		Size: 10.0 KB (9952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9922dc4b2af0631076f972c3c5f30257264b2f226efde916a17115d9826c9036`  
		Last Modified: Wed, 15 Apr 2026 20:29:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b319213f941f73ff5bfe4062308d4fbfb95063618b7a6f1d271af5a758d87679`  
		Last Modified: Wed, 15 Apr 2026 20:29:20 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25fa32c18248fce6e31a45757017eceaf7a02f248179f69e53912703ef98a5e`  
		Last Modified: Wed, 15 Apr 2026 20:29:20 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14aeb208ad5a5d4e1d0f2581af544e81a749e6cf34d666d9526b874481c50c`  
		Last Modified: Wed, 15 Apr 2026 20:29:21 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:3c7acb45c1ea2862bef71784c9a2d8582c3043ed5ffceda85a5ca68028af761e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1221406094aa5947a9e979031e299eac70b0a45781b69f3a4540d1e3c59fb8f7`

```dockerfile
```

-	Layers:
	-	`sha256:601eaddca904eabbfdbf4a2204813864d1904e6bad70c5d599eaaa2b060ec30a`  
		Last Modified: Wed, 15 Apr 2026 20:29:18 GMT  
		Size: 597.5 KB (597488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa5d7ccf1661ae505a4c35e628640240b387596659204629cee1bdf806eb59f4`  
		Last Modified: Wed, 15 Apr 2026 20:29:18 GMT  
		Size: 41.8 KB (41843 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9717f062a3e2a9d9d6830155a33faadf95dbaa0bc1e8eb1a6d3e9ed569a5a21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109279732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb288c51623c21d867f6bb176a3a30086c2d2360f954f42860acab1a4b7fcb22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:23:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:23:46 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:23:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:23:46 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:23:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:23:46 GMT
ENV PG_MAJOR=17
# Thu, 26 Feb 2026 19:23:46 GMT
ENV PG_VERSION=17.9
# Thu, 26 Feb 2026 19:23:46 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Thu, 26 Feb 2026 19:23:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:26:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:26:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:26:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:26:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:26:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:26:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:26:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:26:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:26:08 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:26:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:26:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f8c3d5a1d500bf1467f93627b2619293caeb6960f46981e372f73bc93b2ea4`  
		Last Modified: Thu, 26 Feb 2026 19:26:23 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a760e82798cca3c2bb73c6128fabc03399951781cd9be2c575d3a39ffe5dc549`  
		Last Modified: Thu, 26 Feb 2026 19:26:23 GMT  
		Size: 876.5 KB (876496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48affb7431d8551d25510f5c3c30cf7c62c0a104744898717306b1581217bf36`  
		Last Modified: Thu, 26 Feb 2026 19:26:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06537e9049879169ca26a07b185e4d2a924f9c755948ca56c28c05d2504ff5e`  
		Last Modified: Thu, 26 Feb 2026 19:26:26 GMT  
		Size: 104.2 MB (104188790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2537eec57c29169d9a2320e277beacfa2fefe91813f3c38a9c0f9e2d211a9a58`  
		Last Modified: Thu, 26 Feb 2026 19:26:24 GMT  
		Size: 9.9 KB (9950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460dad80a77aafd905e2903fd60516508f3bd95a0e7f1c9f0ce976925bf87047`  
		Last Modified: Thu, 26 Feb 2026 19:26:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf43d74529dcf20abe81993039ba32fe3f7d2de6bca4360b5463142e0ed4a814`  
		Last Modified: Thu, 26 Feb 2026 19:26:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ead8c734390e0ed2edd10db92f404ed4c292bfbe7564e39fa297108273001`  
		Last Modified: Thu, 26 Feb 2026 19:26:25 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d725b061fdd636920df6ee629951ae196794e1befede6da6b6b0b7c29cd51f`  
		Last Modified: Thu, 26 Feb 2026 19:26:26 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:004bcd1fd58bb657f80d8c19cfbe85a738a791dfff66488468f770f41be78553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.4 KB (639367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f3579746e9ec46937887dbdc86d4424e6f4c949c3339a476cc69255f3d5564`

```dockerfile
```

-	Layers:
	-	`sha256:e0381ee98b1f823a1657447cddefd57c57195568cc02b6402702d19ef8f7bc2d`  
		Last Modified: Thu, 26 Feb 2026 19:26:23 GMT  
		Size: 597.5 KB (597480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e490e37f1309a220d784e78d13ea12f40337322baf05ec35068757ce1e5d00`  
		Last Modified: Thu, 26 Feb 2026 19:26:23 GMT  
		Size: 41.9 KB (41887 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; 386

```console
$ docker pull postgres@sha256:c7ebcb5395a79f271f81a35778b31ed1ee3aac04c5c4c28cfc961913892f3d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117161533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f596aa82561e91a06546c13746f2835657a0a8774b1d91061380fbdbd3787e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:16:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:16:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:16:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:16:31 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:16:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:16:31 GMT
ENV PG_MAJOR=17
# Thu, 26 Feb 2026 19:16:31 GMT
ENV PG_VERSION=17.9
# Thu, 26 Feb 2026 19:16:31 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Thu, 26 Feb 2026 19:16:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:19:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:19:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:19:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:19:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:19:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:19:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:19:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:19:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:19:18 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:19:18 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:19:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020e26be1d0eab1bd1c78a0da436ae7877aaa5c299eb55cf5c3fa34bcca6b989`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd7161f4dd496350e8a1fac2d203e66ad2d8cc4b11b4a484bf9c69e1b64c32b`  
		Last Modified: Thu, 26 Feb 2026 19:19:33 GMT  
		Size: 893.3 KB (893256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df935d681190c6793e38fc37de8c84dc1dc6b2af5ab073fdf4077cd914a91efa`  
		Last Modified: Thu, 26 Feb 2026 19:19:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a15799d425430f4925745a70a8a1b1a21ea3ad70232b4b6f11a9423ce63e9c0`  
		Last Modified: Thu, 26 Feb 2026 19:19:35 GMT  
		Size: 112.6 MB (112563928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1de39a4f9670cc20479a9807475e6561847557d8cdbf9c1ffccb19170681c5`  
		Last Modified: Thu, 26 Feb 2026 19:19:33 GMT  
		Size: 9.9 KB (9950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07acebf764a62692369545797bd73d45c8a20c4f9d672b7815752b9253faaad`  
		Last Modified: Thu, 26 Feb 2026 19:19:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d61cf7622082c28696ebf7748243af176403c393b6caa2565031047946c72e`  
		Last Modified: Thu, 26 Feb 2026 19:19:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ccd6a961778ea3c013693e0f74a89f33311722e4def90762e22a20033de1de`  
		Last Modified: Thu, 26 Feb 2026 19:19:35 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787f791400e005a5bd7ba4905021b5ca7dd7a4ae7fbf3ff8cbbbaa10ad2a15d7`  
		Last Modified: Thu, 26 Feb 2026 19:19:35 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:90a2d7928efc7adfacbc5df26f93ec41759ff418c90c6ac286ca0dda6cd381a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199207c4e833a78e15d13004ed05fbe12547609bdde5fe105924ba797115f475`

```dockerfile
```

-	Layers:
	-	`sha256:0278277b26836b514597a410beba8ddfce5f46cad50e7aab82b99f1fed7d34c1`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 598.0 KB (598049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64973acc54ba503df2708dec241e18c006e0b9ac6b1765716d874ef4cf8dc220`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 41.6 KB (41632 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:689ab943ab18f620ebba601d8d56cbc897e337050f7da303117289f2d8d56022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96106424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea76a344ee9eb51a3e3c5e1ab8899851c0fe67bca2e8a9df1e24288efb3de64`
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
# Wed, 15 Apr 2026 20:55:24 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:55:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:55:25 GMT
ENV PG_MAJOR=17
# Wed, 15 Apr 2026 20:55:25 GMT
ENV PG_VERSION=17.9
# Wed, 15 Apr 2026 20:55:25 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Wed, 15 Apr 2026 20:55:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:59:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:59:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:59:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:59:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:59:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:59:57 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 21:00:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:00:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 21:00:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:00:01 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 21:00:01 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 21:00:01 GMT
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
	-	`sha256:9d747fa8cde9879dba2d8250f9f7e55532a9895dec0b8048c1694af198565ee9`  
		Last Modified: Wed, 15 Apr 2026 20:59:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e5cac5ba8cf96bf5caa44ccb35c786be7169f2a3b134b7ca2a26306e0b041`  
		Last Modified: Wed, 15 Apr 2026 21:00:33 GMT  
		Size: 91.4 MB (91377996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcde273e5fb4b659c99b3a9e604d08288f1be3ad04b19f10b4be076ca051f8e`  
		Last Modified: Wed, 15 Apr 2026 21:00:30 GMT  
		Size: 10.0 KB (9959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08863966a94133f8201da48275d87fa2748afc66841149078397c66a4d1e2261`  
		Last Modified: Wed, 15 Apr 2026 21:00:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e11cea795ae8c735099e346a098fe924d56f7b72e34586194eed6c79719995`  
		Last Modified: Wed, 15 Apr 2026 21:00:30 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3224355102c45e0ecfb872534e04699e7f2b255b7460ffe58cc4502f950c4f`  
		Last Modified: Wed, 15 Apr 2026 21:00:31 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f86254ed80b9f92d9110204db9b5caea03fa11bf324d2228dc14b5bb7049eb`  
		Last Modified: Wed, 15 Apr 2026 21:00:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:674bec7f6c70eb6e54c3d61320c9f54b88dc865b7407754fe2f60ae9ee92ad15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae34176d2d0255aad433992ec261fc034c612c58dbb1b65ad7fc8250cebb8f6`

```dockerfile
```

-	Layers:
	-	`sha256:55463e8dcb675f6523d8e36119b36d22ba7258add1fc7036e3380d9f29c18a7d`  
		Last Modified: Wed, 15 Apr 2026 21:00:30 GMT  
		Size: 595.8 KB (595823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1844a87b58d256f08b032861a8359076456130a38a506d3e9d512cb25519add1`  
		Last Modified: Wed, 15 Apr 2026 21:00:30 GMT  
		Size: 41.7 KB (41730 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:f85eefba1dec75e95652593ee8a1cd5cb6543a9bf8abeed10cb7a881a623d01a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112230618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34fe840398a547faaccebb5dafcf9e89aaf9e3b31d023526adad9b4da201a95`
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
# Thu, 12 Feb 2026 23:09:02 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 23:09:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 23:09:03 GMT
ENV PG_MAJOR=17
# Thu, 12 Feb 2026 23:09:03 GMT
ENV PG_VERSION=17.9
# Thu, 12 Feb 2026 23:09:03 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Thu, 12 Feb 2026 23:09:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 28 Feb 2026 07:22:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 28 Feb 2026 07:22:42 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 28 Feb 2026 07:22:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 28 Feb 2026 07:22:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 28 Feb 2026 07:22:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sat, 28 Feb 2026 07:22:43 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 28 Feb 2026 07:22:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 07:22:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 28 Feb 2026 07:22:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 07:22:44 GMT
STOPSIGNAL SIGINT
# Sat, 28 Feb 2026 07:22:44 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 28 Feb 2026 07:22:44 GMT
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
	-	`sha256:e8148b66fa8f993f7a3afc5dd362babe771ef176b9fd9d740a885b2f05b45d05`  
		Last Modified: Fri, 13 Feb 2026 00:02:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7807af8b9a2b43c68fc1c9b5ce64aa8ff8830ba7223787baded829053de94`  
		Last Modified: Sat, 28 Feb 2026 07:25:48 GMT  
		Size: 107.8 MB (107759013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d38d37ab7ae427ed7cb4494a407ef2c04acbac8c42a4bfc9742f5dab6585c`  
		Last Modified: Sat, 28 Feb 2026 07:25:32 GMT  
		Size: 10.0 KB (9960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753253286d787b28cbece79183713004ac277f76513815b8baddac625dbaf541`  
		Last Modified: Sat, 28 Feb 2026 07:25:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd2c0d2672c90644fb2a1ff40d1078205045675228a5bef7ee9f0d86d4e1e9`  
		Last Modified: Sat, 28 Feb 2026 07:25:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5245d34357325aa16ec1ec4e544181816322bb28ab46975675ba5889523524a8`  
		Last Modified: Sat, 28 Feb 2026 07:25:34 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6937b4c0a0a6c9aa30ee7f992685a7ad6d12b2490dac546d9578f84775e2ac`  
		Last Modified: Sat, 28 Feb 2026 07:25:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:e7aaca9820c3a68c8b33286d12e4b142c959b800e7bdf566feb3b24ced3c3d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 KB (639189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f31c99b05c0ac4f425126584f5d6d857139022e42c6799239b38f0f619094f`

```dockerfile
```

-	Layers:
	-	`sha256:96ceaad1420152ed14d2400f07b2085d70f18115ea137709328a05ed58c65cee`  
		Last Modified: Sat, 28 Feb 2026 07:25:32 GMT  
		Size: 597.5 KB (597453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46eaca0c52811c1e4dca46b9562d04be970327d5ae1efc2740070adc9338e533`  
		Last Modified: Sat, 28 Feb 2026 07:25:32 GMT  
		Size: 41.7 KB (41736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:422cd081fb3edb880d6aa260f3ee60ee9124276823608999ab8cbf5a79ce5283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119252972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f7e13b35db42c0de8d32852a1e41e0ddbc3f70a4e5840eed3551894a77e75c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:14:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:14:55 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:14:55 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:14:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:14:55 GMT
ENV PG_MAJOR=17
# Thu, 26 Feb 2026 19:14:55 GMT
ENV PG_VERSION=17.9
# Thu, 26 Feb 2026 19:14:55 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Thu, 26 Feb 2026 19:14:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:39:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:39:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:39:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:39:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:39:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:39:22 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:39:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:39:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:39:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:39:23 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:39:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:39:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6390f8026daaba6b4a0ba5ea908c8dc6349dd04610c8042fed5bdeb177e261`  
		Last Modified: Thu, 26 Feb 2026 19:19:15 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20d057a6a7a5332d1a6ec5069dcaee3c83e9a8d5596baf55423cd8546a0408d`  
		Last Modified: Thu, 26 Feb 2026 19:19:15 GMT  
		Size: 897.4 KB (897425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0418015b386c8239878390e0c3827343f0ddaf33bb01b5e22256d52b47998b9`  
		Last Modified: Thu, 26 Feb 2026 19:19:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321ad4161aaada3d10ac78bc8d0f15aac83776dfd78c9fe4d1b9dd443d43496`  
		Last Modified: Thu, 26 Feb 2026 19:39:59 GMT  
		Size: 114.6 MB (114612849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec38f73f1b5f7d0e0761f79832f13cbd827b79771de11548d386180367558b1`  
		Last Modified: Thu, 26 Feb 2026 19:39:56 GMT  
		Size: 10.0 KB (9952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0106cf2fd5d681e2d2008469ce32da38d5b7fea310581a4ed7b96ed7ca5eebe9`  
		Last Modified: Thu, 26 Feb 2026 19:39:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855ea8722ac3d3499f0e5c69f0159b05c790192fc5816f29b4aee2c56383e3e`  
		Last Modified: Thu, 26 Feb 2026 19:39:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cbed5737196cb366523fd421f3b89643005d6a454fc4168e56fe24161b686f`  
		Last Modified: Thu, 26 Feb 2026 19:39:57 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f64ca076ee38717aaac1fed9e5e9e40306be61e5946cf3c9a29bbfa291b4569`  
		Last Modified: Thu, 26 Feb 2026 19:39:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:52c1df2f58a48d1e2ec6df3bc3e7262c5c46f7cd1d6adcc9d288da97e3f5e68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.1 KB (639100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a2a10d6b9d60f20a478d83661603f60f81eba411f4ebfd6f790ac81e541f59`

```dockerfile
```

-	Layers:
	-	`sha256:d045cc8701b1236a1166097357c3055e45ac2f092b44d290bf6f2253c79425b1`  
		Last Modified: Thu, 26 Feb 2026 19:39:56 GMT  
		Size: 597.4 KB (597423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5c059d5a8d38a71f1cadb85b3b64e41ffbcaf14319e00e99ecf6fed8498f4c7`  
		Last Modified: Thu, 26 Feb 2026 19:39:56 GMT  
		Size: 41.7 KB (41677 bytes)  
		MIME: application/vnd.in-toto+json
