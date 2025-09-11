## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:11daaf0df7ab74ecabe704140f3ab49b54b5e658258382125aebb158969935fd
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

### `rabbitmq:4-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:8ba5cb752b25098a8563f5375045598eb7b1efbe4e5a5e43ed9a61d61a51f37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82014920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c1123c45546fd44c457310cf8534fb9d1cf0f6f29c526a31ca97718938c427`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:55:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_VERSION=4.1.4
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:55:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:55:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5664d5717dd875b555d9697c90d7b6a6823aa66159a64d19f9ef5e0245a87955`  
		Last Modified: Wed, 10 Sep 2025 23:41:05 GMT  
		Size: 42.9 MB (42855947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a620a0bc4c79655be53a383db422f1d1686f63a4fd733b2fe87fd642f355ed`  
		Last Modified: Wed, 10 Sep 2025 23:41:06 GMT  
		Size: 8.3 MB (8314157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27241e6b0524679469ece5b801e5502596258b456001d41cee517cf993cad31`  
		Last Modified: Wed, 10 Sep 2025 23:41:02 GMT  
		Size: 2.4 MB (2374058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ec9c8ea25eb97dc4a5268f4f46d2a53d460bab2785c61fc26a50cb832b304e`  
		Last Modified: Wed, 10 Sep 2025 23:41:24 GMT  
		Size: 24.7 MB (24669323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b62b20297637f65b2582ea7ed802475072731eed8b918b1afc8adcb8d52982f`  
		Last Modified: Wed, 10 Sep 2025 23:41:03 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e7b7bc14aa596b6e7d48f1e00b0808e853243c736dc821ea7105661d338eb9`  
		Last Modified: Wed, 10 Sep 2025 23:41:03 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109e2207467295090142e32d220133e2331e3a0cd4853002933c57c44d53ed00`  
		Last Modified: Wed, 10 Sep 2025 23:41:04 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67d4d2812fae0e29eb3844735d836c85e0b96ee21b076bbb01f1a9bd657b8c7`  
		Last Modified: Wed, 10 Sep 2025 23:41:03 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a999b1a46cae0a163f22ce7f91bf420d03537ac4f8ad08c937a81b8232c414bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6783142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5ade35a9520de8c57bb917fa7dd33dd095f20e04b30037c473134b86a6b4cc`

```dockerfile
```

-	Layers:
	-	`sha256:cd05213ad24c9d49dfd022945645a799ef074985168f10bccd60e9a68dc303be`  
		Last Modified: Thu, 11 Sep 2025 00:54:01 GMT  
		Size: 671.4 KB (671350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0855e4632befe150c04149f892e0a6f70104525abdd77164cfb6181d50c95399`  
		Last Modified: Thu, 11 Sep 2025 00:54:02 GMT  
		Size: 3.1 MB (3102698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935dbb5d99c30eeb78c96535de0602bfa1e12cf1cf1cfe4676039833f9be709a`  
		Last Modified: Thu, 11 Sep 2025 00:54:03 GMT  
		Size: 2.9 MB (2949137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6a6abdff324d3c4440c61d7b21eba4d99fd2a08aca10118cf3e92389afe82a0`  
		Last Modified: Thu, 11 Sep 2025 00:54:04 GMT  
		Size: 60.0 KB (59957 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:7e4c131b92bc69d449c3e3bdb46849f99dec584efc5c9a4fba51796c8e251aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70048182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d70805edadc534f1fa89e3b0b1eaba337947496e8bffbfa53928dde587dcd33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3be4fe3b50ab512a8ec703b54df0cb101d900e2c30c5d42027e2a44c8b27cf`  
		Last Modified: Thu, 17 Jul 2025 21:44:30 GMT  
		Size: 33.4 MB (33446070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e42e0de7fccd3307047296469cb5f9c9aa2b44e3cf60cb20e759cbf1005ff0`  
		Last Modified: Thu, 17 Jul 2025 21:44:28 GMT  
		Size: 7.1 MB (7100801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8772a75c3b551a77ce5065f3d0adb0bfa846a523d3405c6f8bfb05352bfd7f65`  
		Last Modified: Thu, 17 Jul 2025 21:44:28 GMT  
		Size: 1.3 MB (1329814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04a7720934ab19063e7323ad9fdaf2aadd908fccf3f5b03ec25d6cf56355b56`  
		Last Modified: Tue, 02 Sep 2025 19:07:08 GMT  
		Size: 24.7 MB (24668842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c67ea256a8d814a9e7a3f54a00afddf4a74ed89884f4727b2e981303636160`  
		Last Modified: Tue, 02 Sep 2025 19:07:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2d55899cdff9033e69c56d68abd818b9859aa10530570a17d3768272c7b729`  
		Last Modified: Tue, 02 Sep 2025 19:07:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9de00fb6c30ed0e71c4fce90ed222c9c66f2989127688fdcf2aa23ad406222b`  
		Last Modified: Tue, 02 Sep 2025 19:07:02 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f674bb720418e8d0734252e597f1f7347f462cdf86895e34a4bc5215ca9fbe4a`  
		Last Modified: Tue, 02 Sep 2025 19:07:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6097b50e875c648a46a5bfec88e3fb2d12ca6f52bf7b89e97dd40d52529aa4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f9ba0a7b5a5050a6798ece22330759588dbada0974b69042580e72767877c3`

```dockerfile
```

-	Layers:
	-	`sha256:33352c246ce3bc0541602c84ba5a1c6b9710d042d74114b47805af34d01ad308`  
		Last Modified: Tue, 02 Sep 2025 21:53:26 GMT  
		Size: 59.9 KB (59934 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:b40864fdcf2fd2f942614a97e8be0b04ad4837316fb0e0139d00f5f3d9f51442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69233978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60d83cdf35d669c63864b75d1990c3a64e2b4628bfa020d6a835a5d01c6327a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3e679d2d0ec7b1fb48080f6efc7bda79a7b95ba445c6df26a125283cd01709`  
		Last Modified: Thu, 17 Jul 2025 21:50:45 GMT  
		Size: 33.4 MB (33370909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41015ebcf72a938e41753268064bea0279729fd19f88886b54fb26e816a6a2ff`  
		Last Modified: Thu, 17 Jul 2025 21:50:43 GMT  
		Size: 6.7 MB (6747046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e7d05f7d5f0a96e96248de788396dabc6eddc9358fb2e96695b9fa8ae3524d`  
		Last Modified: Thu, 17 Jul 2025 21:50:43 GMT  
		Size: 1.2 MB (1226708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7706e3143ce082615155b805036078096e5c287cdb827eb3ce8ae8dd1dd735d1`  
		Last Modified: Tue, 02 Sep 2025 19:09:47 GMT  
		Size: 24.7 MB (24668533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1590ae5e7298462c2239249a042830d966f18c2f6712d223300b82a42085ea59`  
		Last Modified: Tue, 02 Sep 2025 19:09:40 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db17130e1ce2d2f8e8dfaed127365f755ac69587a57e5d1060f4f4e37644a90`  
		Last Modified: Tue, 02 Sep 2025 19:09:40 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0f0a7132c4d7152e9dc2e14b2bb25fd7770c176cadc4d92c6495c207024d8`  
		Last Modified: Tue, 02 Sep 2025 19:09:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4ca69b403e4d1b01394478c738d252d5c47be0d1d8166cd96ccf58605678d1`  
		Last Modified: Tue, 02 Sep 2025 19:09:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7db942bb6971169ad175063e58dbdb5c612af0c52cea1bb10e04843803c858c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6547413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819adc946e3083c6239004e991824b59dcb980515e30c52fa19408b55d9e75ee`

```dockerfile
```

-	Layers:
	-	`sha256:a7ca806da14ba25926778b2dca47fb80cf53a1c871ed97b4368c92dadb60a91e`  
		Last Modified: Tue, 02 Sep 2025 21:53:30 GMT  
		Size: 667.1 KB (667131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0d3ea857c49bc94b77664ab6489c091ff2829793f0609fa3be5ad4718c38f0`  
		Last Modified: Tue, 02 Sep 2025 21:53:31 GMT  
		Size: 3.0 MB (2987501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0611b2e6b53f224669769cf0812cdd2376e736f9729af4ace11bcc5dbdb965`  
		Last Modified: Tue, 02 Sep 2025 21:53:32 GMT  
		Size: 2.8 MB (2832631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7adf47df9cfd12e6a67661c8df958f07bfa70cd3a02fd243d1484a3c1e45ff30`  
		Last Modified: Tue, 02 Sep 2025 21:53:33 GMT  
		Size: 60.1 KB (60150 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:373f803600e6ad9a672b5ac6479a9a2202e2f7abcae5836a85d3eb56ee659e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81110251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9dcc668d2a55eb55faa99a39daf19e56f01f30c8d59350e117033e5bce2b9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:55:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_VERSION=4.1.4
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:55:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:55:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09262237a103e5f87b6338638f0a245cde127adac29219fa1c22aadabe430bc7`  
		Last Modified: Wed, 10 Sep 2025 23:42:57 GMT  
		Size: 40.8 MB (40845827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60759e0ad350de2da0812f5e986572445bdde4946e1ea08325aa8f35c152a1e`  
		Last Modified: Wed, 10 Sep 2025 23:42:42 GMT  
		Size: 9.0 MB (9037844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e050a6bff7fd97681a5db6419e6a2ea6afed9be634038a21e8ee7b532b73196`  
		Last Modified: Wed, 10 Sep 2025 23:42:41 GMT  
		Size: 2.4 MB (2424749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59b783e1341300e1eef8a1ff23acbe55b06b46607b416d6c99aa75025598509`  
		Last Modified: Wed, 10 Sep 2025 23:42:47 GMT  
		Size: 24.7 MB (24669335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72aa33d61b4601fb0587dac493815484ca6469a472af1e533ad12e1a3eec04f1`  
		Last Modified: Wed, 10 Sep 2025 23:42:41 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f386fe716f01d5e85e582b0b1ed0c2b09820e9e0c5beb70cb80416945317a73`  
		Last Modified: Wed, 10 Sep 2025 23:42:41 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea62325934b53174b650598c5104e5c62807d16d5f71db426fd2bb36f757e56d`  
		Last Modified: Wed, 10 Sep 2025 23:42:41 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5114e6474f92ddce054816bdb8d2b4c5d1c6ea9e1b26bfce52fbe42727f0e012`  
		Last Modified: Wed, 10 Sep 2025 23:42:41 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f9e2309379d5cef7bc8f21c94d2ba6a4fde720c1545cc96cddeff58b0c2d10de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6891447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329fa28551199abf9f188e717c9b916f851f7f2323f35126ae7bd085ad8dca75`

```dockerfile
```

-	Layers:
	-	`sha256:d92f45dfbff32a9595890b1784b0176dc3fd5371424ecfbc196cd0574d9f45b6`  
		Last Modified: Thu, 11 Sep 2025 00:54:15 GMT  
		Size: 672.1 KB (672143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ced7f8457e34f813e88fca912306e8001d0cb28611aecbf8f1018e27f61df2a`  
		Last Modified: Thu, 11 Sep 2025 00:54:16 GMT  
		Size: 3.2 MB (3156996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c7c8a7dd6196bc17ccd44e39eed3b8c79ee991dbcce01bd19c039840fd74b2`  
		Last Modified: Thu, 11 Sep 2025 00:54:17 GMT  
		Size: 3.0 MB (3002112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e2b9296babe60dc90549b7d36754704a920c0f7ae32c8bf3310867bdf4cb56b`  
		Last Modified: Thu, 11 Sep 2025 00:54:18 GMT  
		Size: 60.2 KB (60196 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:f3d51b1a58c371c0fe31e55e9edf6b5af068701d6d868008dc4b858d51f0fc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71487850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3cddd0daf3fab3c01656bf2b10de59bd2e6153f9c02f96050da20e10e19ecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:55:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_VERSION=4.1.4
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:55:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:55:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85324742d3c98c0a5b411a073738beb787b4eee9d9831a71477b2c228a4108d`  
		Last Modified: Wed, 10 Sep 2025 23:41:11 GMT  
		Size: 33.5 MB (33542852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd8a106253f7c6f284d0a0363bd934ae4bc7f6869bfcb41759aae8409eb338a`  
		Last Modified: Wed, 10 Sep 2025 23:41:10 GMT  
		Size: 8.3 MB (8327291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcbd7ecf6f0478c237a48e858ce4613723b466de2b7d2a3fc2e4ddfac39ba0e`  
		Last Modified: Wed, 10 Sep 2025 23:41:09 GMT  
		Size: 1.3 MB (1332265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529657848d670bd336403e8a4e62570185011a071ca014c247babc6141578757`  
		Last Modified: Wed, 10 Sep 2025 23:41:12 GMT  
		Size: 24.7 MB (24668691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c5e6fa4da95aff114f878f977ec0f1e085baf479ef6dbd0013ce8b21c44044`  
		Last Modified: Wed, 10 Sep 2025 23:41:09 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677999a141c5dbf1d52a54f32a6a563627f008b00f8ae9a05f20b8df2bfb48ea`  
		Last Modified: Wed, 10 Sep 2025 23:41:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fd7ae28b375d35c71f8b15d87aa812b8fa473da3b2a161ac269757cd39358`  
		Last Modified: Wed, 10 Sep 2025 23:41:10 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e68df27e99fe840b914af04b80726e442fbc463678b7e22b317027ab5aaecc`  
		Last Modified: Wed, 10 Sep 2025 23:41:10 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a3c1c627daa3a54bc0e7f9dfccc7e21741b26cc8aeae0a7cf951bb8fab6ca4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6755983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41758081f2226bf5d8d8184fd728683073020474b66e6ae0ec3121c1b55607ff`

```dockerfile
```

-	Layers:
	-	`sha256:847a35279f732056ba65f658b9131806e8193ee696de85692aa12eaa2427b9a0`  
		Last Modified: Thu, 11 Sep 2025 00:54:23 GMT  
		Size: 666.3 KB (666345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aac8c19ad897be9e617517a77ecdfbd19f579526bc89b0249b7fd65e0ae1f1`  
		Last Modified: Thu, 11 Sep 2025 00:54:25 GMT  
		Size: 3.1 MB (3091644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b0830c24fc0fa66d4801391547475d2dd26a9993a719fdf70689bec0fe7b4b6`  
		Last Modified: Thu, 11 Sep 2025 00:54:26 GMT  
		Size: 2.9 MB (2938087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d7ccbd23b4d1113a53e380945ac4fcd5e56b7a34b71388a8cc685001bc29b7e`  
		Last Modified: Thu, 11 Sep 2025 00:54:27 GMT  
		Size: 59.9 KB (59907 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:bb32eaf451c3997ecce10d60917219312e88599508dc47e244c0a489f4ac7d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72624949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffbdb935b21d031e29d2e30a231715f90cd1fc35bc399b31349fe238ec16c08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:55:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_VERSION=4.1.4
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:55:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:55:42 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:55:42 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:55:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:55:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:55:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:55:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:55:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe763b475b9bfef88543aaf2a9a47d9b91f9b0122888d1bab08db00e2698ee9`  
		Last Modified: Wed, 10 Sep 2025 23:46:46 GMT  
		Size: 33.9 MB (33925746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5d8fa46cf74118b53f4710107c57dbcb3c2cb2f2c8cccfc138d2c4a2555fbc`  
		Last Modified: Wed, 10 Sep 2025 23:46:44 GMT  
		Size: 8.8 MB (8849182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316ce3d828d8209107cf840282d095ca9c2df228ea5708f13280504008977b41`  
		Last Modified: Wed, 10 Sep 2025 23:46:43 GMT  
		Size: 1.5 MB (1452385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc2bd0c40f9b402883d78b18115c2936f63a1e766fe1772f554493e51c9be22`  
		Last Modified: Wed, 10 Sep 2025 23:56:55 GMT  
		Size: 24.7 MB (24668770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7c2d72bfa4145d9f0d13829daf715972b3de77fc4464967efb110fd833d6ac`  
		Last Modified: Wed, 10 Sep 2025 23:56:52 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1b5a501c7f34312423fba57d73364420aeebbd51390673e226021eef6aa6b2`  
		Last Modified: Wed, 10 Sep 2025 23:56:53 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8fc2d107719d4f6a02f67e68ca0189e2cad007c21a36cc6d69dac47d8b0627`  
		Last Modified: Wed, 10 Sep 2025 23:56:53 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64549fdb9a7380690488e7a3918a54549be091c02ffbb5ef8037e378aeccc07f`  
		Last Modified: Wed, 10 Sep 2025 23:56:53 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6b329adfa518a56c43f38683db757fb023e62c1be57a825f2912ef19fa2ca7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9db1ffcc11adca03a7b59e24d909b2e48e16a3ff9410113ff16f98ebacc990`

```dockerfile
```

-	Layers:
	-	`sha256:4f7860dcdfb39487d8a0052b24fedd8413b477e3e77a7ddabf45f784eec7c140`  
		Last Modified: Thu, 11 Sep 2025 00:54:32 GMT  
		Size: 665.2 KB (665190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b530a874d943f150599882e3c029393dcab060c17b2a21ffc56f6e2c437945`  
		Last Modified: Thu, 11 Sep 2025 00:54:33 GMT  
		Size: 3.1 MB (3108750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af9d4699ceb27b25a540286c8169022caecfaf0c22e0f91e69c05adb73fb93b5`  
		Last Modified: Thu, 11 Sep 2025 00:54:34 GMT  
		Size: 3.0 MB (2953854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c10b91b2475986aa5497b21cdaaed1c9559d8811e478382e16f5306acdc149`  
		Last Modified: Thu, 11 Sep 2025 00:54:35 GMT  
		Size: 60.0 KB (60018 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:f25f7df6bafa135186296a77f7a32af0a01418a052ea07332001d6f0a7345e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74291038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15dd73ee44b8cf3375fc3c77ed39d4daaa8b81a28770df70660682a30a9233e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4fe1a405e649605f6f08e5f3ba950432a6d1fdd5eab23bd4fa0001d376c36a`  
		Last Modified: Fri, 29 Aug 2025 15:59:47 GMT  
		Size: 34.9 MB (34877928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ee781037fd9035a42f968c33da4d7c009a3ceeb678302f10bd3543722cbe50`  
		Last Modified: Fri, 29 Aug 2025 15:59:35 GMT  
		Size: 9.9 MB (9863421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b979bf23bab82236b58b6b2116f6e338558283f31c224fce02ebeb28a083685`  
		Last Modified: Fri, 29 Aug 2025 15:59:35 GMT  
		Size: 1.4 MB (1366271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4041c27dde8dae65803df70b8b2d2f8b17f9c8a04f691f359f946bbf6e0103bf`  
		Last Modified: Wed, 03 Sep 2025 09:46:06 GMT  
		Size: 24.7 MB (24668866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941bfc7e92f312a73a7af6e5d63b433abad88d5382d9b10c75a34e20aaa63fdd`  
		Last Modified: Wed, 03 Sep 2025 08:21:53 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cafd148aced6a78ea36d321751a88eb83e89a1014d2e57289d96497a406b5ea`  
		Last Modified: Wed, 03 Sep 2025 08:21:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961e81795c2535e2c25fbe1f55f4aeaa3d7784ac8c765e31ac211a65a928f725`  
		Last Modified: Wed, 03 Sep 2025 08:21:58 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28075d9744eb1a92b2158094ca23d796a8d1e7fe3a9cbf1cb6c29bc3de345259`  
		Last Modified: Wed, 03 Sep 2025 08:22:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:aeb000cff82031b5d60e7ae46bc65121373eee504020ef1202361c071c39fa75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6867108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3693e94356f3c707b8bec4be5e4932c348ccd3c0ec45f3bfb7ab1dfac9dc33fb`

```dockerfile
```

-	Layers:
	-	`sha256:8daed1338be8d1a44908d63d8e45052bd80f4aed0acdef57b55250701c160dbb`  
		Last Modified: Wed, 03 Sep 2025 09:53:12 GMT  
		Size: 668.1 KB (668147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ffdd65dea145f88e81cff0e71c5ad51b7822a408d0089b2737c2d977a18530`  
		Last Modified: Wed, 03 Sep 2025 09:53:13 GMT  
		Size: 3.1 MB (3146903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63dfe59994b13e612f3f76e04b6e7d3351299b3a02280cd3ae5fc574b7a55679`  
		Last Modified: Wed, 03 Sep 2025 09:53:14 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e76765b2b338e4132b1ee2d3431e34c6a0706fee6f21a492e5e27291d18de9`  
		Last Modified: Wed, 03 Sep 2025 09:53:14 GMT  
		Size: 60.0 KB (60019 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:50a04b5a1c536dacf87bbf922a03e867cffcdab364fbb58412171e19f5acbd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71217212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ae16959b88d25abe18de45cb1e6463a1ae38a526add8f97a400faa5af1a0bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Sep 2025 17:05:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_VERSION=4.1.4
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Sep 2025 17:05:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 17:05:29 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Sep 2025 17:05:29 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Sep 2025 17:05:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 17:05:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 17:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Sep 2025 17:05:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Sep 2025 17:05:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44517a636765712cde181549cbf7d128d8269c49baf0479ad3554ae5e713cbe8`  
		Last Modified: Wed, 03 Sep 2025 20:21:17 GMT  
		Size: 34.0 MB (33958157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad6118b990bd43a45f2da5c51a500fd67b5f2bb3585478ce04a3fcb9c8f4d8c`  
		Last Modified: Wed, 03 Sep 2025 20:21:14 GMT  
		Size: 7.5 MB (7513252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df483c6b4fc36ac689e4d0da6ac9f95dc40c4330eabbcfd91f868748346cf5b`  
		Last Modified: Wed, 03 Sep 2025 20:21:14 GMT  
		Size: 1.4 MB (1430442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331ee67e51974adc8b5a26bf44d723fbdb582d9d2126aeb54eb8d490de5162fa`  
		Last Modified: Wed, 03 Sep 2025 20:21:16 GMT  
		Size: 24.7 MB (24668642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd79bd391c483c4f66610f6b1c9172b11313cb730c83884cbd041a9b1541795a`  
		Last Modified: Wed, 03 Sep 2025 20:21:15 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97a161ce58ff38b6f9523403622076277075058eb72406afdab7ca35d11a5f1`  
		Last Modified: Wed, 03 Sep 2025 20:21:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcfa646b424eaa944b6e71cb76b62b5a5345336a4dcde09fc1136a4f918fb51`  
		Last Modified: Wed, 03 Sep 2025 20:21:15 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fe448ca9bb2778f75758f521b8e0502a07fdd3ebeabdd9b5fb3fb03e170c68`  
		Last Modified: Wed, 03 Sep 2025 20:21:14 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9c2da99ef784eeef95f4c5c9a1aa110adee500c93b20e96dc2c0a152dd59dc18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6566588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13decc83ed0810d8c3ab0dad48ff378ca6fcc10c9134891dc45d23b507f08a26`

```dockerfile
```

-	Layers:
	-	`sha256:9de2c9a68708386ae0b5c3f1472aa52a60fcbf23cb79810c1b4b125e25800604`  
		Last Modified: Wed, 03 Sep 2025 21:53:14 GMT  
		Size: 665.1 KB (665144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83fe6796caf88b73ffa4a9e2b5cb045a7e070cf21d3269cd6069da0cbe3625c4`  
		Last Modified: Wed, 03 Sep 2025 21:53:15 GMT  
		Size: 3.0 MB (2998167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ef8b41adce3b38a0a6519e25bc9744b2a2344cbaa1a3d7b2d0735ca467919d`  
		Last Modified: Wed, 03 Sep 2025 21:53:16 GMT  
		Size: 2.8 MB (2843321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f63b7dbbe60a2611c8e9c53d7778a36bcb3e3b7b64dd308c6bbbe0406bfd635`  
		Last Modified: Wed, 03 Sep 2025 21:53:17 GMT  
		Size: 60.0 KB (59956 bytes)  
		MIME: application/vnd.in-toto+json
