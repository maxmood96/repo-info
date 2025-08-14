## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:a6dbb0d4e409a371b0c4baa0cc844903be8702ad29e7917fd7f3d19207cb468e
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
$ docker pull rabbitmq@sha256:b529562dde42f1993a0013da03158bc8f6727582e6dd132f41ef218c94aaecd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85941840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1578aa61e6b67380cd31681d81abc9b27b80e2471b2f704e0b751ea7f74c316d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 04 Aug 2025 17:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_VERSION=4.1.3
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 04 Aug 2025 17:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 04 Aug 2025 17:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c5f66ccb3cc0007578cda9c7403306e0294c00b3a4ffe96267057f705b16f8`  
		Last Modified: Mon, 04 Aug 2025 22:01:44 GMT  
		Size: 42.8 MB (42838706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d31688a55c16aa0ce4fa681c6cfb762a1cee3974f957327de32502fad936ebe`  
		Last Modified: Mon, 04 Aug 2025 22:01:41 GMT  
		Size: 8.3 MB (8314151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7de5dd0f650cf488d307a6fbd4d18ea35a94eb7abf3f8c3d5c4aac51ac8a648`  
		Last Modified: Mon, 04 Aug 2025 22:01:40 GMT  
		Size: 2.4 MB (2374075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9ba52ca75159f52f9fb7b8a40d4e1b43446fe8fcfa6b813afd0973966b4c90`  
		Last Modified: Mon, 04 Aug 2025 22:01:43 GMT  
		Size: 28.6 MB (28613475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a13011c58db47d18b20ae2f07009cd8064ff75a27e276e31f6744a8dd2620a2`  
		Last Modified: Mon, 04 Aug 2025 22:01:39 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061f9a61e9c26dcee7d4feebf6f882fdd008ade7b180efd05bdb87fc95f1f760`  
		Last Modified: Mon, 04 Aug 2025 22:01:38 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bbc2b0e0f6daf2bd436c7840cf68286409a04ca60341fb381c39c780037f91`  
		Last Modified: Mon, 04 Aug 2025 22:01:38 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af63c1637b062191a390a644ec053340d92d051c93309edba02e3d285ea7dad`  
		Last Modified: Mon, 04 Aug 2025 22:01:38 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a104804fcdaed2f156167744cf09abf9a24f5ef60e263b1f8d979ad9e9b67b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6783109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897f838208dc29a67d308ff4e553feaad450482b55c320404e9fdb4fdf1e2d77`

```dockerfile
```

-	Layers:
	-	`sha256:a4ffb32edc9faab8e41bd9b6d682344a2786691785dd12cec640e4ba30ffa0a9`  
		Last Modified: Tue, 05 Aug 2025 00:52:48 GMT  
		Size: 671.3 KB (671338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b0fe59dc0ea965e0ae4e75bffa8f62fb56a06f2024dbabbc51e4e9e8d1323ca`  
		Last Modified: Tue, 05 Aug 2025 00:52:49 GMT  
		Size: 3.1 MB (3102678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8fbbbacf45a5d1661235647ff953426f5862693a571b2047101cadc385aa1b`  
		Last Modified: Tue, 05 Aug 2025 00:52:50 GMT  
		Size: 2.9 MB (2949137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f3c00aa45b22107f7ed50f7129aefd2459f0848507aab8939edd0941067b4d`  
		Last Modified: Tue, 05 Aug 2025 00:52:50 GMT  
		Size: 60.0 KB (59956 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:4162dc375ecd56863a879812022a110d1bbc7305393899e1f564c60552830126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73992550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b2aee3cd06771ab5eebc2f5fb7f00fcf78270abb13c938b0ddc3e168fcca10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 04 Aug 2025 17:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_VERSION=4.1.3
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 04 Aug 2025 17:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 04 Aug 2025 17:05:26 GMT
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
	-	`sha256:d000bd631de48c160a824cedd6f544a36d0d182d6e4770bcf7bdb2fb8012ca81`  
		Last Modified: Tue, 05 Aug 2025 00:36:33 GMT  
		Size: 28.6 MB (28613215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bea5ecb0f8d8ef7f92ea07496c25124f37ba2753a884399995398fe7c999d2`  
		Last Modified: Tue, 05 Aug 2025 00:36:29 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bf272d65efc8fb609e0e879966c91076330b4c83a11498e7039bc2928c5eb1`  
		Last Modified: Tue, 05 Aug 2025 00:36:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520ef26cf9ebb5509323901e13ef52d70eef4100620ec30501fffdd70c133bdd`  
		Last Modified: Tue, 05 Aug 2025 00:36:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627c894c5ec0c925e8a28c9160fb32d819e0a9059549e53e08126744d69e0db2`  
		Last Modified: Tue, 05 Aug 2025 00:36:28 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:79cbcbca203fabdef116d4d9925736f7382739f4385210091f8064960dba16c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec53df2a5110f99bef9fbc38802367631e7272540ae94f39cffa9bf0f759f91`

```dockerfile
```

-	Layers:
	-	`sha256:252b5efb0e9c8ca60495f0842bb3b640568f805f00b2bdaa930092323d14ac6f`  
		Last Modified: Tue, 05 Aug 2025 03:52:48 GMT  
		Size: 59.9 KB (59935 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:692ffe68c53de3b85658d4aeea7107cc8e4652f84722c5a1e88f074e12d3a2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73178310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc3432041c10ed5ccccf1834badc5d91457417a2b244033aa01acce30a411cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 04 Aug 2025 17:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_VERSION=4.1.3
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 04 Aug 2025 17:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 04 Aug 2025 17:05:26 GMT
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
	-	`sha256:b1c28c980f9b19075908683e0ae54ca7baf45eb4a52dbe75939044065c246434`  
		Last Modified: Tue, 05 Aug 2025 05:16:14 GMT  
		Size: 28.6 MB (28612865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f374117fc3a0d6f709f1ad1fe9efcbf6dcee8bd3cceeacdbe5ec735557c8bbae`  
		Last Modified: Tue, 05 Aug 2025 05:16:13 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358f6a58058ec48558392f94bfdb22bf250bd57f99a0b20f7d16b7ee9febd893`  
		Last Modified: Tue, 05 Aug 2025 05:16:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9cf60d3940efedc07535df7a267d2ec92aefc349ebe2cdb1e6fb7041c292c5`  
		Last Modified: Tue, 05 Aug 2025 05:16:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609a31fb9a4713c76e976d2b0699fe3441a69d63153bc3311485db2775a29626`  
		Last Modified: Tue, 05 Aug 2025 05:16:13 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f6416b6b4a20b19c9ed6ae5a2d82a2713326e45d51558d1ef6924eb8520d081c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6547412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e75ecb8c4cae7086b7c8a6bb88c11e084816805e0d59aa5f385ab2b330f0c3d`

```dockerfile
```

-	Layers:
	-	`sha256:015e5abf2da4fc80e35519634101bee2d3436d134b989da1e20c43424bc4c88a`  
		Last Modified: Tue, 05 Aug 2025 06:52:52 GMT  
		Size: 667.1 KB (667131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2003e414bbf009eeac796bf17a9ba9ed575cbee5d0777babc64d03760ba57a44`  
		Last Modified: Tue, 05 Aug 2025 06:52:53 GMT  
		Size: 3.0 MB (2987501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2badd8ee855ed7cdfec1582493b04b9f83620fcaf5c28ddbb3a02c1d2519a7ea`  
		Last Modified: Tue, 05 Aug 2025 06:52:54 GMT  
		Size: 2.8 MB (2832631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35791c6c0553ab23aae882dadd3b1b59e2983a0404e3c771fb4fffb90ea05cf6`  
		Last Modified: Tue, 05 Aug 2025 06:52:54 GMT  
		Size: 60.1 KB (60149 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:f6ae8959904b205a90dc5e14ab62fa88a85aec248480a4c6bcf65a470197262b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85053585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29c8a58ff36ee66e568b160077fe401d7a60e8f535ccb6e7fd0d3654fd1e130`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 04 Aug 2025 17:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_VERSION=4.1.3
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 04 Aug 2025 17:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 04 Aug 2025 17:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0587d8c24476c1fc5396fcac6c76c465e168a883956eca8008f3e654fedaf656`  
		Last Modified: Tue, 05 Aug 2025 06:35:18 GMT  
		Size: 40.8 MB (40845023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a218fa069a318a38adbc7015fd4c6e3a318789db8f7359146ae1c4c8307fc2c2`  
		Last Modified: Tue, 05 Aug 2025 06:35:15 GMT  
		Size: 9.0 MB (9037844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d54c7e1e77aba01a7073dfcfe37e4c377becd1d499776f322c230dd59f4193`  
		Last Modified: Tue, 05 Aug 2025 06:35:15 GMT  
		Size: 2.4 MB (2424774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fed9c649f232cd374b52be0508e9c53bac8121de8d10f00878e34d3c43bb307`  
		Last Modified: Tue, 05 Aug 2025 06:35:18 GMT  
		Size: 28.6 MB (28613454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1136f819d09897a1d3b121b152062641555004441506d0df261e2ca6c206728e`  
		Last Modified: Tue, 05 Aug 2025 06:35:14 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773cf0f709a140800b24b2fd6380fd2ec00f78d50bbb5493252f326d4fa2084c`  
		Last Modified: Tue, 05 Aug 2025 06:35:14 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8ba21254d2601742ffc556ade1a693a4b6ff974a2cd67311170b2f85c810e`  
		Last Modified: Tue, 05 Aug 2025 06:35:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558b15036638ab57e54d8663058b205e6b995f6494060b3036e506ff00265fc8`  
		Last Modified: Tue, 05 Aug 2025 06:35:15 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fabb0ae804a68a6b1bdccf0c45bba24b69af789e0ee8eecafa4a42dcaa9adf0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6891415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24758c4bfd93f9f054735ffb27a547a7b09c6490ea7d610facf182e3b3354ca`

```dockerfile
```

-	Layers:
	-	`sha256:bfb47e6ab978975bb070c4a8db7bf81ec3250b6445b8fc1dfd7b64b606c8a896`  
		Last Modified: Tue, 05 Aug 2025 09:52:53 GMT  
		Size: 672.1 KB (672131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:603c702e8bff65ced26fcd5f92f246e1934aa76e6131b90804fbea05b0f975ad`  
		Last Modified: Tue, 05 Aug 2025 09:52:54 GMT  
		Size: 3.2 MB (3156976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16a9fb2a8b179eb7c0076e86face3a341da8aaf4a914cee281f6539bfe6f1ddb`  
		Last Modified: Tue, 05 Aug 2025 09:52:55 GMT  
		Size: 3.0 MB (3002112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc8677194b1829b40872018d5610dfb9d57191b69a866c3a0b8790f5073498c`  
		Last Modified: Tue, 05 Aug 2025 09:52:56 GMT  
		Size: 60.2 KB (60196 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:bced213170d45d706a667e7499d1a64715e8b890f90a1a7b0c73006fb63c8e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75435180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c852c642d78e80e2a80382a130a27a7b390fe4ba623b408e34ee10c97287efe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 04 Aug 2025 17:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_VERSION=4.1.3
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 04 Aug 2025 17:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 04 Aug 2025 17:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d06da8d77ac8715e20891e1befca4955459d83403e4470756aa992b0d6d1cc`  
		Last Modified: Mon, 04 Aug 2025 21:12:19 GMT  
		Size: 33.5 MB (33546091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d8a4d6fd475efc1c2c642642a9208e0648b0c0b61d28dbdf991ae70f5b17e8`  
		Last Modified: Mon, 04 Aug 2025 21:12:16 GMT  
		Size: 8.3 MB (8327303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f614f9432d4843e7ae8adef1a80278445ff85a4532e3e25d3a3d1fdea9ce4e`  
		Last Modified: Mon, 04 Aug 2025 21:12:15 GMT  
		Size: 1.3 MB (1332251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b949e6567639e8a6a0a9bb3ae2635675e90f975012d9b59f6be0a77ba78581f9`  
		Last Modified: Mon, 04 Aug 2025 21:12:17 GMT  
		Size: 28.6 MB (28612784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b347c2da540764e96b7da7dcbf4ff0d2a9874970fc9ebdc3cadd3b8cf66a0a2f`  
		Last Modified: Mon, 04 Aug 2025 21:12:15 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1efaa216efd165ea559cdce22cf177f880bce6c4a3dc9ff46ba7aa7c34dac92`  
		Last Modified: Mon, 04 Aug 2025 21:12:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac45066890b95f73c5d3a5818d3ccc3824fcc4c0d2edf7b05b019661e2e48d93`  
		Last Modified: Mon, 04 Aug 2025 21:12:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6069a0207c34dd369738d462984f48b125d534b6d53d8f3a2620471b64a40b13`  
		Last Modified: Mon, 04 Aug 2025 21:12:16 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:023b56f52b8347955862b656e8c6a359451b7e11aa06d7a006ed0404551a2cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6755951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9cdbbab87fad04ef230805989b57f48359bdd3fb7df39989e844fca9b6e93b`

```dockerfile
```

-	Layers:
	-	`sha256:050bebb011a61d01a35bf2886f947708764bce1a3744510b346029ff07f4598d`  
		Last Modified: Tue, 05 Aug 2025 00:53:16 GMT  
		Size: 666.3 KB (666333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b91874385fcf3a58afd286bf69eb359ab0619f5081915356d59265cf065c2221`  
		Last Modified: Tue, 05 Aug 2025 00:53:17 GMT  
		Size: 3.1 MB (3091624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da20a82753a1e049e72f641f521b8ea61b1dc153fc7eb00fbabb057c6fd1e8b4`  
		Last Modified: Tue, 05 Aug 2025 00:53:19 GMT  
		Size: 2.9 MB (2938087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faf2b20325ac72a02bde6e2ba2b0cc382ffd3c70659b3d8291e3120973b701eb`  
		Last Modified: Tue, 05 Aug 2025 00:53:20 GMT  
		Size: 59.9 KB (59907 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:9eabae37e1bc97fd6945ec8f50ef470dfdaa031c2d6157e00100ee4791ee18b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76567383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2582f563b4666ad7a301706dc1a02d09c66923136377fce4bfb4802b7b1843e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 04 Aug 2025 17:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_VERSION=4.1.3
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 04 Aug 2025 17:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 04 Aug 2025 17:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12d6ef4d32b01829f32c21c9ccd5b2fadbb4ba1df99b99a5467e0f888405cee`  
		Last Modified: Tue, 05 Aug 2025 03:50:48 GMT  
		Size: 33.9 MB (33923889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a06394163e9ca6b1effa4231ca188a391a8966a61991dc2d13f35bb97ec0556`  
		Last Modified: Tue, 05 Aug 2025 03:50:47 GMT  
		Size: 8.8 MB (8849249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d4aa8979c7a83cfa3702ccb6111e72ee05261e4ec038c6823a2a94bfe44ee0`  
		Last Modified: Tue, 05 Aug 2025 03:50:47 GMT  
		Size: 1.5 MB (1452388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfb330e1026472eb14b23e84be2e495644eb6bd8f885db4419fa9075afd1327`  
		Last Modified: Tue, 05 Aug 2025 03:50:50 GMT  
		Size: 28.6 MB (28612995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca8885dfdb725fa9c176dce9d50ea5e55ac6cc75098265b8a99be69050eb255`  
		Last Modified: Tue, 05 Aug 2025 03:50:46 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095992d1b24d71f5006108ac0bedcf2601cb3c22789d76e21c849f94c8fcf33f`  
		Last Modified: Tue, 05 Aug 2025 03:50:47 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00d08427f0f8dc9583487c1ded243250099390cce9afd0b99d7bc529f81bfe5`  
		Last Modified: Tue, 05 Aug 2025 03:50:47 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b055dd241b87cdeffba4f72bef1a737a2be6cd6f86f9bf252659c32d29f1213`  
		Last Modified: Tue, 05 Aug 2025 03:50:47 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0ed83bf3578129523b3b9cc18252f826362134b94711fdb5dec62fb402b9e065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d172c3175a5e22376b2ac981a94c977deb474f8bb23afeb5ff5a31fa845b9b`

```dockerfile
```

-	Layers:
	-	`sha256:970619111ea59109e09151463341f2eff193fae811c1540d0f43415c49d92f78`  
		Last Modified: Tue, 05 Aug 2025 06:53:06 GMT  
		Size: 665.2 KB (665178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e664b083c1c982fbe618abc8f3480cd7ce5f1b34f9ff33efb1abe7837aaa88`  
		Last Modified: Tue, 05 Aug 2025 06:53:07 GMT  
		Size: 3.1 MB (3108730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd698b4828efc75edf65e6a39085693eacff3ff6fa01ee5f89ce2acbd8e65a2`  
		Last Modified: Tue, 05 Aug 2025 06:53:08 GMT  
		Size: 3.0 MB (2953854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:953d44d48424feea8cd0df893025946bbd3be1ed9ee1d00cf594c1930575cd70`  
		Last Modified: Tue, 05 Aug 2025 06:53:08 GMT  
		Size: 60.0 KB (60019 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:8dff801bde87722556d3da75052e1e93771bff68627e7adbe01beda5476a9e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78235487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ae0979264b4ed3caf5ebe818789c80a745317db66a6369a00a76fa264bbeb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 04 Aug 2025 17:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_VERSION=4.1.3
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 04 Aug 2025 17:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 04 Aug 2025 17:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073ffd46dcb637c8d387387cc47d80a04e265c17305ecaf85b0db6cb5c7a8275`  
		Last Modified: Fri, 18 Jul 2025 23:47:00 GMT  
		Size: 34.9 MB (34878055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7a629412ea555306ed6a1c0603271783da81388541d4b65aacab9e8acd27aa`  
		Last Modified: Fri, 18 Jul 2025 23:46:58 GMT  
		Size: 9.9 MB (9863423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dd69413818eb9ba00ac5708f3f11d9071a5877b3968515ebcbfdb51cf08cbc`  
		Last Modified: Fri, 18 Jul 2025 23:46:58 GMT  
		Size: 1.4 MB (1366276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e44a5b80f0b933b7db0a3709b70515e3b477d94f45ca30fbc14faa3b1d7cf1`  
		Last Modified: Wed, 06 Aug 2025 06:10:59 GMT  
		Size: 28.6 MB (28613180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b3508946f996f52e62530e4289b92b33fbae1cb875144bfbe5f24cae48b5da`  
		Last Modified: Wed, 06 Aug 2025 06:10:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2f0630593803eaee0e0a7c08cd928644e96bba50a9c18af60cc9007aaddab0`  
		Last Modified: Wed, 06 Aug 2025 06:10:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fdee96b8b8371b1f52641a93a447dc3a09e1a2671e7cdd280adfea53100cc2`  
		Last Modified: Wed, 06 Aug 2025 06:10:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0de390a5f16e8a3c279f3339d17df9a7d16df6ad69dc42b0d38954789bae36`  
		Last Modified: Wed, 06 Aug 2025 06:10:57 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fc9fee7c9e27e763d9d50bacdeb3f90d19bd5405dabb2959a01a3435575cd006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6867108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afcc1ea405606450b217cb9525672e286cf4388948258e00ad66ca073140fa6`

```dockerfile
```

-	Layers:
	-	`sha256:075639df7eeb77f6fab2f85616fd6151a1f69e49ceb63d4106dd5cbd63dfb748`  
		Last Modified: Wed, 06 Aug 2025 09:52:57 GMT  
		Size: 668.1 KB (668147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef30bba69be66a432f5faa13c77b8346f128f7d7394935d940810461abceeaf6`  
		Last Modified: Wed, 06 Aug 2025 09:52:58 GMT  
		Size: 3.1 MB (3146903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2858e37ce8032694c7edcad0f6ee6ebcf2faf34d4a7a35f85d43876dc9b287a`  
		Last Modified: Wed, 06 Aug 2025 09:52:59 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0bbbe455498d862ec5b682102ea72b830060ae11c2c24b0c85238dd4c48bcb`  
		Last Modified: Wed, 06 Aug 2025 09:52:59 GMT  
		Size: 60.0 KB (60019 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:62712a8f94ead72c5b1e6ed9e886d8fa2a16f6eca058339bd8f87cb044f060d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75161433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd42e082a087bdbb8d5479bcd93d440bd1631e5a66b0fb31f10bf40dcf59c6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 04 Aug 2025 17:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_VERSION=4.1.3
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 04 Aug 2025 17:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 17:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 04 Aug 2025 17:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 04 Aug 2025 17:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 04 Aug 2025 17:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Aug 2025 17:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Aug 2025 17:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 04 Aug 2025 17:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f435efa4903bcc9bcce5e00045170d90ab626d8cc251aa7d16cc6e93034e7d`  
		Last Modified: Tue, 05 Aug 2025 02:03:46 GMT  
		Size: 34.0 MB (33958015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b5156b91c1a20d7472a7b6a543a2fdf0864bd2fafdaa8f5a9f1e81258d793a`  
		Last Modified: Tue, 05 Aug 2025 01:52:46 GMT  
		Size: 7.5 MB (7513271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ec2c7c9f66df6014c07e4bd4e65deae31c11517b3300c007c8a9357352b4fd`  
		Last Modified: Tue, 05 Aug 2025 01:52:44 GMT  
		Size: 1.4 MB (1430447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a799e6dbe85f7451ba4a13d548a0fc417a9f368c06dd01cfe6a2576e5cabc635`  
		Last Modified: Tue, 05 Aug 2025 01:52:50 GMT  
		Size: 28.6 MB (28612982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4f6af42c5220c8490752e16f4c6d42a6583fe4afb35ce6852c2b81f54d3965`  
		Last Modified: Tue, 05 Aug 2025 01:52:44 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db275c5c34aa3b6a56f31c4015df585c4e0917a3b3a6cd71d28c1da4d782ea1`  
		Last Modified: Tue, 05 Aug 2025 01:52:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008d13876c6cc2140323321b85d7b4c7e5ed87d59d7f0956bc1c9c030ccf0c00`  
		Last Modified: Tue, 05 Aug 2025 01:52:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9403ba672bf99029d6a26d07e2da1f308445a2ee05498454692f42b634aea76`  
		Last Modified: Tue, 05 Aug 2025 01:52:44 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:22b44a87d8059452847f9a7189557391eaeb2cae9a4725ff3908814b0e529ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6566588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcec4b33d12d24cc8023d321d6ba3ea92796af1d8e8fcc6e403787acc1984490`

```dockerfile
```

-	Layers:
	-	`sha256:aea25c79d76f7ef1beeed176471d5be00b4c452dae02a1a14f862eeaa63cfeb0`  
		Last Modified: Tue, 05 Aug 2025 03:53:12 GMT  
		Size: 665.1 KB (665144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002efa0cb3fed8a28885dd4e593588299ea6fdfa029d384c4b4fa2eeefb42a8e`  
		Last Modified: Tue, 05 Aug 2025 03:53:13 GMT  
		Size: 3.0 MB (2998167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83806333839668ac4daad18fe48dc76221ab529f05af526a8edc5a6d05da4a4`  
		Last Modified: Tue, 05 Aug 2025 03:53:14 GMT  
		Size: 2.8 MB (2843321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:007229a438d01472bf364563cedab72b74ae31a60169ed339ed49cd48c3f01e9`  
		Last Modified: Tue, 05 Aug 2025 03:53:15 GMT  
		Size: 60.0 KB (59956 bytes)  
		MIME: application/vnd.in-toto+json
