## `postgres:alpine3.19`

```console
$ docker pull postgres@sha256:631e07c2d162da0b59144d47cd12d8c6714a80fe3d9094aaf1b6e7adf22217c3
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

### `postgres:alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:a2a77ae7d7ecf5e01d4a21b943933862228c715e7cd81719271c95255f5cc5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98123713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4a8e182e3c8847ec3164b7ee8669db2ee226987a6c74e01dca9b1dcec0637a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_SHA256=7e276131c0fdd6b62588dbad9b3bb24b8c3498d5009328dba59af16e819109de
# Thu, 26 Sep 2024 18:19:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173b120eb10784a680081f1628ee88e8d60d6ab26f19bd89cfb885e2ee44891c`  
		Last Modified: Fri, 27 Sep 2024 00:03:12 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0462d5f7a3be7765c44145402933009363e548103ee34a9081202070e6a3dd6b`  
		Last Modified: Fri, 27 Sep 2024 00:03:12 GMT  
		Size: 1.1 MB (1120286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c37e7ce57ce8c68eb37b81efd72d544120ec0033b029a642c03c94e2b7793bd`  
		Last Modified: Fri, 27 Sep 2024 00:03:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbdb8a5582a14db24056470fd01a55f82bc2d59af7aced584bec2f310a9833a`  
		Last Modified: Fri, 27 Sep 2024 00:03:13 GMT  
		Size: 93.6 MB (93566559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1f604fbfe74f7292f2184629d4de142c1b06444d1c741b64ecb27594eb014b`  
		Last Modified: Fri, 27 Sep 2024 00:03:12 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cf19323232d46b3cbb73b3d72d5bcb2d3893dd9a0559064da824ad25ef9677`  
		Last Modified: Fri, 27 Sep 2024 00:03:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2054c9f266983342051e9980b2cc0b9d38d2751755d6cb88025f8ea59b3f805`  
		Last Modified: Fri, 27 Sep 2024 00:03:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd5e6646936ad3f06360f96043ff481baa6e9f2da18cb5b93aff3e13e7d8799`  
		Last Modified: Fri, 27 Sep 2024 00:03:13 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850dd96f5ab994b5af32a717a6f923ad8b9a90c7f8782cbf938dd140c9c57311`  
		Last Modified: Fri, 27 Sep 2024 00:03:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:37a0bb0bc4cdbb93f552bf2342a63acd1409abc385897d8f79092bc34c2bff18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1011703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2176aec81a6f137c66ecc53d129c939ad2e9a057ea77eca5f3a2dc844324d33d`

```dockerfile
```

-	Layers:
	-	`sha256:729efaf9c68571ee5a04bf5b6644f7336e8f9f5ede3e884a77d68ce1c395cd11`  
		Last Modified: Fri, 27 Sep 2024 00:03:12 GMT  
		Size: 969.0 KB (969004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c08830ee9c27bf8ab19cd7c903846bb48c9a157a55b07d2c84db2fccae035c6`  
		Last Modified: Fri, 27 Sep 2024 00:03:12 GMT  
		Size: 42.7 KB (42699 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:ecfd7675b431ea4eeb320a8dd0b8167c7ae58d3778fc6d872980546626c5e3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96768219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9182edb710e4bca6b48575fc20ebaaeb3de4392ac7fc5ef22c57ef63a6a20ccd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:26 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Fri, 06 Sep 2024 22:49:27 GMT
CMD ["/bin/sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_SHA256=7e276131c0fdd6b62588dbad9b3bb24b8c3498d5009328dba59af16e819109de
# Thu, 26 Sep 2024 18:19:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d826e605346ac703fd4bb49c66f0da21ade0330bd6f0365a01ffacb9e9b5bd`  
		Last Modified: Sat, 07 Sep 2024 08:48:26 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65abd2f8c8203e91dbd2e59181770a8eee351135174c82c7167d10017bd7f7c6`  
		Last Modified: Sat, 07 Sep 2024 08:48:27 GMT  
		Size: 1.1 MB (1086689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40167ca09e520a497007dcfa6eb16e9b748aadaf5604c9068b72b2c41196b05c`  
		Last Modified: Sat, 07 Sep 2024 08:48:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6890e44469c3e0a5e2b4bf8283e4d5ffecc64bc6f7f09906b27a4eb844572cfd`  
		Last Modified: Fri, 27 Sep 2024 00:54:21 GMT  
		Size: 92.5 MB (92487970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ffa92311aac305191e4595a1fff1b4f62d8683873adc8272d948f48a1e2f28`  
		Last Modified: Fri, 27 Sep 2024 00:54:18 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbffd0b4a1761325e091e5c80f9611b98cb9c9d5e935151423b7cffb14328ee`  
		Last Modified: Fri, 27 Sep 2024 00:54:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372def620b19548440d38a96446dbce5b1bdfdf46b65db7a249966f6f79cbd72`  
		Last Modified: Fri, 27 Sep 2024 00:54:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9092125fef70cb86d078cf40fe48bc826a9670412f6ffd316c3f4d774969d26`  
		Last Modified: Fri, 27 Sep 2024 00:54:19 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910465e0d35910ecf8a61ae7cc7c8f3407a8da60cb7dcde775e6a7369a14502e`  
		Last Modified: Fri, 27 Sep 2024 00:54:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:75384367d1f3d6f43bd5e7bcbb9e370b5a002556abb148369b0df6593b4b490d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 KB (42633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471385f660dc6e02da779bb907e2a7bc343f9d29c7ec539319f887f7baf32d57`

```dockerfile
```

-	Layers:
	-	`sha256:23725a19ccc880c470d4ff081968371df74dd585012d8d27aac040333c7e1539`  
		Last Modified: Fri, 27 Sep 2024 00:54:18 GMT  
		Size: 42.6 KB (42633 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:4a974fe6dbf41cdc24f14b1409da901c04bceeeefe391a190e222110f58c6698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89972060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b99092bd8dbdc670ea7705cabb45967738000e76ca14fcd0ad3ffdd62fc1e75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_SHA256=971766d645aa73e93b9ef4e3be44201b4f45b5477095b049125403f9f3386d6f
# Thu, 08 Aug 2024 17:20:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7301be67e4738b26ff038817b98ba1651b096b6f4c8282ec263badac035e791`  
		Last Modified: Sat, 07 Sep 2024 09:11:15 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f6bf8db32a8805b9bb6360898111fe2af1e0d20467f3823409618a0fc832e6`  
		Last Modified: Sat, 07 Sep 2024 09:11:16 GMT  
		Size: 1.1 MB (1086692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72950ff2803c09d980a0d9157258772394aaa758b7557547ca81523be397360a`  
		Last Modified: Sat, 07 Sep 2024 09:19:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1088c5228e0298817dc05644651492611a9414d6a2ea9a6d8904acf1fb5b03f`  
		Last Modified: Sat, 07 Sep 2024 09:19:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a075c503a3670a338eaf26e4ea7a7cf649d77d53645114d277e3a4a064caf243`  
		Last Modified: Sat, 07 Sep 2024 09:19:05 GMT  
		Size: 85.9 MB (85940688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cc16ea807b0be3ca4767bdadeeea742e1fd8920c9bfd7376c717650a464c68`  
		Last Modified: Sat, 07 Sep 2024 09:19:02 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a45a1f541395e40985fdbac10f4cb9d314665a0b7e190a00c640e6e12fe11b`  
		Last Modified: Sat, 07 Sep 2024 09:19:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f580d311ad99a454e14e9304975a66a66eeaf5a6a889fff70e95760d9a283fc7`  
		Last Modified: Sat, 07 Sep 2024 09:19:02 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32de9abfa8d7d18c80a8b036a186f7e7c1b51d84879f2d5efd0c880189299163`  
		Last Modified: Sat, 07 Sep 2024 09:19:03 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c97670d86a661d2fac1782517004eee9cbbc82938201e432671e5f71b4c7f2`  
		Last Modified: Sat, 07 Sep 2024 09:19:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:b02695057020fede0b945756f83921fad98f00cb5cb4c8c83c2047bf21e73c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adb6692d65584a52c41d0658e9a70c251fdad6ccc50053027bd91dcf73b3acf`

```dockerfile
```

-	Layers:
	-	`sha256:7c7d3da87a67a8cd239f1f1b9b63d9889bd0d54f73305b777f093ea7580d0290`  
		Last Modified: Sat, 07 Sep 2024 09:19:02 GMT  
		Size: 969.0 KB (969019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1723a9e00817cb9e013c032df8c1df13baf7b0da4ea51119fb8e54fcc8f5de20`  
		Last Modified: Sat, 07 Sep 2024 09:19:01 GMT  
		Size: 45.5 KB (45492 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:255b93b394ea3e753c33293a474966a85aab64859d60db1e11fc515a54ccfed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95531222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca573c4243b589b1305d70dde63077dd6b5815ffb1fab42f433c904fe03bd74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_SHA256=971766d645aa73e93b9ef4e3be44201b4f45b5477095b049125403f9f3386d6f
# Thu, 08 Aug 2024 17:20:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896d03877eb37d824efa1dcb1e0aa39cdef05d3080317292a8ddd2075f6fb7a3`  
		Last Modified: Sat, 07 Sep 2024 08:46:55 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb628377f51a21b951e4859e56c887983ad44edd0c0d40e10a1a4781b8f6ce7`  
		Last Modified: Sat, 07 Sep 2024 08:46:56 GMT  
		Size: 1.0 MB (1049350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138c337c1b814ed3a686b00f46337a82058005613f3830004d8b616bf97002d2`  
		Last Modified: Sat, 07 Sep 2024 08:52:44 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ee9476909b17036c9f0204a4a3948592cdb06576f49909f160800cf7173fa8`  
		Last Modified: Sat, 07 Sep 2024 08:52:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36354c7092a9af5c37fe4d17f2581f08ec6c674ffcc24edb55afae3c1f6c8343`  
		Last Modified: Sat, 07 Sep 2024 08:52:47 GMT  
		Size: 91.1 MB (91105748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add3494e93f69a892114df4d3bcdde8c568729a0e5b6dd593475f0ca02a6c375`  
		Last Modified: Sat, 07 Sep 2024 08:52:45 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63512dd1c99156916af280695ced410574b1b7c49ecdbe6e359f92db8271841e`  
		Last Modified: Sat, 07 Sep 2024 08:52:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4766032eebf757b29419d6139d060b44be847dcf13a1134cce3a13cd79352007`  
		Last Modified: Sat, 07 Sep 2024 08:52:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e4aa4ca76ff02638641de181ab7913255306f22356cd8fd4cc5608fac60881`  
		Last Modified: Sat, 07 Sep 2024 08:52:46 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac828aff31731f4583af1d8f231d38ec41de6919e8283770d5396050ac92d21f`  
		Last Modified: Sat, 07 Sep 2024 08:52:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:1af0d79c8b18ee94b9840e2ac9b06054b2fba91452f822312a86e7abb9ddbc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e226ce315511ac892daedb42fb39e3754437f28da260a4f1965c292ada8dcd`

```dockerfile
```

-	Layers:
	-	`sha256:c3d07c0588775f53b26dc55c57d1aa4b829e0b4767eb26fdc2991cbf801ae618`  
		Last Modified: Sat, 07 Sep 2024 08:52:44 GMT  
		Size: 969.0 KB (969035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8bb48e4e253dc4b26b7580070c441e6ed36859af004ef9a3d7234479d7258a1`  
		Last Modified: Sat, 07 Sep 2024 08:52:44 GMT  
		Size: 45.6 KB (45614 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:809d5da047e8cc5786fd5fdbcdd70203ff63ab87942a374ce281dfcc1b92a2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103421789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d2002919e655f3bf3e6008abd6955c1868899324761979fd22ac8bfbb6681e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_SHA256=7e276131c0fdd6b62588dbad9b3bb24b8c3498d5009328dba59af16e819109de
# Thu, 26 Sep 2024 18:19:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e3d6b31bc58ef938567c477e72a08ee1791b45585d8489f2257ae36242a4f2`  
		Last Modified: Fri, 27 Sep 2024 00:03:45 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6368d8f629b1454ecf172633d8079659199484be8d81bf743fd7154e6491a3`  
		Last Modified: Fri, 27 Sep 2024 00:03:46 GMT  
		Size: 1.1 MB (1095466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697bbf05caecc74a3659cd5e2d6f325e6dc9f360a8815e0aebfc58bcf5aaab5f`  
		Last Modified: Fri, 27 Sep 2024 00:03:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6405d05399e9272989619509c44fba17671dc98c93d997ab2096f34027c6026`  
		Last Modified: Fri, 27 Sep 2024 00:03:48 GMT  
		Size: 99.1 MB (99055547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9514ac90b97032fdf3ff52f742fccbbe1cca24e31508ea5c8ac560f6029321`  
		Last Modified: Fri, 27 Sep 2024 00:03:46 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec1b177bee4753fc9b7119fbf6b048ef7563a9f6e8b00bf00485f78c09a0e7f`  
		Last Modified: Fri, 27 Sep 2024 00:03:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213be7f15fa723440323543727ea2e5924bd68bc14a2fb2b916e48c77f2453d1`  
		Last Modified: Fri, 27 Sep 2024 00:03:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30262fa8bb6884216a8f9ed5aa7737d3a4c98b00ce6e32f82ca95d0f921209fa`  
		Last Modified: Fri, 27 Sep 2024 00:03:47 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0d546d9b115c0213f964589a50e9e14faea7e1bf9eacdc4d9367f900350f36`  
		Last Modified: Fri, 27 Sep 2024 00:03:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:ceb9e50d6480d6662398a602e42fdb0bd7b2f90dbba29539a5c4a35f9b418663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1011645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c977141a474cb8b0d8b2839ddebf507f920fd37053f26ffb150eca658c4206e3`

```dockerfile
```

-	Layers:
	-	`sha256:3f60ea1a3b3061a254029a5abc92f806d851ab99f8be457b9961db29e33f9fd9`  
		Last Modified: Fri, 27 Sep 2024 00:03:46 GMT  
		Size: 969.0 KB (968984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a108a9db0d80ba8f4e80ddc1dcd4696766661598ea532c5971643be915da48a5`  
		Last Modified: Fri, 27 Sep 2024 00:03:45 GMT  
		Size: 42.7 KB (42661 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:fa5260471413e92ababb3b05c13b62cfaec4c433ba25a38204513795b6893ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101421836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece799fe360ca87503edecdb4ee4d7df6cf76ef8c77dfbd399a88d953ffdc06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_SHA256=971766d645aa73e93b9ef4e3be44201b4f45b5477095b049125403f9f3386d6f
# Thu, 08 Aug 2024 17:20:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02f5f490f95d2b3fc6f063070a7454d2c3bc3e3fbf1a39ccb5cfb232b5c54a7`  
		Last Modified: Sat, 07 Sep 2024 08:15:21 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e90f8e25b6668b7d290e0dd4df1451615699705988c9e87c111e2645e26782`  
		Last Modified: Sat, 07 Sep 2024 08:15:22 GMT  
		Size: 1.0 MB (1039691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4a0a51ded59db453720882af890f5bb722fc37928b2b97111f18505a4661e8`  
		Last Modified: Sat, 07 Sep 2024 08:21:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75429841b4db99e5f30a35ee5083deaf37dfa7e4285d027981721fb02a01faf`  
		Last Modified: Sat, 07 Sep 2024 08:21:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a9eb4f27342ac05c0654e8343dac6b81f754bfb85d105901f0eebe3e41d83f`  
		Last Modified: Sat, 07 Sep 2024 08:21:27 GMT  
		Size: 97.0 MB (97000656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e998e9831448b5357acac1dec5efe177446851bee68f410e69760a5ef95a0a3f`  
		Last Modified: Sat, 07 Sep 2024 08:21:24 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbc85d9f9137d15821df3a0f37c07cf736675fcf9f82bac2765616abce74d1b`  
		Last Modified: Sat, 07 Sep 2024 08:21:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f87ca076ac3ad29f08179044d33e14a05bcc157afddc95c4864d7f1fc4d847b`  
		Last Modified: Sat, 07 Sep 2024 08:21:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed3d1e8dad2c0977ec0b884858a7c2b6a7cc81ea00e6afd2a68566d5ee69ed9`  
		Last Modified: Sat, 07 Sep 2024 08:21:25 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21df147fac42747380202e5690f8b41c24e637a2cf1c89d5fd9530e7ea455fd3`  
		Last Modified: Sat, 07 Sep 2024 08:21:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:71af51d0d60724daaba1e69e306f327fef26c31a634c02cd94e3b7781697253a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ae496633081c583371d0bda06ecb49bbe864bdca479e59da4d87d5793c1a77`

```dockerfile
```

-	Layers:
	-	`sha256:304edd203978dd35aed92252367947ca90d846b09b0bdff950afb1a9fde2342e`  
		Last Modified: Sat, 07 Sep 2024 08:21:24 GMT  
		Size: 965.4 KB (965401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151d1cba0f9b7fdba53c5d2e714b7a23d8b89f25c925f8141e43506df66ab788`  
		Last Modified: Sat, 07 Sep 2024 08:21:23 GMT  
		Size: 45.4 KB (45374 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:2ddc35aee06d41eb7820ca380382dd544954d9dda959f5b5f4c496c9264200dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105727685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b446c66a77d877026bcb8d5e3689aae6726583dcd9ccad312804a05367311e99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_SHA256=971766d645aa73e93b9ef4e3be44201b4f45b5477095b049125403f9f3386d6f
# Thu, 08 Aug 2024 17:20:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b332d47914fd31ead4a60b0094c348297bc38ef29f5b3eb692132ff8910b0e9a`  
		Last Modified: Sat, 07 Sep 2024 07:33:17 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a0768a2d48558dddbc4835820dc9de94b42c05a140368d161f5ac6a9ae6d49`  
		Last Modified: Sat, 07 Sep 2024 07:33:17 GMT  
		Size: 1.1 MB (1083902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b507d79abae4f8b27322cda698439b6f39b8ed53ee2009a5cc6968687d6fde43`  
		Last Modified: Sat, 07 Sep 2024 07:40:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506e95536d7336d2e022a806d1310871e88ac9ac976020de86d74b66d7dae547`  
		Last Modified: Sat, 07 Sep 2024 07:40:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8d3cff27da4413c44dc37dc22fade27c5cd24da049f759188c0c84d71928d2`  
		Last Modified: Sat, 07 Sep 2024 07:40:57 GMT  
		Size: 101.4 MB (101373406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2631e709b0fce2ad259a58536faba1a4a6851f686fa9c3b8dd8b78f3ec607832`  
		Last Modified: Sat, 07 Sep 2024 07:40:55 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc00ab8101172df5457abacacfb7eec200db9b991c4cb628f75c37c760ac83b6`  
		Last Modified: Sat, 07 Sep 2024 07:40:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2200e1e69b18d5f95d4f28d1fa239279f4502532a3d8eb89ad9a6d0e71a767ae`  
		Last Modified: Sat, 07 Sep 2024 07:40:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d056ed9b5d063c5197ea8ee1b7e5599a5ad79ec2967ba24671abb7fd45cd2f5`  
		Last Modified: Sat, 07 Sep 2024 07:40:56 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2862e0288a804830590396666b770a45870ff8efc3dcdbcaadcf9316b40e93`  
		Last Modified: Sat, 07 Sep 2024 07:40:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:e334801aa32a538e524aad375fa9d511b0d49d8c720e9d119823288acd45a5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340a2f9315a35998e3c4a422ae4c983154373fbafe2f44a779b32266ad6b0a5`

```dockerfile
```

-	Layers:
	-	`sha256:13e35b0099cb0dc5b2eee3d7f8c9949683fbb44ca7bd4acab74fdac1422d5c99`  
		Last Modified: Sat, 07 Sep 2024 07:40:55 GMT  
		Size: 967.0 KB (967037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b5245c61c0baa2a484e07c7fbc3c0febc54a00a3a4d1b395f24d5c94cc4b20`  
		Last Modified: Sat, 07 Sep 2024 07:40:55 GMT  
		Size: 45.3 KB (45332 bytes)  
		MIME: application/vnd.in-toto+json
