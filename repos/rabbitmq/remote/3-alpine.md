## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:29833bf3b3a9936d851e91cee9697e6eb8fc399de6ad888607b722e943e46149
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

### `rabbitmq:3-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:f4ba893bc1aae14ac17cbc5a88d62601e4ae96f29e8b6385de481a77cc7ec5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74007186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211a3eaf72ae5b13a8ca853a1f6a23bc7c998b098f0b347571377c15334f045c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:24:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:24:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:24:51 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c3ba4c82ff490fa272d3760c50caf843df47099ff12d2fd11259f53bca7e31`  
		Last Modified: Wed, 26 Feb 2025 23:33:21 GMT  
		Size: 41.7 MB (41728904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa533d28a5a73745e2fecb3d973499f48fa919226fd59d1eaf10344cce2c1bb`  
		Last Modified: Wed, 26 Feb 2025 23:33:20 GMT  
		Size: 7.6 MB (7600319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3419d2ef6b7a1db30aa0cfb9823edffeb83ddb009291725b5b8ed5038dd3a56b`  
		Last Modified: Wed, 26 Feb 2025 23:33:20 GMT  
		Size: 2.3 MB (2277749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cbc02d62f70a7e407158bcd1f265234b3a7cb217a0fc7c874bd8e4de7dd2ff`  
		Last Modified: Wed, 26 Feb 2025 23:33:20 GMT  
		Size: 18.8 MB (18756225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54704e908263164a5d406cbe1247f692d463feb4b2cd38434d2a2048a3b0d18c`  
		Last Modified: Wed, 26 Feb 2025 23:33:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e1163cb8d1830ddfa22ec99b17ddb1c9b3bd1cabc2de900daf170588ceb2b`  
		Last Modified: Wed, 26 Feb 2025 23:33:21 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90c4b291e2ce3a0655a6267b22f82d7a2868072d49f8b21e5ff00b6e0d9cae`  
		Last Modified: Wed, 26 Feb 2025 23:33:22 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3563992d595a28ec8da5f84d578ea1bef2d56bc2eea005bd1dbb65a0664c29fc`  
		Last Modified: Wed, 26 Feb 2025 23:33:22 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:baf59fc935f61a2a853cb3b40a47d3e8be6bf02af7ac8b565819d918968713f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6457292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f51e913c0bcdf0c67a852b509e455b0655b301b8af8e977a7eb600925846af3`

```dockerfile
```

-	Layers:
	-	`sha256:3a85c19ccba81691f55ce40c1cb4b62bdc1e6fe654d4642eb003f23d511a87cc`  
		Last Modified: Wed, 26 Feb 2025 23:33:20 GMT  
		Size: 538.0 KB (537954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc2b1f73230b1b0bac66a09e0e1eedcb2675e3fff7354de87764cb972e08a72`  
		Last Modified: Wed, 26 Feb 2025 23:33:20 GMT  
		Size: 2.9 MB (2931975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6cb596d80fbe5c29e5d76106c31531cc318bd88817b1f27f2ed5c45e26b4a2`  
		Last Modified: Wed, 26 Feb 2025 23:33:20 GMT  
		Size: 2.9 MB (2927783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94528c7b02fce2f38561d2ccd2654dc1a31d1551704f393b076639a9ea891243`  
		Last Modified: Wed, 26 Feb 2025 23:33:20 GMT  
		Size: 59.6 KB (59580 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:51b344009937af6b6448768e6918033c14f4683394baea03a2adcd125206d075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63060777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa3daa0cca85f908e2f6d7c82fac1c3373703dba9bbb6fd80b4d1abc0a39f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:24:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:24:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:24:51 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e762405ba07362b00dde76a8b30241c0ceef318642b85ede3b73cde203341c6f`  
		Last Modified: Thu, 27 Feb 2025 01:59:31 GMT  
		Size: 33.3 MB (33287454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd1472c7e01af7835f8cf603c6fc1c77ec14a4bdb8f6ccf00d8f5df8dbe7df`  
		Last Modified: Thu, 27 Feb 2025 01:59:31 GMT  
		Size: 6.4 MB (6425488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65bd3fe2f9acea8676a91e49dd13454316722bc2dfc4dd962d0e5927d379173`  
		Last Modified: Thu, 27 Feb 2025 01:59:30 GMT  
		Size: 1.2 MB (1225218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8962db85d89dd184614db94dcfaaeec8d17a77e2af1589a73a049f4148489b4`  
		Last Modified: Thu, 27 Feb 2025 01:59:31 GMT  
		Size: 18.8 MB (18756139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038eef65b444bfec17367af0d06af038f1869d89773c233653fa7dd5eaf7f7ee`  
		Last Modified: Thu, 27 Feb 2025 01:59:31 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96b278a7a7b3f1577d35463d1a35f869789141381f9a2f0909c4f5cd091880c`  
		Last Modified: Thu, 27 Feb 2025 01:59:32 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9ae56197ab16f8986ef05e9e2a587b9c7ee19cca30a6482320c468e2ae5cd5`  
		Last Modified: Thu, 27 Feb 2025 01:59:32 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47109e2997fce223334983aa870abb89ad78a361c953c5330c044408a71a8d15`  
		Last Modified: Thu, 27 Feb 2025 01:59:32 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ad881f1c7b845c20698974d842c1d1fa2cebb2ded2a46fc3e6c1c0f243919cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 KB (59550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fbf5528f14b3963d5d765d2ad52cd94e63303c790ba09f9636a1a4a7bf8fdf`

```dockerfile
```

-	Layers:
	-	`sha256:8416214b58acf53aa96c28e939c4db4d0f50f498f4a7ab693785cef706a5ae6f`  
		Last Modified: Thu, 27 Feb 2025 01:59:30 GMT  
		Size: 59.5 KB (59550 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:02b174a7b1b985574f486bb7e8f93fc7bc7a244bf7dd1f45e17336dcfad10b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62333115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3de47e548034d947dd7e0efb1aceb4f0df66f43eadcb840433ba97fe8af2a88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:24:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:24:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:24:51 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2a7ab3c866a06d2f75a5be51bb9d42966abe2ef4e2fee8ad8e160f98fd4fda`  
		Last Modified: Thu, 27 Feb 2025 02:18:41 GMT  
		Size: 33.2 MB (33218721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a392f75fd4f4603986ca90a983c72e10116ff854619cbb07c312ffb9944d85b7`  
		Last Modified: Thu, 27 Feb 2025 02:18:41 GMT  
		Size: 6.1 MB (6125510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3df7d6f02bb57ab94d14e8d38d69250659ccc0006f78f806bf3a3e839bdbc7`  
		Last Modified: Thu, 27 Feb 2025 02:18:41 GMT  
		Size: 1.1 MB (1133032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e550d4fb02c91611ff53e5ffb788f68a941b91afdde8f547dbff0d0eed2101`  
		Last Modified: Thu, 27 Feb 2025 02:18:41 GMT  
		Size: 18.8 MB (18755989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d81e93ecc6799b259e3628a35e8d03ea3372b2a5582c0a252ebc7c22f63cf8`  
		Last Modified: Thu, 27 Feb 2025 02:18:42 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7567583c82773f41dcdbdd44e199749c708aecc828b3660c8268cf3b67e7b42e`  
		Last Modified: Thu, 27 Feb 2025 02:18:42 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32020eaf527cbbd8487a843b3211189f01c1768014454c2dd1abb8ab68a99aed`  
		Last Modified: Thu, 27 Feb 2025 02:18:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913f7b20824a54676312a03c1ed28c1cd88d18680f989cfe1286e8eeb2945ee9`  
		Last Modified: Thu, 27 Feb 2025 02:18:43 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1fa5bfffac853877eeb50824a882213701f1bb5b2fb79998b17ac2268fd7db4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6492234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc66f1b302b83b1e9b7c20e29f6bcada75e5f484d517ade7cdf17f65a1ec8009`

```dockerfile
```

-	Layers:
	-	`sha256:a362f841fa956598f5b0e293dfe859050e7f1d7167cd79f078d8235d2c64ab89`  
		Last Modified: Thu, 27 Feb 2025 02:18:40 GMT  
		Size: 651.2 KB (651213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f4cdb0cb1eddce530a214697b822503ecf4cc38821a14e18bb03cfd6ea4649c`  
		Last Modified: Thu, 27 Feb 2025 02:18:41 GMT  
		Size: 3.0 MB (2968952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9efdb8d0c7ebd9e3f45733bcc4e20b610d26c0240103a80623d87f9c53b60573`  
		Last Modified: Thu, 27 Feb 2025 02:18:41 GMT  
		Size: 2.8 MB (2812304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13b0fa1955730d10b7e66cc3271ee5c2715401630ba7039453ea1132a50c776e`  
		Last Modified: Thu, 27 Feb 2025 02:18:40 GMT  
		Size: 59.8 KB (59765 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:0de37aa7974dc8dac8f23c65f37fc9452d90f4c72b12c8aab26e10d2013909be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72232811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecb3a50f68209376f79bb7e63d86d91f1a1e991f9bf8a74c5a289b7b543dd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:24:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:24:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:24:51 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e3e7926d2ba9924709d59d8eb6432d781f6b3034719e0ec466885f8c2b4e9c`  
		Last Modified: Thu, 27 Feb 2025 00:51:20 GMT  
		Size: 39.9 MB (39918992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39f6f7a5d9864db9a719a307a961344541d51f88005071a46eba1bbe8183b5`  
		Last Modified: Thu, 27 Feb 2025 00:51:19 GMT  
		Size: 7.2 MB (7240535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f592aaa908f1ab29455066fa8bc9dd39e2116b054ff2e93aa1307f1e2a07f20b`  
		Last Modified: Thu, 27 Feb 2025 00:51:19 GMT  
		Size: 2.3 MB (2322444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b823711668285f1478bb87eb2a0870aa09b0357729ad2826425e48fb1c680b09`  
		Last Modified: Thu, 27 Feb 2025 00:51:20 GMT  
		Size: 18.8 MB (18756068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe97b89945f814631ae140776785e39a60821e5025d9e5d5a6528cadac617ce`  
		Last Modified: Thu, 27 Feb 2025 00:51:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a1732ff398a56afb79e0dcdcf90b0450f4465d888af3cb7aa9ac7c22364109`  
		Last Modified: Thu, 27 Feb 2025 00:51:21 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b673004a6d3ca550026d00aae41e65bb81f46c4631f35055011868cab63ee6`  
		Last Modified: Thu, 27 Feb 2025 00:51:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3d62ceca08a18c214ee76e254dbaf8ce6587373470c76d03115052b1c7d6d4`  
		Last Modified: Thu, 27 Feb 2025 00:51:21 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c18a8c2b904c9326b8dd584a066f6e0e5d1da724a21aa0cdaf30d3593c32e166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6834826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d485e9127bdfaba830db7e2244ef1c5b55e122848b987eef2f70ece016dd306`

```dockerfile
```

-	Layers:
	-	`sha256:67b6e47b98508b28b8200085f422b1eb21da20a83b75dabc6bc0480b11e9b385`  
		Last Modified: Thu, 27 Feb 2025 00:51:19 GMT  
		Size: 655.9 KB (655855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1ad65caabe2ccae6300bdb97bcb72574f8ba9e924e37a95f391b96565e89792`  
		Last Modified: Thu, 27 Feb 2025 00:51:19 GMT  
		Size: 3.1 MB (3137903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1c6621f26df9a1051bab2abd298af4532186d3dc2e0081e9deaca873650e35`  
		Last Modified: Thu, 27 Feb 2025 00:51:19 GMT  
		Size: 3.0 MB (2981261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dda22cbc0591eb364aaa60042c4a25c57e033f9b17fe104e5cdc126aa985e55`  
		Last Modified: Thu, 27 Feb 2025 00:51:19 GMT  
		Size: 59.8 KB (59807 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:6f5d315c451bea86cbfcc2a35e6531bde9193b5310b8ad48c91990038f77e6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64334751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9629975c657c6918cb99403c0d9d90ec12389d2f05025165eb4f13eeb6be0ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:24:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:24:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:24:51 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846a61db97a028a8eb7be565fcb194606f50e1f304c0d3682945457c95517ffb`  
		Last Modified: Wed, 26 Feb 2025 23:33:27 GMT  
		Size: 33.4 MB (33375032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8009ba510fbb1c6c935ebbe58b3bbb64dd67f8930c46faeb3cbe6a845f5f12`  
		Last Modified: Wed, 26 Feb 2025 23:33:25 GMT  
		Size: 7.5 MB (7509079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8682256898ccb5cb2fa74bb79e4c943bb2b07140d0e8c595e5f8c27f81d07e8`  
		Last Modified: Wed, 26 Feb 2025 23:33:25 GMT  
		Size: 1.2 MB (1229263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62be01e0aa13a7423838d8d76cc750701f1fb2781f0af6e81a3e8332179d13e`  
		Last Modified: Wed, 26 Feb 2025 23:33:25 GMT  
		Size: 18.8 MB (18756007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304bcda23a5201bde01c96083da460e00c58611e18b38a1e70a3133cab5a2b14`  
		Last Modified: Wed, 26 Feb 2025 23:33:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591dd62ff8cfc8ffdc6f3f982da61d67ef5aa047a3c1fcbdb9a31e507cb78f34`  
		Last Modified: Wed, 26 Feb 2025 23:33:26 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d810a423a9ef6d6a38025b0d8daeab26d75aadb72f6a77a58add9b552d3883`  
		Last Modified: Wed, 26 Feb 2025 23:33:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d0d8e2b04cb0026f3d8855cb978cc09c0335c5a62d7c6ab317a7ec2d7742d9`  
		Last Modified: Wed, 26 Feb 2025 23:33:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:197d78c7d3878af7183b348bc7384788cb32120a68df497b04ab140a9221e241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c09d9c0f2628ab8e1d507d033a1f466ca377c5e19540ca3e8e48b29bfb603a9`

```dockerfile
```

-	Layers:
	-	`sha256:f19b9b80bef39fcc8e5a263d4442cfd6149e40765bd1d731b4439d6e0d198332`  
		Last Modified: Wed, 26 Feb 2025 23:33:25 GMT  
		Size: 533.3 KB (533308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec218ad15130911b549ec89f2b43b271200829eb068af5b080915bb0956efe5`  
		Last Modified: Wed, 26 Feb 2025 23:33:25 GMT  
		Size: 2.9 MB (2920926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b2f2506cc2752899bff92749e37fd12859ec6eec32af167080b3e8896bb2ff`  
		Last Modified: Wed, 26 Feb 2025 23:33:25 GMT  
		Size: 2.9 MB (2916738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7718c828ad75fa8fdcdcd14a838bcd06cc4537ca35232d63673f596d294fab30`  
		Last Modified: Wed, 26 Feb 2025 23:33:25 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:71ddeb9af6323d3121e1dc66619fe7f09eeecf0caebe8d0a047cc739fd422038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65430821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76224bbce6f28a543dbb9416f709f0171d2b6dd94764caa3c00ca58f0dd82c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:24:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:24:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:24:51 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4a743322bda01a0acb93a91ad24dcb0757a72193cb022eb2d013f6e202391e`  
		Last Modified: Thu, 27 Feb 2025 02:58:07 GMT  
		Size: 33.7 MB (33749786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80ffda4f1b98cfec136bd204475efb0c0e3047ca41b00250bc0af2e01f6e5fb`  
		Last Modified: Thu, 27 Feb 2025 02:58:06 GMT  
		Size: 8.0 MB (8003854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab2120deb3504f464e74d8e95c5e7e871b3be9fc57f219d6665e89ddec8380f`  
		Last Modified: Thu, 27 Feb 2025 02:58:06 GMT  
		Size: 1.3 MB (1345003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403145a39e0292c315d268623a75a3951564d7d9138510ca378dbbfcdbed46d2`  
		Last Modified: Thu, 27 Feb 2025 02:58:06 GMT  
		Size: 18.8 MB (18756074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bee458508c5962c8b661b9f6e132ceab0b6393e7d1f1b4810c8c499da5d1c1`  
		Last Modified: Thu, 27 Feb 2025 02:58:07 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b75f4c88bdf98c45077a6915fea34611a5292d1470bc67faa32a42bd0287f1`  
		Last Modified: Thu, 27 Feb 2025 02:58:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc911bbcb2e8222bed832b39a4f3a11f7ded614a420e17d36c10b424df396b`  
		Last Modified: Thu, 27 Feb 2025 02:58:08 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ba90502dc5acb4eaba9eff990db0f8575c6d13f30ba7ec9758b741fbd1a21`  
		Last Modified: Thu, 27 Feb 2025 02:58:08 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:34d52c74892ae2fc7267ff307cf49cb63b2e43ab91bdb1becc426ac6a99287c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6730520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7d6cdb581d3b3347c87960c908fa02b903094db5ef97b65da3cc0064db988d`

```dockerfile
```

-	Layers:
	-	`sha256:a09454023b9047120755be75a99ab6159dd93158c8c43e76cb89209e6f782774`  
		Last Modified: Thu, 27 Feb 2025 02:58:06 GMT  
		Size: 649.3 KB (649262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d220a8afad059c4bdd0653d18d01e6af5dae44442a4ade127161391afdd02c7d`  
		Last Modified: Thu, 27 Feb 2025 02:58:06 GMT  
		Size: 3.1 MB (3089138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d781a1933450626e1b09de70c23a4292f79716eb3c5e691e1ee7e36fb1696b3`  
		Last Modified: Thu, 27 Feb 2025 02:58:06 GMT  
		Size: 2.9 MB (2932484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8eb37b6bad2a8d7cb9e197e0bb649505d8076af41f048689d1bc0dfa768f7b`  
		Last Modified: Thu, 27 Feb 2025 02:58:05 GMT  
		Size: 59.6 KB (59636 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:7715a5a76cfe410cf892fedcf1c677bd38b2474734defa3c60c60476150664aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66834173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9997209ff12b9473f8711ed9bae4f66caaba9a8eea844a6a2ddaf9d946fb8afb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 12 Feb 2025 18:05:13 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 12 Feb 2025 18:05:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Feb 2025 18:05:13 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8ad515b7dc9624a06b7514280f58f06ad8d717a3f2b30f42f9a3d955e8ea89`  
		Last Modified: Sun, 16 Feb 2025 13:31:01 GMT  
		Size: 34.7 MB (34699412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921e98cc3a756c5000198f46a80969859cd015e2639ef5516d6f97322d457b99`  
		Last Modified: Sun, 16 Feb 2025 13:30:57 GMT  
		Size: 8.8 MB (8760499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b222a479df1ba45b322fcd884348f77b514551e327f9b28aa568c10cc3f7e7d7`  
		Last Modified: Sun, 16 Feb 2025 13:30:55 GMT  
		Size: 1.3 MB (1264902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc4a06140e93d8b9a141f941186c712e4828f4c4833b22e58dbbdc453569919`  
		Last Modified: Sun, 16 Feb 2025 13:30:59 GMT  
		Size: 18.8 MB (18756162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1b8f44014ff20330c3df475f141e2dbece708cc32841b72d3dd94ee44791b2`  
		Last Modified: Sun, 16 Feb 2025 13:30:56 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388d37a8eb0727b858fee5e714ff818c06c8719217acedd7ed7732b9089de6e7`  
		Last Modified: Sun, 16 Feb 2025 13:30:58 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e61c6705fa826ea2f669b26c2d8d1a44124da52fb37258bfe5050cc8503928`  
		Last Modified: Sun, 16 Feb 2025 13:30:58 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07b5dac4e41f71725a92408a3d8424c31ddc0292417633d8c23235328933d6c`  
		Last Modified: Sun, 16 Feb 2025 13:30:59 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:890b6f0767891fb656cfe2ea69cb872925070d64852a5b292d70bcb8bdaf56d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6808634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62834e7d464f2517694e1297ba6191ea27d3fc919cd33074e9a3394c0626b75e`

```dockerfile
```

-	Layers:
	-	`sha256:6fb40d6e4a0deea97f4fdaebf1cb4a684857832a931ecda9c676c243e72d10e7`  
		Last Modified: Sun, 16 Feb 2025 13:30:55 GMT  
		Size: 652.1 KB (652054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab9983b383156ddceee5bb5ece0a4572232cca6b98ed4838a8c2cc5e5b80fa8`  
		Last Modified: Sun, 16 Feb 2025 13:30:56 GMT  
		Size: 3.1 MB (3126793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37acfdf1da92a521993de7c4882189b47b5116b1ccceada34a9e4c418343ac84`  
		Last Modified: Sun, 16 Feb 2025 13:30:56 GMT  
		Size: 3.0 MB (2970151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2607a1739b0347f3cbd35dccdbc35aef0f5786e296b211237a3713e313bfa889`  
		Last Modified: Sun, 16 Feb 2025 13:30:55 GMT  
		Size: 59.6 KB (59636 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:60c2de35c1ff49be3216a1f6fd997eb5bfed6e3ba5eb146c9a535776d135f055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64073106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1a48960a8b1d27ce370e73e7d0a1adccde37b81203baf277fed5f2488b000c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:24:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:24:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:24:51 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:24:51 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:24:51 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:24:51 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:24:51 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:24:51 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac6b8d0b5d7289bb292a2646fd0fce962f0871780bda640e922aa07934e6e53`  
		Last Modified: Thu, 27 Feb 2025 02:08:13 GMT  
		Size: 33.8 MB (33779189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec5fc71f3a8089a8d173ad9ba042459ccf045d9ffbc4c55ef98ee66e66a4f91`  
		Last Modified: Thu, 27 Feb 2025 02:08:12 GMT  
		Size: 6.7 MB (6745398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c82c25f6cc3318e6a77afb899390ada59d019901440cca454bb89dc6b7a03d8`  
		Last Modified: Thu, 27 Feb 2025 02:08:12 GMT  
		Size: 1.3 MB (1323208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd08179877f003aeafa14c2d5a87e17e1d00aa146520a6484d5a7112809268`  
		Last Modified: Thu, 27 Feb 2025 02:08:13 GMT  
		Size: 18.8 MB (18756000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b261a77c8c1701e98b273e40a54869151876b2a4d615d69cb70828d6fda7fb76`  
		Last Modified: Thu, 27 Feb 2025 02:08:13 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558855e983e9e1be6abd7fd29e12cfe171cf80c1a11bc65900c9b2f35b4cb3e7`  
		Last Modified: Thu, 27 Feb 2025 02:08:13 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8181bc352668d9341ef7ea70145754976e981a0caa199a3764d2a7d57787ad50`  
		Last Modified: Thu, 27 Feb 2025 02:08:14 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa0887eed9755c704bc100c52c82ad37875272e71a83207807b7cfdf401d1ff`  
		Last Modified: Thu, 27 Feb 2025 02:08:14 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:99273dec43d3c198e4d44888f742bf2f310c23026938490d98c09526e7d44e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe47dbc70a924ac0c68de81570630e56d5d9770ff2a945c2631926f14fcbbd0`

```dockerfile
```

-	Layers:
	-	`sha256:7adbc22ac26fc53b78d9c87d434f919af295e7b9a48a5ddb55803306b11e35ea`  
		Last Modified: Thu, 27 Feb 2025 02:08:12 GMT  
		Size: 649.2 KB (649234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3544aaea4aa2cfc5a723affb5f412d21c3e884a6335bb3d097a64c24bd274b`  
		Last Modified: Thu, 27 Feb 2025 02:08:12 GMT  
		Size: 3.0 MB (2979111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92384a50f03e37bfd0445435a12d5bda98dd4e0a52ccbd243642239facdb3263`  
		Last Modified: Thu, 27 Feb 2025 02:08:12 GMT  
		Size: 2.8 MB (2822487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db900aec72913b3e085625b5dd32db52e334efc322b7060cd127169efe5aa41c`  
		Last Modified: Thu, 27 Feb 2025 02:08:12 GMT  
		Size: 59.6 KB (59580 bytes)  
		MIME: application/vnd.in-toto+json
