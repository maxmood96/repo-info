## `postgres:15-alpine3.21`

```console
$ docker pull postgres@sha256:fa8c247245b17a10547baa187a3171b9595a1d4604082a1970ab48ceaeb626b4
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

### `postgres:15-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:6b31e79c2f9dec041bf0a03a3f3b1fd5498938fc906ea11c65966de0581d6309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108863989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b3bc4c0da6ddf1a044a191ada2f129364c4b069758518805cf68c91adc8b65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b4248a42e70be780b438777da3596f98f51474740f7ebf88f85db70859e885`  
		Last Modified: Thu, 14 Aug 2025 18:23:55 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc33c94d5f108dc2897bbf4366227b987f0f80c8a5462b37eeba03f8582f0a`  
		Last Modified: Thu, 14 Aug 2025 18:23:55 GMT  
		Size: 1.1 MB (1115516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239958ea930cd4e98900f63a9cb57fda86247680fdec0266b67832181c6e3bda`  
		Last Modified: Thu, 14 Aug 2025 18:23:55 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d06278a74e784447b91ba54bb559936fbecd4d70a4d693414b139fb3ca0469`  
		Last Modified: Thu, 14 Aug 2025 18:23:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420725a87de6a89287fcff320af163609e38a0e7978401fc2318940d590ca83`  
		Last Modified: Thu, 14 Aug 2025 18:24:13 GMT  
		Size: 104.1 MB (104093780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cfb2a9933bb2ff2aed7d3578745dfdeed12ae401e159f648422fc2ee0acde7`  
		Last Modified: Thu, 14 Aug 2025 18:23:56 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29ccb131e738fa71f58a3abb23b60a674e694a9a1209425af87ae64b2aaf5dd`  
		Last Modified: Thu, 14 Aug 2025 18:23:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133fcc54859d7cb39195f37f935e9adb08a90610d2076086369f7004b4a802ac`  
		Last Modified: Thu, 14 Aug 2025 18:23:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff663e5558b7b68d504ecc3c6b19dfac5385e6c858bff9c701fea2889448734`  
		Last Modified: Thu, 14 Aug 2025 18:23:56 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc97b46e6d1fd6d45f99babe7bc1c0b994c86caf81b68522a6991359e13c29b`  
		Last Modified: Thu, 14 Aug 2025 18:23:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:ac691d6183ee848102f37f471134f0bfd2d645d167267ac7e482af68420a5b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9dbdda7103cef9ac0a2b96411b81e05035dec616a23c8214670184094a71af`

```dockerfile
```

-	Layers:
	-	`sha256:6c7f8f4b45054874e224a3f5c635a27f159109a647fe7d4c6bf0f7026d4108a5`  
		Last Modified: Thu, 14 Aug 2025 20:11:34 GMT  
		Size: 598.7 KB (598696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db7e804e241f6b934d8eccb1459e708e7d3fb67802254a6a3ae57f09e8cbeac1`  
		Last Modified: Thu, 14 Aug 2025 20:11:35 GMT  
		Size: 43.8 KB (43752 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:b55bceb9a930818dccb8ebb9d8a63ed5dec24e6e0fa482db7096e6e0c8e50b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88485689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6ff3eeb5f582a17f7a04ea3129eb0d557f5178e3cfc190f3b77ff94933dfb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c24d3e045a6ae3a2737e134a0660bb67966f1c4c59f473117ca5bfb7f462df`  
		Last Modified: Tue, 15 Jul 2025 22:03:20 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85a4c1614afc683eca7c5ab777456f2ae53dd7e1347e7e75764a6a74abf3b8b`  
		Last Modified: Tue, 15 Jul 2025 22:03:21 GMT  
		Size: 1.1 MB (1083487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0535ca87f130f01bd91aa140a599a3b6ee5d8f43b88e249c7c036a020c97a1`  
		Last Modified: Tue, 15 Jul 2025 22:20:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a590464760964dee563efddc9e8fba7d79df0dc36493bcf3cf136c63fbf94eca`  
		Last Modified: Tue, 15 Jul 2025 22:20:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029ef2e13137cf4a243830a106fc824b127b43111e2818ca1bc8e63f2bcf1aca`  
		Last Modified: Thu, 14 Aug 2025 18:50:56 GMT  
		Size: 84.0 MB (84021276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee963ec9065505ebef1e3298fd59ab6c8c13ce526fc687ee0cdbc58c1db7e3c8`  
		Last Modified: Thu, 14 Aug 2025 18:50:31 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d608a40d1617f142cb4c8e342bb69b5e3835586dd4515fdad384798cfbd574c2`  
		Last Modified: Thu, 14 Aug 2025 18:50:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bbd1208c71ab7b588feaf073b3f8034c4a44d61b04378f93975d958ee0ecb1`  
		Last Modified: Thu, 14 Aug 2025 18:50:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4b701a38313fd246074a371e9872a3b402fbb99b7b445bfd0a84feb7f42bbd`  
		Last Modified: Thu, 14 Aug 2025 18:50:31 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609985c8834afe2b9adafe867ecd4c149aa0a71f0d9c74eb9b9585f52bf5dc08`  
		Last Modified: Thu, 14 Aug 2025 18:50:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:e9e461336e934247ab172e5f3d49a56d2c605844c6683ef48d76169275421338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2ac6d1f1c4968935bf22797b9fd3a89f1db3b026f77ff7f7dfb28e82192f2d`

```dockerfile
```

-	Layers:
	-	`sha256:74f4ff1a30aaa7778d4a7f569109868ef3588dd2a94eaf53f7975a611a011e25`  
		Last Modified: Thu, 14 Aug 2025 20:11:38 GMT  
		Size: 43.7 KB (43695 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1a40037d9c6f1968dda78d27ee8de0aaa937769d55b5357634e05b3ab8c0aa62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83719415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174fadc83152aad854a3f597d4457dc7d633a44ae112f0187e175ed73e42d91b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2479436e58684e2eb112538b475b64df7a6f0cf622c2aca2d7639797003ee3b6`  
		Last Modified: Thu, 14 Aug 2025 18:55:36 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d6ea01dc2439d65ad9dee1318259d41e82100215755413d0040108baa9fa0`  
		Last Modified: Thu, 14 Aug 2025 18:55:36 GMT  
		Size: 1.1 MB (1083499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5e8ca01571f801604a91a356f4a79638d1a6336c1672944782dc73c9e1cc7d`  
		Last Modified: Thu, 14 Aug 2025 20:13:52 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8677a97a22961f3ee93622613e813b0d0803417ad6f01209358ebc161f892760`  
		Last Modified: Thu, 14 Aug 2025 20:13:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dde40a36b74910a6d4eab45135e109b01404ab8ed2f3e07b5ed56f8db596d2`  
		Last Modified: Thu, 14 Aug 2025 20:35:16 GMT  
		Size: 79.5 MB (79521919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1246145b832579a2fcb92f9049b0b8703b4bad46539098afb030fed5b0227a4`  
		Last Modified: Thu, 14 Aug 2025 20:35:06 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2f03217f8814bbf62c8499fd3eca8c2bf53e1ec5bc3accee5cba4651427665`  
		Last Modified: Thu, 14 Aug 2025 20:35:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf1dd1cc9bba7a1cdad3b8f45a5a108d3ede4d3213c127047c6877622d9b10f`  
		Last Modified: Thu, 14 Aug 2025 20:35:06 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ce8412ecd2e0f89923fabe2053149903a97865a4a93abb671c4f1abfb1e666`  
		Last Modified: Thu, 14 Aug 2025 20:35:06 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586f552b258adbaca6717458e05034f4707571f8b7132a2424e11600066407b3`  
		Last Modified: Thu, 14 Aug 2025 20:35:06 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:fae051a0179fb7f0c5a38e812cff0b0b9681496e4c575ee3a6a94227abf1ffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.6 KB (642626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c51ad3d7314c9f64c56f6c72153570e69755b4e116a56f56d228a95e820c2a`

```dockerfile
```

-	Layers:
	-	`sha256:d05a6299b9a5b4a603210bd2e877075e42fd89d79b68e0f729a6296cada5a77c`  
		Last Modified: Thu, 14 Aug 2025 23:10:35 GMT  
		Size: 598.7 KB (598716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25226aa01ce53f61583b4915ee2a4911462e37c8d758a8653663b021f02aa144`  
		Last Modified: Thu, 14 Aug 2025 23:10:35 GMT  
		Size: 43.9 KB (43910 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:1912828ec516eaa70f9e7e9cc2e1360afdc53f7a0ed53bc41b5e1dbd64c5e467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104748913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd620cc875d562de4c1ad9ee88351e320da424f113c72ac8415844b20dd5c82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0500e99ece82743454c50a08c0096387587592b762bcd82bde615671de2024a9`  
		Last Modified: Thu, 14 Aug 2025 18:57:34 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e8c3ce0b2d4fdb59659874d9a5099fdfb9996a16960ffb02ad370697f0ff35`  
		Last Modified: Thu, 14 Aug 2025 18:57:34 GMT  
		Size: 1.0 MB (1042486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1955b6a04ed68235e0d981512a3832f5113738d70fa2ed45a1b135161226e7b0`  
		Last Modified: Thu, 14 Aug 2025 19:12:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ef4a1f173221a39b19f0de13e787160a010a523f5c3222607bce9aa06a3bc4`  
		Last Modified: Thu, 14 Aug 2025 19:12:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fcfc2cbed3f78fa888e1dde088eb222863264ac321a66cb06f20ca62d02131`  
		Last Modified: Thu, 14 Aug 2025 19:20:25 GMT  
		Size: 99.7 MB (99702371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882873a2582a534cdf7157c217f5d81d46f92ed42269c9f9104f779f310de272`  
		Last Modified: Thu, 14 Aug 2025 19:20:07 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da869d3ec3b459e6d8b141c1c19eb536fdc11f1d9ea517b24a6fea3b872d2d3`  
		Last Modified: Thu, 14 Aug 2025 19:20:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a3dbe06dfda1f06100e1b3c6326ed928f623c86ee149f60438ecc3527562c7`  
		Last Modified: Thu, 14 Aug 2025 19:20:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d298c3c92d7e8667bd4294c0707c107c349f10c888859253f936751e50d9afb`  
		Last Modified: Thu, 14 Aug 2025 19:20:12 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5752be0ebbdc69e8ed558f1bba429693f18afc05a3b81f0d77380f51d6e02d`  
		Last Modified: Thu, 14 Aug 2025 19:20:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:f0b69cbc0a1bbdd3186282e4c10f8a9d752b3d71cf9330f188cc79059037036f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.7 KB (642672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b303648d21d086f72d51a9403da4401808f672afe44f5c6c64a0ecfcd12098`

```dockerfile
```

-	Layers:
	-	`sha256:b44be87e2f22b0761ae3cbc7c763e5b58645776bbc245198926856c5e1567dc2`  
		Last Modified: Thu, 14 Aug 2025 20:11:44 GMT  
		Size: 598.7 KB (598728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3a22298a39f57ea5fd60fa65dc31463d2ec0a68ca2ea8aa59997d740c21f759`  
		Last Modified: Thu, 14 Aug 2025 20:11:45 GMT  
		Size: 43.9 KB (43944 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:35d28e3f8db6e51e0a849b06d1503fd5d73284c6dbd3f614ecc762f420cd1a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115023037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a8daf57a3050029d8b903bb5ddd1c790043e250b4891154243601f33737e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0263d825f6960bc4a5950078a41848478c358b645db723db8b9dec47aa3a5a0`  
		Last Modified: Thu, 14 Aug 2025 21:06:08 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916005bf4d536518bebadac6ef154d4085262cd4074dd154c13b7cf528582a35`  
		Last Modified: Thu, 14 Aug 2025 21:06:08 GMT  
		Size: 1.1 MB (1091468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5ea76953ca4e458034a3ad07b89006c1e4a7e88cb845570e78e6b370d80800`  
		Last Modified: Thu, 14 Aug 2025 21:06:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cebe4310d9407fd8b5c798c9a1ed407ddc41928ae8a4285a55036a65975a68`  
		Last Modified: Thu, 14 Aug 2025 20:34:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c769a96d4a92b23754578f48497dff09e010c3cd545e291cf272b12716efc74a`  
		Last Modified: Thu, 14 Aug 2025 21:06:13 GMT  
		Size: 110.5 MB (110453731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67673b5e0bc08e962130b647b12e5bf5019eb8fc4946c4920c5107f2b775b9a`  
		Last Modified: Thu, 14 Aug 2025 21:06:09 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89958fe50c45b8f744a87a420689edce9e9f18dd0d5db58d5f7c5febcd16adee`  
		Last Modified: Thu, 14 Aug 2025 21:06:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8e5f4e20467ce4d7d796a2cd573c1ac96acfbb5ad345490ef9a28640663180`  
		Last Modified: Thu, 14 Aug 2025 21:06:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec85b9fb063c0d851c8ccb7629546a15a88359bbc92dc0d4d649d4d144a6ae90`  
		Last Modified: Thu, 14 Aug 2025 21:06:10 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf8e7755aa09e24dadd4ed4a24e047b15e2a5bd2dc55f541d0085cd9ca8258a`  
		Last Modified: Thu, 14 Aug 2025 21:06:10 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:e1643df565cffd6a300cfe13b8af5e47cccc47cd07b8a95d410538de5298f26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6bd6ce35c775eb4169acfa035daf5fbe2676fc667a8d9b11f1e17813760a7d`

```dockerfile
```

-	Layers:
	-	`sha256:9e7ac0d56cf96b1fcda8c82cad9443a89c5c1507f94fe2980d86278124a0f93c`  
		Last Modified: Thu, 14 Aug 2025 20:11:49 GMT  
		Size: 598.7 KB (598681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae81fe92d5cb5897168067d656deb2b07c06f4176a89d002e4d7d6ff7a9e11b4`  
		Last Modified: Thu, 14 Aug 2025 20:11:50 GMT  
		Size: 43.7 KB (43714 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:cea5b1955134065f8bc5c8fe1b27423ece75f874d31a0100334199c2243bf242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92574807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636735ed929b1fade1cf3b0802f91669517d6a618e1513709938289af1fee7c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8dda28bfc0d36b2cb180c6fd3e6a4cd86ecd59274144d20796a06aa044d95c`  
		Last Modified: Thu, 14 Aug 2025 19:18:59 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ad6b1df0987d63949c70018c4fea86e55f4647d138d50f9d0d6b1a34a79140`  
		Last Modified: Thu, 14 Aug 2025 19:19:02 GMT  
		Size: 1.0 MB (1032144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1811f8ad9016fdae08bfba73eb5823d071995c3df0399e43c62da53c16d864`  
		Last Modified: Thu, 14 Aug 2025 19:32:29 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d7f33c27276d664ab88c3f78c3c3159c094409cf70f5db8b7b76e4faad699b`  
		Last Modified: Thu, 14 Aug 2025 19:32:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abca05ab4dbfe896214facc48632d858005021df7694a35fb449429103ced3a8`  
		Last Modified: Thu, 14 Aug 2025 19:46:08 GMT  
		Size: 88.0 MB (87956406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a488b0cca14ce542904ce528702e9faf85982b7f95506cd5d7e03d2328b678`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5d46ac9534c0b26551098844778d2317fb94b8924544d95f4926182e6ef0e4`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56980443c1b48d438df159b47286ab5ec3a2c53eaf32067905741734ed39b97f`  
		Last Modified: Thu, 14 Aug 2025 19:45:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50f09621051b610960e741aacec411687f324dbb5ff2d962a3fa43c3df34b01`  
		Last Modified: Thu, 14 Aug 2025 19:46:00 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66451ff30e0ead51a39b4b8dcd77d878c41113fae5afee200ad5387185bb13fe`  
		Last Modified: Thu, 14 Aug 2025 19:46:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:36f82c5598cc5419d99b1f1e025c8fee514edf6dbdb63f6c2894cdbd1d5711bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8b5d1198ac07ff8d6d70f16497b59fdf11b0aa39a38e925c2b21eff66bb176`

```dockerfile
```

-	Layers:
	-	`sha256:2589c825e1df4192f1558e71c963ad1bc01c6b6fa254ea3ed5692e0417f4e59f`  
		Last Modified: Thu, 14 Aug 2025 20:11:54 GMT  
		Size: 595.1 KB (595105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1551105c4ae77c1e863e3bf59fe9a7656f3eda79d188627c2e5edf9ca62f417c`  
		Last Modified: Thu, 14 Aug 2025 20:11:55 GMT  
		Size: 43.8 KB (43794 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:13e1bce2b6eaaa204f57fa32015d4e9215a4f1bafa86f10f776b5eec4f19be16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108836880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d561a2b17f2fa80c9bb0877cc79277fd42a4c9b59d9153eb29bb48db78f28586`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d3c0f56503ab40c4140d482406fc770090c1cfa210c2d815c27c3258a8846`  
		Last Modified: Thu, 17 Jul 2025 05:47:43 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff15b55dbea7fde51e6fef1d6c983e6787f061f6e664e60be0bed1e73ab2ba1`  
		Last Modified: Thu, 17 Jul 2025 05:47:44 GMT  
		Size: 1.1 MB (1085403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ff73cb83ff95cd3fe3390cca7fe98ead3af3f7eaab789fae97b8d74ceab76b`  
		Last Modified: Sat, 16 Aug 2025 18:10:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dc9ca0ae2804ca5f780b8c8c64a1f57a291a2fb246d2145e51b10e549dce8`  
		Last Modified: Sat, 16 Aug 2025 18:10:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed992f3c6b5ff917f4b9c46d941052853a95813a1ccbf72e5b016ebef3f2a7e`  
		Last Modified: Sat, 16 Aug 2025 21:52:38 GMT  
		Size: 104.4 MB (104385257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e7ba98a7b4fe72c9e853d42b6c27d27e459768fd2dbf34d8a1bdf75fa8ee43`  
		Last Modified: Sat, 16 Aug 2025 21:52:28 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d287f5c1b714eaec7dbd6611429f785b5acc220dfc3151062dd23effe3c3a3b`  
		Last Modified: Sat, 16 Aug 2025 21:52:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dafc5a911e0794166c205928097b7098dd8c5c2fed5ffecbd2cf29f11a76e0`  
		Last Modified: Sat, 16 Aug 2025 21:52:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfc009c98ae2d44cbd3371b0bfaed729ac1f3f9ce5d01eae9990fcdbbf97ea1`  
		Last Modified: Sat, 16 Aug 2025 21:52:28 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff43402a2e4eb812c44c8944faa5fd74f00fc83fc74b54414bbfdebda657e7f`  
		Last Modified: Sat, 16 Aug 2025 21:52:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:26f7758f21289e762c62f4e14ad0ef0542a3994acbb84673df165fa5916ff17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147378415d7c1d5f87f7ac11d899c2e268d627f0759a8805607901f03920f225`

```dockerfile
```

-	Layers:
	-	`sha256:d6bae588e6d8169e2304093efb59636af62a6aaef428c28d6179904da7cc4c5e`  
		Last Modified: Sat, 16 Aug 2025 23:08:19 GMT  
		Size: 596.8 KB (596763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45f7f67563dc9e9ee1aca0789056a0f37b21e019bdbb5167d5dc2d66804a21c9`  
		Last Modified: Sat, 16 Aug 2025 23:08:20 GMT  
		Size: 43.8 KB (43800 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:c46841234c54d1aace5dc0294a4f955fc6c9f3aac1c9e50d2fe9e6d4004bb37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117446835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5d8f3bc1f068c012eabb2ebdc6fd657ea10fbcd2c38f500d2146ee1c1e0596`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf403390a37eed6f4bb75f6f5da24ef2cbbe8774ada82627e4d0e821092f247c`  
		Last Modified: Thu, 14 Aug 2025 19:27:54 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86202da6bb77005318244a960b1e8c704d587a448f1ca52331d1e81ccfa2b4d0`  
		Last Modified: Thu, 14 Aug 2025 19:27:54 GMT  
		Size: 1.1 MB (1081103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f874035dc8e0bdfe13d4565fe528274a63ad2b9ae6d16df5918abd6a2b4e521`  
		Last Modified: Thu, 14 Aug 2025 21:14:09 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee52d05cc2214a16d5d2a764d203277b34907a271da9644c99dcf76911703a`  
		Last Modified: Thu, 14 Aug 2025 21:14:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4498dbb9f71d4023e5cd309a539099c4d12decfae3996a150939719143815bd9`  
		Last Modified: Fri, 15 Aug 2025 00:04:53 GMT  
		Size: 112.9 MB (112886505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0da8c256f18036e746d2d5d23f1d367db4ecc0be4a9a26fd6f0ca37000c37f5`  
		Last Modified: Thu, 14 Aug 2025 21:57:55 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476927ecf0f87174fac33bcc48342ac27e5b9971846919c03c12a32174dc4748`  
		Last Modified: Thu, 14 Aug 2025 21:57:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122d716b7fdc99f5b35557d91be50ea1d2fcb9a020b497ce492433fc9e00106`  
		Last Modified: Thu, 14 Aug 2025 21:57:56 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2389a7588a9183d5469b09d1e5401011df6e3dfa91f4be5502deeb5b2be7b8c`  
		Last Modified: Thu, 14 Aug 2025 21:57:56 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275026e6ac0d9322b82260397247c663943622c66966ffe15479e24ff3a09c33`  
		Last Modified: Thu, 14 Aug 2025 21:57:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:11da0c0be90f4b066f1bddf8380a834a946b32f1326e44de6957de19657ec2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820d11d0811c4b4ead40eb2c550aeb7d37196eaaaaa4e8384820ccfe931cf146`

```dockerfile
```

-	Layers:
	-	`sha256:01b555c798439656eeb0a56b5306b1f64bcdbe1d5e5550548b8ff10a5cf594a7`  
		Last Modified: Thu, 14 Aug 2025 23:10:48 GMT  
		Size: 596.7 KB (596745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e2056900a7e49b75ef6994bf2ea7ab0e3a753c4dde6e3289434b025b73e45e`  
		Last Modified: Thu, 14 Aug 2025 23:10:49 GMT  
		Size: 43.8 KB (43751 bytes)  
		MIME: application/vnd.in-toto+json
