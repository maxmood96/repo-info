## `postgres:14-alpine3.19`

```console
$ docker pull postgres@sha256:ea6d1929689bc4e44670a493d06193d9cfc31c6c3d0f0f3615757a6aeb18ac2d
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

### `postgres:14-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:fdef6426d64901414fef824617c695e3bccf51c6767cc496c986fd8d3ec27210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97384969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e43a2e0a0a3bcf54dd593b56eb6831a341477f08d57a8bdee5c9afb72b7691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7f2aaa40a8378a9ceb18a7b191cf1fd4ef319bc473301f3b109bbb6adea1b4`  
		Last Modified: Tue, 12 Nov 2024 02:38:10 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20113b28a8e3caae9a84e660439154bb3ce3c2f2edde8de8232debf3d3a74276`  
		Last Modified: Tue, 12 Nov 2024 02:38:10 GMT  
		Size: 1.1 MB (1120288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241e030f0057c30becd6943054d6b05136751bab3e5394abcc098717ca58cd5a`  
		Last Modified: Tue, 12 Nov 2024 02:38:10 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477175d5bb950133e718deda82060d6c89eef2e424e65b1e6e709d4ee6e89542`  
		Last Modified: Tue, 12 Nov 2024 02:38:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87f8b229a2433521b716dd8dc0373a328eaf5d843a3fd1892544dfb19c176d5`  
		Last Modified: Tue, 12 Nov 2024 02:38:13 GMT  
		Size: 92.8 MB (92828299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39330188e1a14c4d283c4f55994e18b32d1a8544fc431a6351dd78be57f29ae5`  
		Last Modified: Tue, 12 Nov 2024 02:38:11 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7486d936e5fe728151d2792cc86fba7f1f99ef0361e0c4f33cd0700f41e3f76`  
		Last Modified: Tue, 12 Nov 2024 02:38:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e4243250ab52877417c1d2b659be879a7c572742ec2ebdfcf51a99af645e7a`  
		Last Modified: Tue, 12 Nov 2024 02:38:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ae1aec6ca48a0fb77e7336623be2d998cbeec5ab1dff608e9301b775221a7d`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b48c060979817a368e7904341b7636125f31edc9126a3333b3ab0fcb162e44`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:fc96900824e8bfe4c1bf085703e6c466074979a7c3767623f14edd6bc2a6cebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df44f78ae34200f2a9df2540d960dec0974881bedb9f8e72898377b96acc640`

```dockerfile
```

-	Layers:
	-	`sha256:cf2719912ae362ef9156a63743ffc847a73aa11620671fb049b3b6302dfbde43`  
		Last Modified: Tue, 12 Nov 2024 02:38:10 GMT  
		Size: 969.0 KB (969003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ddaf8ef50024761951780695a0cd6beac9483fdefe710183da207f5d61106a2`  
		Last Modified: Tue, 12 Nov 2024 02:38:10 GMT  
		Size: 45.0 KB (44979 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:cf304f7f071458a8bc3cedf3e2d75119fac40e295ed9563682dfd135bfbfabdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95831609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d690e0cb70563f5837b727f76145a19ef89ce77133cc756262afebbe10eff29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1129eba1c516693bf2f340f0343f658e37e7812832c7f2e7493ce214856d3fc0`  
		Last Modified: Tue, 12 Nov 2024 05:41:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1855f1ed4c4392b8709ed6c84e2a119012e83c080f39bb8faf7f1bbc735a9252`  
		Last Modified: Tue, 12 Nov 2024 05:41:41 GMT  
		Size: 1.1 MB (1086678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255e16740a45a54b3ba44f9bce09b1f67b316dd94e12dc4ddfcfe274678036ac`  
		Last Modified: Tue, 12 Nov 2024 05:49:37 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8874dbe6c02989a5e3c4a6f7b2a59292b8f32afd21211d3933902093d814455`  
		Last Modified: Tue, 12 Nov 2024 05:49:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01eba24e7398fe256f551b033eddfad1ac6682c62e22db87cc6418e326d96983`  
		Last Modified: Tue, 12 Nov 2024 06:05:36 GMT  
		Size: 91.6 MB (91551827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6e82bb72875e222c67d0caa608697e33298757b9e9c0bbc40fc4cdb99d06fb`  
		Last Modified: Tue, 12 Nov 2024 06:05:34 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e9830df3dd7ed9a9d22e3a33f378876c1ada7b5237b7b8d791d756f36c4615`  
		Last Modified: Tue, 12 Nov 2024 06:05:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d64c32e85cd0b15152819e5b713eba3334ad3c3551da90f925c9c4156c79302`  
		Last Modified: Tue, 12 Nov 2024 06:05:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd02f0b4dabc335e371b2497fa7846d240d9cb7b3ba26feefd0b2d7dfeb4860d`  
		Last Modified: Tue, 12 Nov 2024 06:05:34 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472bf17087ff7eb06bbbf7c12ed763e1d49caa5ef1a786a7a140eefaa4a21b9`  
		Last Modified: Tue, 12 Nov 2024 06:05:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:38ee1d3694a18a46b66f07b91227a67cc41fa67526a1944c1b3f51065fac459d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 KB (44928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86961385ae61170f27bda4d529ec3ea036cb33b7646edfb7c5fdd877ce14445`

```dockerfile
```

-	Layers:
	-	`sha256:0727f5cc820531025b929b80b300482c8e0a9768773d96233bad7feb6ed584c9`  
		Last Modified: Tue, 12 Nov 2024 06:05:33 GMT  
		Size: 44.9 KB (44928 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8cfa6bca89c4763d395646603a5f31178929b3c7c7e9624f98573d3db34f9a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88552387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88198c6be2a74c523a48deed03312d0a6e7760f62805fd1ef6786c11602ad625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
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
	-	`sha256:eda4c519495926cbe7ff7866cd069e5e5d0030c3c4820ecc3fe49d225ecc78b1`  
		Last Modified: Sat, 07 Sep 2024 09:34:18 GMT  
		Size: 84.5 MB (84521373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b2d2bda103238fb41d0b872a112bfddb67d4b23b249ec1a8009e5cf1e382b3`  
		Last Modified: Sat, 07 Sep 2024 09:34:15 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7463bb0420db286a7ca63a27aad6dc68fd777145bb64eed9090d72f5cc6fac8`  
		Last Modified: Sat, 07 Sep 2024 09:34:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb24cdaa82e758269a9aa22e75857c61da4ae480d5f254aee01ad13dde4be33`  
		Last Modified: Sat, 07 Sep 2024 09:34:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355eb5384222d0550d3f499816e0b1973f0e5278ab1fc8f7c4615b5dbea8a404`  
		Last Modified: Sat, 07 Sep 2024 09:34:16 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123291e45bcaa47edda4e5df8cc1ccc0651208e66e2c5687c3a65c96525020b`  
		Last Modified: Sat, 07 Sep 2024 09:34:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:727fb409b45a794faa1ebce924d7c1ba50cb4151ccbaaaf8ae1a865c13279588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6ef1b16f567e7634765be09c93d24927ef5f49132f369dcae16442476021a4`

```dockerfile
```

-	Layers:
	-	`sha256:691a35066fde8be9b9c6dec8765517e01fae17ade6285a15cccb48841f4c4a87`  
		Last Modified: Sat, 07 Sep 2024 09:34:16 GMT  
		Size: 968.7 KB (968705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f47d1c0ebe3baa9de83970acfddf27fbf217df9dc1ac87b2be380c362494e583`  
		Last Modified: Sat, 07 Sep 2024 09:34:15 GMT  
		Size: 44.9 KB (44946 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:1c7823797c1b6580e78efce1d555cdc200aed5582f0aeea6109ef57e8ba409d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94022491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f50dd7ce08cc2d8d4f6b661d271dae5f1d103ad7cbe3891156e28b9e9ed796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
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
	-	`sha256:d0eb74c6e0a374f8a358270e8ffb3d907fa653cc8a37cd4c6362813ca8459fee`  
		Last Modified: Sat, 07 Sep 2024 09:03:57 GMT  
		Size: 89.6 MB (89597379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be03fef46638c53610203bfdd0c4e977a3c6e403bf96da7823db5a93c1d9b47`  
		Last Modified: Sat, 07 Sep 2024 09:03:55 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275ca8e3074fd12405a11163bf01b0f42b55fd43ce942b7a3fae545161493470`  
		Last Modified: Sat, 07 Sep 2024 09:03:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7c411d31f4da8bb821f6e05d22c34191ec4a9a53fad63b0524e192df56f0d9`  
		Last Modified: Sat, 07 Sep 2024 09:03:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5bd2c9109c3dd67c55271bc00df29de2cf896f13a1455f8db822df9a2ac1d`  
		Last Modified: Sat, 07 Sep 2024 09:03:56 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329427f47f72c55fff83ef0b2b96796e7c7d9c9fa365824fba8b131d65c5ab43`  
		Last Modified: Sat, 07 Sep 2024 09:03:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:c3b7714e1cc52dc27105904ff48fa0eddcf1ac5ecbceb3662f1dad7aeadba3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9744d0eaa8b291caa8eae8878a8c1407850483c663237f5a3c5138556cc3d43`

```dockerfile
```

-	Layers:
	-	`sha256:09c9552964e8379aefa114a3e855c454557f943cdcee9862da8576700ddc5f9b`  
		Last Modified: Sat, 07 Sep 2024 09:03:55 GMT  
		Size: 968.7 KB (968717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34eb6468d153c8abc847c2e469e846559215213320a5b50280f6b5abc4fa3f5e`  
		Last Modified: Sat, 07 Sep 2024 09:03:55 GMT  
		Size: 45.1 KB (45064 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:dc5b99be85e3cad651b487532020767345c4d74ededf52885bc5d48a9ef8d0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102487255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c15abddd75b9df02e1f7a6964ef5f3064da8d5554fdaf29b8cb3f207e808df8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddcea63aae35520c6333dc038dd33a4fc785dc00e2a50243c0fe6c2982106e9`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593bc3970d36cc0fe517861164999c046031e954342967bd21315625bb1f654a`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 1.1 MB (1095469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e8d5aaba9d074e3966a91db421ef7ba317eef4a23435991923568139bdaf7`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b670ed0c4ca2ba8bd4e8f83730b398cafd3d32adf9273d1c4b213bdf3726148`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0327a43f80321b12b35f613a8079bd22734b7a2870bcee49d63b60f02a40309d`  
		Last Modified: Tue, 12 Nov 2024 02:39:05 GMT  
		Size: 98.1 MB (98121458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1c3ac9bb88a3c8652e62ca271be98f557e197af643eccc933f509c079021c0`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b38f519ed6c1914b59b28342a380c0a426c357478612b83da5fbe744e895f86`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e0e8a125706835df1eca0c5831da31de5264764c96d23ed51d4c9cd94c9836`  
		Last Modified: Tue, 12 Nov 2024 02:39:03 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f261bbf758e58337ba8a7369916ce0993f2946456186e7b94fd3d7179f1749d`  
		Last Modified: Tue, 12 Nov 2024 02:39:03 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11229274d497893d2e81a41e20f32937a4883a46844a00cb8b59f8edaf18157`  
		Last Modified: Tue, 12 Nov 2024 02:39:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:fbe2a1048bfa693a01a7aee29405121176dca67a2e60d3503b35e095e7c64397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a0b0fdc7802eb3b166a2b9a40824daed006ed900b4adff7fcf330230922f27`

```dockerfile
```

-	Layers:
	-	`sha256:572814463184523185ac8fea5ab41f114644e3bcc0d29d42fa0e92e812650c2f`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 969.0 KB (968988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c778b944074772d6db327999e2497218770b0fff532f562e762836046de2fa5a`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 44.9 KB (44941 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:11cfd05aad41fefb5a5ea4f1dba2d03724f906dd441f68b7a2913bf3e714dc10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101749586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b7d1c81faf1c1aa014c21a0d371a200f281b5320a6b3111c930dd03a08329`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44aed1596aae53b43b5c560a70ed3077f01224dad331cd0f195462cd93de112`  
		Last Modified: Tue, 12 Nov 2024 07:04:17 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c1eec1649b1b27928c826ff7967e09692327c62f6641f0fb1010c2e92117e`  
		Last Modified: Tue, 12 Nov 2024 07:04:18 GMT  
		Size: 1.0 MB (1039697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ad50198d9aa09c32245fbf4ebc775137c6396b849af754b3cb0958d7b808ae`  
		Last Modified: Tue, 12 Nov 2024 07:13:05 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d730f1e31929ec96a765b66b931f5f6ee89769f0e4ad0de920de3c467d6977`  
		Last Modified: Tue, 12 Nov 2024 07:13:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ad71c95cbe3a78a566ab2733b16156f30438d4b3effcbfa440042b647151a1`  
		Last Modified: Tue, 12 Nov 2024 07:30:19 GMT  
		Size: 97.3 MB (97328721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ff3af36763a20e001adb936705ade084120ab93ae1abf1c8e6a95326d93885`  
		Last Modified: Tue, 12 Nov 2024 07:30:15 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6fe3bb9f4589d1fbe10c580c4b6173107cd651f949a7bdddc32562aa8db33b`  
		Last Modified: Tue, 12 Nov 2024 07:30:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f9802e370da7452a87458c9f5761231ca530a10c2f290eb4948f23705921df`  
		Last Modified: Tue, 12 Nov 2024 07:30:15 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52d0f462c7b528fa820fb20f806a8b04e354918e2688c50f17f1175efabb3aa`  
		Last Modified: Tue, 12 Nov 2024 07:30:16 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90529e27c1797e0f6729c6e4b81a92a940e455744b0ec5081a09a23b8a455756`  
		Last Modified: Tue, 12 Nov 2024 07:30:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:19ca64305d0832b0b892141e8087fe97e284247766589f575acff49ea84db992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3147e1e468a09a446073efe50e447c544302818da585afdec9a268a12c053547`

```dockerfile
```

-	Layers:
	-	`sha256:9e919a14e95705b6f253b5ebf872ce3175758c0ff218ec4ae21efb12c761851f`  
		Last Modified: Tue, 12 Nov 2024 07:30:15 GMT  
		Size: 965.4 KB (965407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d0fbd4f2ecc3877b7145cb276facbe0abf8e412fc631c15666ee61a17fb764`  
		Last Modified: Tue, 12 Nov 2024 07:30:15 GMT  
		Size: 45.0 KB (45027 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:5d3c2fea9b23c1bcf9b1e562117e462548914c8b906a7d784d89c0f388b514c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (106015481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeccb7f6e183f3837f1cdc50dc97bab4066e6258f27adb2782b5eca2dadf87d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be5dc1246d0976e782f1978d2b2c680cd917af96a6f248e327cf6c5a71ddbac`  
		Last Modified: Tue, 12 Nov 2024 07:39:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea0a759c44d4c20668d2dd240b15b5122b742a9976f56b2975b365b6c05623a`  
		Last Modified: Tue, 12 Nov 2024 07:39:49 GMT  
		Size: 1.1 MB (1083901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca36db6f4d56245ca10555850fe42a93b94514e3a413dfee1561b0bf0ad39e3d`  
		Last Modified: Tue, 12 Nov 2024 07:49:09 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fa16f70538566b10dbb068814b0148bb3126bf49f5e2f7a00b9a0be1ef603b`  
		Last Modified: Tue, 12 Nov 2024 07:49:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6efa8cae11849435a411cb6ada33001d885d085d4fc01de0577687378d7ec6`  
		Last Modified: Tue, 12 Nov 2024 08:07:11 GMT  
		Size: 101.7 MB (101661513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcc226fbbd799d6ce264b67f4ad6299b83bad11ba06e7e09846edea9b890971`  
		Last Modified: Tue, 12 Nov 2024 08:07:09 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5d6d5d480e9043d8ee029d678abcbad3104e358be9d8d72af2d6ad2cce4ef8`  
		Last Modified: Tue, 12 Nov 2024 08:07:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7df53f66c24ea74e81a9950cdf948008a2fea7e1b9b0d77594aa2172065cd6`  
		Last Modified: Tue, 12 Nov 2024 08:07:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4aa20a8d3b02c5c23dae95635edeadd3aa9cec02ab03660e41aac8f82d145f`  
		Last Modified: Tue, 12 Nov 2024 08:07:10 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7015b6afa43fa8225e2d75de714c19b72baba60a3635e2d43bed08229d005ef`  
		Last Modified: Tue, 12 Nov 2024 08:07:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:ba40d1101cb4601a6c8fb50727bd3c23cc20c738557e75539fa14566d99b4f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3bd4a3a04ac7e60cb7200a3432f403d5d49a0608c32a719cf7349527ef6b0c`

```dockerfile
```

-	Layers:
	-	`sha256:55cc5bb36eef364e689373cb8a0ebf118cf8352e8d67f4a82b66710a413d0d35`  
		Last Modified: Tue, 12 Nov 2024 08:07:09 GMT  
		Size: 967.0 KB (967049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca0eeeecf91af7462a342961f39ae13f386d72fe8d562ad01f7debb8d554c11`  
		Last Modified: Tue, 12 Nov 2024 08:07:08 GMT  
		Size: 45.0 KB (44984 bytes)  
		MIME: application/vnd.in-toto+json
