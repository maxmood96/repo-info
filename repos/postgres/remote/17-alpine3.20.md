## `postgres:17-alpine3.20`

```console
$ docker pull postgres@sha256:ebe7564018853cbb5c5a7d0d86d5c0bee7ade63b4f2d104bc159b61bf6992de7
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

### `postgres:17-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:25b8468ab07c3659ec8b66ef84722ed30827c4048ae9387cc46246a7efd2659d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98368237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305a6f95a0683f8514252095176bcc07ee298e5d48eb2c2dc5b41658eaff9a70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 19:01:08 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 19:01:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_MAJOR=17
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_VERSION=17.3
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_SHA256=13c18b35bf67a97bd639925fc581db7fd2aae4d3548eac39fcdb8da74ace2bea
# Thu, 13 Feb 2025 19:01:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 19:01:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 19:01:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a422ccf527057878c0657a858ba88fb1b17fa4f59c379e82ee8799c4ec37f1f`  
		Last Modified: Fri, 14 Feb 2025 21:09:27 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423c7f7e628a31c414166cee44acfb3cd086f1af5f0f7bf9fa6b9c96ba833f22`  
		Last Modified: Fri, 14 Feb 2025 21:09:27 GMT  
		Size: 1.1 MB (1120293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b2ac2d4f5306ce3aabd9be9796c4a5d1ff3e3b7afc738dbd0fd98439ccd830`  
		Last Modified: Fri, 14 Feb 2025 21:09:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e2455d364656dbdd75fb8afcef2488051d061f92b9ef6af42ab5fdd54fdb7f`  
		Last Modified: Fri, 14 Feb 2025 21:09:35 GMT  
		Size: 93.6 MB (93604166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce7e681050c26eb43bacc7e0c74978cfbfaec79fe7bf0e560d853b9a9393c7b`  
		Last Modified: Fri, 14 Feb 2025 21:09:27 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c92f9c88f157655770fa649fcb279e0e85fb50eb1096956e8b5166cf96561ea`  
		Last Modified: Fri, 14 Feb 2025 21:09:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4b5bb2facc21a88666ba4036d801744e3ee819778966312ce26a89098ac1e7`  
		Last Modified: Fri, 14 Feb 2025 21:09:27 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13adc540ceeadb0c20fef406e76e5cf05cd5a46b31eda0f551fb81fd6ec4bb52`  
		Last Modified: Fri, 14 Feb 2025 21:09:27 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0b38ad03314ea06be5612163b50da9eaff3e418f790ca617155a4f009af8aa`  
		Last Modified: Fri, 14 Feb 2025 21:09:28 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:96925c74fc97a288cf8db076c796d8b760e1797999d2e2e730f9b0e52a07b57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.2 KB (632235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de9f0fb6e8df439696daa876167b55df7a9e83e05c233ca189ca2647b5e916b`

```dockerfile
```

-	Layers:
	-	`sha256:0b8167ec785c70eba91365d0eac2715833d6303b29f5a9b1186a50e14ed17d21`  
		Last Modified: Fri, 14 Feb 2025 21:09:02 GMT  
		Size: 589.8 KB (589832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910ed812996880b5609489ef3e194aba9bb5466410c71373cdef1ef9f4173167`  
		Last Modified: Fri, 14 Feb 2025 21:09:02 GMT  
		Size: 42.4 KB (42403 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:f667d3fb98b6284f3c91ce8abb954712a39968428dfad982e4f7ef4f7557c337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97008885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b44bc8d15418cb098b9b2fe04fbc3afe000d734235ad9c515e5360687b95561`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 19:01:08 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 19:01:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_MAJOR=17
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_VERSION=17.3
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_SHA256=13c18b35bf67a97bd639925fc581db7fd2aae4d3548eac39fcdb8da74ace2bea
# Thu, 13 Feb 2025 19:01:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 19:01:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 19:01:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f562bdeccc677affba17117a3e71eed437842fbd24407b2ce425aa5819d3dab5`  
		Last Modified: Sat, 15 Feb 2025 00:09:21 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c15f54b7c7b9df1d9b4f973855ca80d075a47a5343b27c0f6e4ae7774389b5`  
		Last Modified: Sat, 15 Feb 2025 00:09:21 GMT  
		Size: 1.1 MB (1086525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc1372a5f57dcd34d27e141a48157389c01e5db33ceff6cd76a810d4aac4b54`  
		Last Modified: Sat, 15 Feb 2025 00:12:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd341632ea776236fe80665f19d62a5b5a1cb1d1630a822cef2e43775a775084`  
		Last Modified: Sat, 15 Feb 2025 00:12:39 GMT  
		Size: 92.5 MB (92532941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00172e64076de487062049939ee5eb52b8c0e3d7cabd99f7de713c661d2e7525`  
		Last Modified: Sat, 15 Feb 2025 00:12:32 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a49a7fe771ab3b1fdaba6c76c84dad0ecfb22918599ddb11255ac389a73909`  
		Last Modified: Sat, 15 Feb 2025 00:12:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e826890282547cf383375fb045f749980164d5b10446270d5af99e9482d70c`  
		Last Modified: Sat, 15 Feb 2025 00:12:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e47e4b663fa05e2469c38a8eded501f94040b356ddba4d0083f21b7b51d482`  
		Last Modified: Fri, 14 Feb 2025 22:33:15 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06846fc224a95823b9c5cc045964ddb2f246d3d274ba98b628ff24ba9a3ce66d`  
		Last Modified: Sat, 15 Feb 2025 00:12:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:5948573d59c47ff47604a0f88008935033d304477193651e7daa4df51067b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 KB (42347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f934fe3afea19ff1ac6d4d84f85524e557f099036df9e3221bf1b0c603f1a17`

```dockerfile
```

-	Layers:
	-	`sha256:d76321240a90cc51f37d7eed03915330bd32ebcb49e309c99a634ef609a10d44`  
		Last Modified: Sat, 15 Feb 2025 00:12:15 GMT  
		Size: 42.3 KB (42347 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:31c11bad28378dd78970a3aca790c68409a6234f3716a60da129986f2320a722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91363075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91699cb808db35cf8cfbcf0b2f973718adeba4de981098c52aca8ac6db22f1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 19:01:08 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 19:01:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_MAJOR=17
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_VERSION=17.3
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_SHA256=13c18b35bf67a97bd639925fc581db7fd2aae4d3548eac39fcdb8da74ace2bea
# Thu, 13 Feb 2025 19:01:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 19:01:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 19:01:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25896e659de9add0d4b908897850cbf64b7928b4104747d7d2f865d03c785b5e`  
		Last Modified: Sat, 15 Feb 2025 00:24:03 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f74483a18f569a1fa2c939344a028b1612c307bf93662a4fdaf02c3f961ae8e`  
		Last Modified: Sat, 15 Feb 2025 00:23:59 GMT  
		Size: 1.1 MB (1086514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0c319e5f187e02e312b83237af62b7b995a5b55af59cf9608af4f0fc3e9be2`  
		Last Modified: Sat, 15 Feb 2025 01:04:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c68776dfab4898e08ad4e46f0dd48bc35a01674d31c1778365d5c3fbc4537`  
		Last Modified: Sat, 15 Feb 2025 01:04:10 GMT  
		Size: 87.2 MB (87163715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b001ed874e722f147e2e2580a0b6588dac112c355ca0c60afd4e37b31a47edc3`  
		Last Modified: Sat, 15 Feb 2025 01:04:12 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf80d21e6d4f057f61d318e639c6d6598f7c64e872a9b3f03b2a3c5f9539994`  
		Last Modified: Sat, 15 Feb 2025 01:04:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017fff3d9e794b1950ae8deaeb57ef404d4fe278e9281fa52dc1ceae1bd6bb8`  
		Last Modified: Sat, 15 Feb 2025 01:04:15 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad9f8510b7c6f8e3866133ce77b01706f1219d21c747298d7ef7e887fdf643a`  
		Last Modified: Sat, 15 Feb 2025 01:04:16 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8df5809227ac47268513bbcbf746aa24e472dea21b85b8989bb4252e2c6e3e`  
		Last Modified: Sat, 15 Feb 2025 01:04:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:5f3f569d4b93dcd999a87fda3416c591806623e1b0ed4639a4bfede7e505f39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.4 KB (632422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b23736b338c5b10df7f13cf037f82c3380e8dd91f5f6dcb9f5727c18be82a6`

```dockerfile
```

-	Layers:
	-	`sha256:e9b91377e8953756afd63734c71e2df29f29726c5e5860a96da3a5c5c63060bc`  
		Last Modified: Sat, 15 Feb 2025 00:12:16 GMT  
		Size: 589.9 KB (589860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df0e1bc346f6b70c2e01cf6b83360f2eddad243d2e68c1493b4669a89708054b`  
		Last Modified: Sat, 15 Feb 2025 00:12:16 GMT  
		Size: 42.6 KB (42562 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d43871566845f4ca8b72c94c7e94085c5e9c15077770bfedc9d4acbf4bc87407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97582287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bb4921d56ba2bc1b0fed6ad053a99141f3f2520d3fd4b9900cef2f858972b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 19:01:08 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 19:01:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_MAJOR=17
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_VERSION=17.3
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_SHA256=13c18b35bf67a97bd639925fc581db7fd2aae4d3548eac39fcdb8da74ace2bea
# Thu, 13 Feb 2025 19:01:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 19:01:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 19:01:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc8827c16e8ec088d48c0b753a38f9b70fa76626b8e70929dbb63cf84cc89b5`  
		Last Modified: Sat, 15 Feb 2025 00:22:17 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0907d060ed36b58b8341b1b05e996014c48ca9a918bb7414420e2e27fa4bc054`  
		Last Modified: Sat, 15 Feb 2025 00:22:10 GMT  
		Size: 1.0 MB (1049755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d9f69255eebc2a3a8c29690561f536203f6f168cd0048af59833024fb4abbe`  
		Last Modified: Sat, 15 Feb 2025 01:04:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae72317fdde25372a399341e4dc71b5a4394e871158b1e56d35cbc4f92261337`  
		Last Modified: Sat, 15 Feb 2025 01:04:34 GMT  
		Size: 92.4 MB (92424489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed06c9046dd4b4c005cefb43ad3c11bfa74224be1f63316485352b1a85d64ddc`  
		Last Modified: Sat, 15 Feb 2025 01:04:36 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8a7cc6b60efbf2e4233d8c6b41da69d4023c5624290abf5fb1347b3a780f51`  
		Last Modified: Sat, 15 Feb 2025 01:04:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1746006f4b69c00a2cd3d6c39b6b1d3fb7ed652441c3b6c1d6497bb6c256fcd3`  
		Last Modified: Sat, 15 Feb 2025 01:04:38 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a8c814e4daa0e4c8c4810e901f760c3151394a5299ca36d2c53de1198cf26b`  
		Last Modified: Sat, 15 Feb 2025 01:04:39 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8fe14a0b9c923c5894e6786a6f82e0f1695cf484ad1071fb84eb983a7b1f6d`  
		Last Modified: Sat, 15 Feb 2025 01:04:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:80bf828b70919690d570e4bdaec5d06468e06e1804ba282c34e5c78d1091f9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.5 KB (632476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8361e0c6013a077d108f3506129a1475db37d0736ca4743382902e1ec28a98`

```dockerfile
```

-	Layers:
	-	`sha256:d18f34138a47502eaa33eefe91b7e237264f4bb74966d1be255feec9bce0de95`  
		Last Modified: Sat, 15 Feb 2025 00:12:18 GMT  
		Size: 589.9 KB (589876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:552bae1854b00271192bbdb9d640b0f76e8a096aa7d62e39535da1675f4dc2d1`  
		Last Modified: Sat, 15 Feb 2025 00:12:18 GMT  
		Size: 42.6 KB (42600 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:f6f6ea229f84d9da5d91151fa70fe8bf7810d3b44171eb598d64a295c00eb42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103724399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d049fde61a3c285ff72192d05f57f72298deef7848e5e96df1c45ec7ed38a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 19:01:08 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 19:01:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_MAJOR=17
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_VERSION=17.3
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_SHA256=13c18b35bf67a97bd639925fc581db7fd2aae4d3548eac39fcdb8da74ace2bea
# Thu, 13 Feb 2025 19:01:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 19:01:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 19:01:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f0c9e0266d07b1e48211f41a405b6a9626c60ebb74dd37e2b1a3d739b053b`  
		Last Modified: Sat, 15 Feb 2025 01:04:50 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9662f3ac6b0e27b4365cb8e0a64271b1c96d860bab5be13f7555d3c157c60a38`  
		Last Modified: Sat, 15 Feb 2025 01:04:54 GMT  
		Size: 1.1 MB (1095374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e720a2f3980e084f149deb536eba309846d5e204940730520319329f97683c60`  
		Last Modified: Sat, 15 Feb 2025 01:04:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185a7595f03ee64f8d1d699721c81c9e6af9845d1b7caf54bd0b899776f9cfdb`  
		Last Modified: Sat, 15 Feb 2025 01:05:00 GMT  
		Size: 99.1 MB (99140475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77bb0bc3713d4cdb274c6e5a36d5dd11e6822532d3a625f95f1102c7da67ab9`  
		Last Modified: Sat, 15 Feb 2025 01:05:02 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3c03b810041815ca30ebf76e69096a62c16d509bf06e65622ee3066094c91a`  
		Last Modified: Sat, 15 Feb 2025 01:05:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234ddf0cb0e8570a3d9075f9eaf192e8b9978d85e175615446aa52a11a11b19`  
		Last Modified: Sat, 15 Feb 2025 01:05:04 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4963102022d1684760823cabc300019962c13ff4d1482374c6b05a43b9115f98`  
		Last Modified: Sat, 15 Feb 2025 01:05:06 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20109783ec54b1ff23c8a0da59acfad3b4c8fa847f2210033eda79ca1ffcbed7`  
		Last Modified: Sat, 15 Feb 2025 01:05:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:2e0d334fc72011a2d1e3f11c321eb1ec6d9ca6259538fb5f43fab7074964b2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.2 KB (632174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb12f99c47cebdcf6cc40ed9b1009df20280666aa4a6c5a734bf1c34250c1d7`

```dockerfile
```

-	Layers:
	-	`sha256:5efaa24db730349c33ef49ef3cffbe9a5f01277ccc61777203e5681acdfd7daf`  
		Last Modified: Sat, 15 Feb 2025 00:12:19 GMT  
		Size: 589.8 KB (589812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18dec378a397107202086cf0c6b35f4bbd8292358cf927101a91cba5cdfdb5fd`  
		Last Modified: Sat, 15 Feb 2025 00:12:20 GMT  
		Size: 42.4 KB (42362 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:c432e26953043ede1d8f10e18159ce286eabba2b12e9ffd6a0594e5b8e98dab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103016383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d29eb7f7f82d3f77177ec76e7c95294acc079a6e889de4ee454d3f9963c43b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 19:01:08 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 19:01:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_MAJOR=17
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_VERSION=17.3
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_SHA256=13c18b35bf67a97bd639925fc581db7fd2aae4d3548eac39fcdb8da74ace2bea
# Thu, 13 Feb 2025 19:01:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 19:01:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 19:01:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4560e6eaf6136fe9ed082dd565c5a37bb5ec3e433bd72a01116ae44bd04994e`  
		Last Modified: Sat, 15 Feb 2025 00:18:37 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a2d29dc8697219ebfcfe5e6e5c56b2549f8e69e4f3f0bdf9803dcbf630c294`  
		Last Modified: Sat, 15 Feb 2025 00:18:31 GMT  
		Size: 1.0 MB (1040018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a956be5bcefb3aa53694b1f5072ac7e1a62d33e3f466db0382981289260d427`  
		Last Modified: Sat, 15 Feb 2025 01:05:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3601b14eba9d79d9a775cdcd1c0fc30aa1636c5a7e0bb819ab04eaca6cba63`  
		Last Modified: Sat, 15 Feb 2025 01:05:25 GMT  
		Size: 98.4 MB (98383800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b222e72a39976d42754c8a6f785783c58a915a09ad2e1be556796f0b79c53ae3`  
		Last Modified: Sat, 15 Feb 2025 01:05:27 GMT  
		Size: 9.9 KB (9888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c350f31956256d00526b38f533d3f1082cdd4f548e75b25c8c44d33507fb0e`  
		Last Modified: Sat, 15 Feb 2025 01:05:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a71bea8cecfe95fd7892593c5e7376261b8cbf866f53c10ff0577810443fc29`  
		Last Modified: Sat, 15 Feb 2025 01:05:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621cf36be3569bdb734dfbc8d0e53f60d424dea1e4ca132a38114a299987f32b`  
		Last Modified: Sat, 15 Feb 2025 01:05:31 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b27227c5c5d8d12993438a2094c18f7a3b1a3014544b024ed1a7ba61818887`  
		Last Modified: Sat, 15 Feb 2025 01:05:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:f11677ee067807f944b6ef04d0e681984883b7ee76f32c5201c6eb6a77e91f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 KB (628702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f383b9c7d88db09ea74244854b48348e5d4b29d5fef76a90f5ea3a77c2dd92`

```dockerfile
```

-	Layers:
	-	`sha256:9ed0609413ac394f52f64670ef1507b35dbbecbf3dcf3d942704cb6e5e623b07`  
		Last Modified: Sat, 15 Feb 2025 00:12:21 GMT  
		Size: 586.2 KB (586247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf7bf6ea94049a0d74992884177b47a48df163ecb6d602b04dc0b8c4e78d829`  
		Last Modified: Sat, 15 Feb 2025 00:12:21 GMT  
		Size: 42.5 KB (42455 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:c860103a84e7d07606188392e96914f66f0d16a7fd73e727388177e1356e2786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98517769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8b03a095ae508b647dc52533af10cf32406983645eff7219945d8e0eba12aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 19:01:08 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 19:01:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_MAJOR=17
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_VERSION=17.3
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_SHA256=13c18b35bf67a97bd639925fc581db7fd2aae4d3548eac39fcdb8da74ace2bea
# Thu, 13 Feb 2025 19:01:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 19:01:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 19:01:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 19:30:36 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a667969f118faf629e202aac4ad97cc21b7c3811a145f4275dbf42e59555a`  
		Last Modified: Sun, 16 Feb 2025 01:00:44 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebfd62b87648c7ac5476d245882fa59a55ae434a2214feefa5b371c5fd1aa34`  
		Last Modified: Sun, 16 Feb 2025 01:00:45 GMT  
		Size: 1.1 MB (1089587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b380aff9bdfc35c380af8e1615d6f44fa39e3b86059ac3e2a6e7e6479d2cd6d`  
		Last Modified: Sun, 16 Feb 2025 01:00:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4774f2467a83189ecd4b5c9a7b6a4ae4bed7424b1f2a66e397a313f3febe0135`  
		Last Modified: Sun, 16 Feb 2025 01:00:50 GMT  
		Size: 94.0 MB (94038053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072b52f2a39ec67937573ae7f8c06bd901934a1eb72af81862a0b1f63c448929`  
		Last Modified: Sun, 16 Feb 2025 01:00:52 GMT  
		Size: 9.9 KB (9893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedc0bdbeb671f0f78882b797808b678395e45d3183a50b1898fd213a4050aea`  
		Last Modified: Sun, 16 Feb 2025 01:00:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a101c2025df7abaad74f3cce91fd977c86f0a55491f4f7e42f5e10dc13460`  
		Last Modified: Sun, 16 Feb 2025 01:00:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002b7d191f47442a4eb269f801011818a28e17998773789d98ed85e4c11a6224`  
		Last Modified: Sat, 15 Feb 2025 23:07:13 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751dbf7d28de36186d9b4ecafa27078f35501cab0505676da9f200ffa2eac6b2`  
		Last Modified: Sun, 16 Feb 2025 01:00:57 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:33baabcb747748d84561548e44d8920ef25cbb8c9549fa0dde2df9440c32952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.4 KB (630359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fb50159cf0f0b7c1bc78c643c5c471fd4128e5f9d6c334d00e7b670511058b`

```dockerfile
```

-	Layers:
	-	`sha256:25cd9749e7e08c5c4993d9050946be43794ff36059b3abd45b35053fa028cd97`  
		Last Modified: Sun, 16 Feb 2025 00:08:50 GMT  
		Size: 587.9 KB (587905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4716095241e7c336c0e4e7c6616d64b2f066f76ca32ded08757c309302587c93`  
		Last Modified: Sun, 16 Feb 2025 00:08:50 GMT  
		Size: 42.5 KB (42454 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:b603047444e5333d5afc4b87e7a75f207425fd7edf68b27360253381fdf31ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107317638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24880c1382acf50e936c2bdf5fe0bf3d78be48235c0b817e1ba2853144885fcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 19:01:08 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 19:01:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_MAJOR=17
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_VERSION=17.3
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PG_SHA256=13c18b35bf67a97bd639925fc581db7fd2aae4d3548eac39fcdb8da74ace2bea
# Thu, 13 Feb 2025 19:01:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 19:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 19:01:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 19:01:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:01:08 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 19:01:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 19:01:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bd808fe0e001bd5a66a02c69406d4cdeb252f933c590cb4d320052ea3b3546`  
		Last Modified: Sat, 15 Feb 2025 00:16:42 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b626b09720dc73a31296f38e3ebe6c64e8a0f0170f1d84c424109e9cbbfb03`  
		Last Modified: Sat, 15 Feb 2025 00:16:35 GMT  
		Size: 1.1 MB (1084163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eb8806d6607755ec83ba1b6ae29378821a1c707f5bbbffc9ebaf9efda2912c`  
		Last Modified: Sat, 15 Feb 2025 15:21:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f590776f56e17f877ffb94302914d20dc22fb6175031c11d9f48f96436676e`  
		Last Modified: Sat, 15 Feb 2025 15:21:56 GMT  
		Size: 102.8 MB (102752465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d706a383c1a17992fbb1c630edfb26a369ba341f534088ce33cb921114e822`  
		Last Modified: Sat, 15 Feb 2025 15:21:53 GMT  
		Size: 9.9 KB (9891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a1ef1cfe94a79d4ab008e8c9300f0e8d484030b6d4894795ee6692c0233f1b`  
		Last Modified: Sat, 15 Feb 2025 15:21:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2048ae860eb6d94a34fcaa96fab7348ae99fcc02a370a5502b729cea5d9b6efe`  
		Last Modified: Sat, 15 Feb 2025 15:21:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7665f39abc9df4e4635cb623662d8e2c7eb711fb89795eb5392a1239012e51`  
		Last Modified: Sat, 15 Feb 2025 11:13:08 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929b4028898bac6d21677baf279bd7f28cfc43f9fd586d421b523a3d9a2a5a09`  
		Last Modified: Sat, 15 Feb 2025 15:21:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:16d17d024af3d0c0cfe11627b5a91e7619ae28ae7a9ba64653d1f43cb00c6ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.3 KB (630290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b1ccbfa08725cf2de5343f03804d65b19d0bb3cef23b98115cd2b792ed0658`

```dockerfile
```

-	Layers:
	-	`sha256:aacede97c7e5ef4c7a944793c00001e5680e91a6e9f1c595da3b3cdb343875b5`  
		Last Modified: Sat, 15 Feb 2025 12:08:42 GMT  
		Size: 587.9 KB (587881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:549b53e73426ed8fa367ad2ed9f950842d73a2fa0f934035e5212fa668c27334`  
		Last Modified: Sat, 15 Feb 2025 12:08:42 GMT  
		Size: 42.4 KB (42409 bytes)  
		MIME: application/vnd.in-toto+json
