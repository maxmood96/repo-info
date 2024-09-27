## `postgres:17-alpine3.19`

```console
$ docker pull postgres@sha256:514b9f1c489fdb7a0343557005e8e07cb7d7d96053090c8d2d8fc02cd5d94c82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `postgres:17-alpine3.19` - linux; amd64

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

### `postgres:17-alpine3.19` - unknown; unknown

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

### `postgres:17-alpine3.19` - linux; arm variant v6

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

### `postgres:17-alpine3.19` - unknown; unknown

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

### `postgres:17-alpine3.19` - linux; 386

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

### `postgres:17-alpine3.19` - unknown; unknown

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
