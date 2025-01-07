## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:352a0b4d598001ed0e52cf63214a174bdc2aa4689df39fbccca470edfb16b143
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
$ docker pull rabbitmq@sha256:0896519533399a55df88f75072d0a1aab508993e6608d8b576b6d98cbc0868cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac252d2024e98a7ee0f722f9e03cb87ade84887b2a99f83f053a4708d7db641`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 13 Dec 2024 00:49:14 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Dec 2024 00:49:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Dec 2024 00:49:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Dec 2024 00:49:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62102b675bef2da1c390347780df8ded0ac79d8c5c6aad7d08a2f05e87968001`  
		Last Modified: Tue, 07 Jan 2025 03:23:18 GMT  
		Size: 41.7 MB (41721290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d43bec3a60bfa7e0b4926b4cd5a859a3cb2c5bb4985be089b44d9b63b6221e`  
		Size: 7.6 MB (7597212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a555ece717a38fbc478fdb27c25bef64418173064d0825b5a076a00398945fd2`  
		Last Modified: Tue, 07 Jan 2025 03:23:17 GMT  
		Size: 2.3 MB (2277950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4143d74abba219f8df3a4eadaf9d0c77d36d0e8f40a74b51a3dcee8161ee53c1`  
		Last Modified: Tue, 07 Jan 2025 03:23:18 GMT  
		Size: 18.8 MB (18756221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cbe1ace192b83070648255b698be09df87d1586f85487c589f9bcdb3cc699e`  
		Last Modified: Tue, 07 Jan 2025 03:23:18 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf4043ad72149ea39cf0ddfbc09e0068ea5db0a16e7cdef987590bd6bc5fc08`  
		Last Modified: Tue, 07 Jan 2025 03:23:19 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba35350993bf3986c67773b242e977f36fa717bd07b9af3458106b242bfff1a`  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b350fd75bc1470cca83b399c68f8362159fcbe833003a2f92fcbd57125d03e5`  
		Last Modified: Tue, 07 Jan 2025 03:23:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c9d1609aeaf7be94a16b02f4d24067465efb9584683bd8e89017e52774b4b2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6725515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a121ce62407cc67fec15946bebd0bcad1c0b5daa441cec3fce65e784454e84f`

```dockerfile
```

-	Layers:
	-	`sha256:bc648e41ff51d0e96b6e93310322b77d62909338533f2d7e8f95e8380eccd238`  
		Size: 655.1 KB (655068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e206f69827d365ed7d67f1a972935390e0f64c3988f9b77697a7748ab7fa2b3`  
		Last Modified: Tue, 07 Jan 2025 03:23:18 GMT  
		Size: 3.1 MB (3083092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef7b7231694d621cc4cbfb9c70afefb646ecc42935aa62e94ce33e3dc1d7f0d`  
		Last Modified: Tue, 07 Jan 2025 03:23:18 GMT  
		Size: 2.9 MB (2927777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96637b519bb25c03a11069068bdd77359861a2e8f431ff9db0ab481fd08181d0`  
		Last Modified: Tue, 07 Jan 2025 03:23:18 GMT  
		Size: 59.6 KB (59578 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:4c20326da583f914a372332b849df339b41aa73f3cfc06ca1b018414123f7f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63057835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b850f4111277807c2425bd66047294953989b99edd951a5f7be828be06867575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Dec 2024 00:49:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Dec 2024 00:49:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Dec 2024 00:49:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b826e38ed0771a837e744448e5748340c08eb3c7e237e4a8d0ffe3c201c3d0`  
		Last Modified: Sat, 14 Dec 2024 01:44:44 GMT  
		Size: 33.3 MB (33288421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce4a3f28f112aebd4e2e55717843a32af96b8853241c3681b98615b9b580efc`  
		Last Modified: Sat, 14 Dec 2024 01:44:44 GMT  
		Size: 6.4 MB (6418903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5b64b5e5d177cf79ef2805b7b9bb70644b3f0ffb77028ae37322c7e7d26058`  
		Last Modified: Sat, 14 Dec 2024 01:44:43 GMT  
		Size: 1.2 MB (1225390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad900bbfc342797bb1be421ced86ed79bdb3f3d7abce462ba0fdd415ba6a3845`  
		Last Modified: Sat, 14 Dec 2024 01:44:44 GMT  
		Size: 18.8 MB (18756185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c88c2567e86ff25742158e04bb10636747a8924c55ad6b8fa1e0b4b591b493d`  
		Last Modified: Sat, 14 Dec 2024 01:44:44 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d7b48a6329f4a079ded8e5637cce983f8a46927b4b95e9712bf980ac645269`  
		Last Modified: Sat, 14 Dec 2024 01:44:45 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bae74a7b457e6142e6f67b9eee51836ad2099fccd2a344bd18b8b5be61f327`  
		Last Modified: Sat, 14 Dec 2024 01:44:45 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dd72619c95f958246ecda2d515cfe3d07f46ae98e45f40c2f874c6ca8a2253`  
		Last Modified: Sat, 14 Dec 2024 01:44:45 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9942ce5f11e542ed5494f6daa8912dc0439728a7eabb846c642b7bf700cb4820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 KB (59548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a1c07914b97ad1969134da15f29c64082c66d92b3757497692583d7cb7b004`

```dockerfile
```

-	Layers:
	-	`sha256:8fbdb14828d3567274724472f9c27b4e978619b7c20b65bc253fc484becb9f94`  
		Last Modified: Sat, 14 Dec 2024 01:44:43 GMT  
		Size: 59.5 KB (59548 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:a92946a93b7f5711c548103f3dad843ae2e222b5b3d048f8e61537da3d86fbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62330719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a476d3838417ea6fb6d484c87cb5532cf8156c439384e8b7d35fcd0e386bddb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Dec 2024 00:49:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Dec 2024 00:49:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Dec 2024 00:49:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b36cee7ca597126290562cf6ed11da098ca91cf8c3ae60d0e29761ed02429c3`  
		Last Modified: Sat, 14 Dec 2024 02:01:34 GMT  
		Size: 33.2 MB (33219241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952a386502354aae3d447d452b6fbcb9e1c393a4ed6c690ec5e533d97ea702b`  
		Last Modified: Sat, 14 Dec 2024 02:01:34 GMT  
		Size: 6.1 MB (6120501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deb4306b5961a85056e4b3996b51be2a7009248aff81219ae781744093e7c10`  
		Last Modified: Sat, 14 Dec 2024 02:01:33 GMT  
		Size: 1.1 MB (1133166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac625879eadc8ac5c1b2f260117e4c7bcc5578999ceebc82c62582546a2e2346`  
		Last Modified: Sat, 14 Dec 2024 02:01:34 GMT  
		Size: 18.8 MB (18756025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5e4e0e4b68af4b4e90cfbc5100421da902ce5e472b22f0a95f4b90d393961b`  
		Last Modified: Sat, 14 Dec 2024 02:01:34 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ea49a54da8efc62582a4bd283d06c9d98add1ee91dedc7aa9b829c9668837`  
		Last Modified: Sat, 14 Dec 2024 02:01:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7eaff8a3aa4891790c05217ff29036a79f1af343f2330ce8c8b269e8af9169`  
		Last Modified: Sat, 14 Dec 2024 02:01:35 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1d257ed2ddfc6f52eb9029e5b7b248681c54c2054c54f712c25998b53b6a7a`  
		Last Modified: Sat, 14 Dec 2024 02:01:35 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7e1e947b9a3f6b7a945b8c1cc4bc79316ae6c19d858a4e9a538a1ab364bf42b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6500878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6b8aadd10303660b5fc4ab322e4141c96702588e1f0dc1eba8f6a4c905cd91`

```dockerfile
```

-	Layers:
	-	`sha256:426414858b63b0a63248cb4d2b84091293b04d6905d7095850b5152c14631804`  
		Last Modified: Sat, 14 Dec 2024 02:01:33 GMT  
		Size: 651.2 KB (651191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36421e9779b86106fff53cf94af691387977d24431d0b95d82bbd9a362e78401`  
		Last Modified: Sat, 14 Dec 2024 02:01:33 GMT  
		Size: 3.0 MB (2972864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73da496f246a6d8e177dd44a83e61d8f13f1557be1a42a46838e0ddc3f7db795`  
		Last Modified: Sat, 14 Dec 2024 02:01:34 GMT  
		Size: 2.8 MB (2817058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61a8a7da5bb41d6e252bb946922af4c30ecd61fe09fd46f2eb631dafa6c188b9`  
		Size: 59.8 KB (59765 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:767535b42c061efe053b839db27141137d733b3eb6c2ebb0bed42cd64ac7705c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72224125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61514ce77e94384949214559a090e7b517235230697c9eeb4aa13e9a6815dc39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Dec 2024 00:49:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Dec 2024 00:49:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Dec 2024 00:49:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae5132102e731d9cc259ba2f79e8f7772401dd98846cd521c6d9496c6f185cd`  
		Last Modified: Sat, 14 Dec 2024 02:01:52 GMT  
		Size: 39.9 MB (39915297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5187a0cae87e5b3318694a49080c212e5c3ff4f7e7f3498013b9e2e323b606bc`  
		Last Modified: Sat, 14 Dec 2024 02:01:52 GMT  
		Size: 7.2 MB (7235107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cfaf0cdced1c9a9e01f96be297de08f4f2db0982a12cbf853d264314b1a95c`  
		Last Modified: Sat, 14 Dec 2024 02:01:51 GMT  
		Size: 2.3 MB (2322555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553337c269cb39f63f4e86caf3a62f271adb703247e0bf9423ef6b100bd89e2`  
		Last Modified: Sat, 14 Dec 2024 02:01:52 GMT  
		Size: 18.8 MB (18756234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d548fbc128dcf54f0b4dfa57eedcda9710dfc4be1b9e7ff21666a8a6419d0`  
		Last Modified: Sat, 14 Dec 2024 02:01:52 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23959e45b0928eef32b50272d7fe17b60ed5ee16107ff9edd0630cbf14b524a0`  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d4f471945eaccc8d24c75ce13b6691f24fc32c6e5d4eb7093d3fd4495ec33f`  
		Last Modified: Sat, 14 Dec 2024 02:01:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaf0b7938955816c91d3cc9acc418282326a36217047de8eef8ff19907d9b6f`  
		Last Modified: Sat, 14 Dec 2024 02:01:53 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c75d13503f81afbaa27722223910ca0b28cbeb5c56e10cfe0a71a7dc024995f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4caa475d9cdb40da0a7e81f7608a716c748d4294834748263cd167d55c5326`

```dockerfile
```

-	Layers:
	-	`sha256:48d05224f1b5b6d9c1b514069041f14814bd7e3ffa68c35f1474077895801492`  
		Last Modified: Sat, 14 Dec 2024 02:01:51 GMT  
		Size: 655.8 KB (655838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edbe91b44e93abc3a05ddabfd936207925a3bdaa70bffc2fe2d570a2d56dfce`  
		Last Modified: Sat, 14 Dec 2024 02:01:51 GMT  
		Size: 3.1 MB (3142126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14bf2feadcf045d2013b1096309cacddd5e9c3f5419fcb99ce8a9ce3be002873`  
		Last Modified: Sat, 14 Dec 2024 02:01:51 GMT  
		Size: 3.0 MB (2986326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6dc103177ea23f9fc9d3f4190b4f6528d0190d91867fec196bf0683572dce53`  
		Last Modified: Sat, 14 Dec 2024 02:01:51 GMT  
		Size: 59.8 KB (59806 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:beb35daded53e5b3ab7dc52b280c7065036680cae8ab2b6e2b612c80d7732d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64316336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b193b511d4829b776c097529dc03a38b9bfd76ad4c39571611e2138a4e691361`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 13 Dec 2024 00:49:14 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Dec 2024 00:49:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Dec 2024 00:49:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Dec 2024 00:49:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b80e9af883e565a50ac2271a6ff973a1329663647f591d8485501f71c8d92e`  
		Last Modified: Tue, 07 Jan 2025 03:35:37 GMT  
		Size: 33.4 MB (33368668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024cf4f22a247fa4706f28881cb321cac60fbd937150701bb7f7e9c2d233cf11`  
		Last Modified: Tue, 07 Jan 2025 03:35:36 GMT  
		Size: 7.5 MB (7502202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6ac0dc1e1d679c878dab01ee9f39fa1145977ccc55fb539b3e9cee8011d171`  
		Last Modified: Tue, 07 Jan 2025 03:35:36 GMT  
		Size: 1.2 MB (1229377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7252f316f80ed074a428f868cf79153b609d7ec6bc2319aaa7353f41a2cc41d9`  
		Last Modified: Tue, 07 Jan 2025 03:35:36 GMT  
		Size: 18.8 MB (18756067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b00bc376fe3c37108230b7eadbd31fdff897ad3f2096c6f19a1f7ea4c252fe3`  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f8dc9842cdd16762cb682f0b6c85bfd3adef47e0be95951331369233ccc369`  
		Last Modified: Tue, 07 Jan 2025 03:35:37 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f5fb5ebdd26b5b8f560d7b7e60f845a38d990570e83495d1f02b88f2051a0d`  
		Last Modified: Tue, 07 Jan 2025 03:35:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a633cea4790e5222f2733021bc03e220e999f3b197b9e6a811ddfe79bf6da8`  
		Last Modified: Tue, 07 Jan 2025 03:35:38 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2e8d62a59777527ed8f8dc9330c02eccc8fcc72d10578e17418a46e3495b0cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6698732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43dae77e57e452377d6a05e529cacd72655a400c242f2231b6115e02920712f`

```dockerfile
```

-	Layers:
	-	`sha256:5ccb0df4bd07d956a37cb6fea2c34d6df45dc78c7f152a801fd1f31ed7ba0c82`  
		Last Modified: Tue, 07 Jan 2025 03:35:36 GMT  
		Size: 650.4 KB (650422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676537e375bf95102ecf7c97a0a45fa7891078bff60cd79ee5a38f888f60f403`  
		Last Modified: Tue, 07 Jan 2025 03:35:36 GMT  
		Size: 3.1 MB (3072043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc0dbd9b9ed0df7e7ab883c36b02659738285ab7af415d9d3f5587c4276bf517`  
		Last Modified: Tue, 07 Jan 2025 03:35:36 GMT  
		Size: 2.9 MB (2916732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:525ba107066bfbfa9dfa448e84ea378b46ff4daac0310bb083cef5bff09d5986`  
		Last Modified: Tue, 07 Jan 2025 03:35:36 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:2d154af3792a1a1a491d78822ad5fa3f17b716a101fe317cfbefbcb8ed0c2140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65431772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7521a4ead5f28825c2521d8b925e648339a72fc60e0de7ca8a6029784306950b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Dec 2024 00:49:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Dec 2024 00:49:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Dec 2024 00:49:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf0c12358be9623c6faeacb1dc8f885559856edc56c0f47f024020977e007d2`  
		Last Modified: Sat, 14 Dec 2024 01:57:35 GMT  
		Size: 33.8 MB (33750033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160bfb66f16569dc7b8a48f690b87cc1144ff8ff41a3ecc6d22ce3cf27768e3c`  
		Last Modified: Sat, 14 Dec 2024 01:57:34 GMT  
		Size: 8.0 MB (8001647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9c5fee1ad4dd4de2b9767c915062fbdcf7b3fed8b2e5528c5b099f9e8723f5`  
		Last Modified: Sat, 14 Dec 2024 01:57:34 GMT  
		Size: 1.3 MB (1345139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357a4ac0d67a5c7e2cd5d4a0090fb77a1ea39580bc16a05c4678edce1e74f11`  
		Last Modified: Sat, 14 Dec 2024 01:57:35 GMT  
		Size: 18.8 MB (18756091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be86603b06b4ae072fc9226457135123bc1e1e553f296dacc39bdb6e9dcdf669`  
		Last Modified: Sat, 14 Dec 2024 01:57:35 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d864eac654b16994eff5ed8e6963856a53e3ad1c41876679440732445dfc6c`  
		Last Modified: Sat, 14 Dec 2024 01:57:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b460aa091d2055020e4976e5f125bf78764a07e1562e5a3fa502123ceef736f1`  
		Last Modified: Sat, 14 Dec 2024 01:57:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a6158b2be3940171bd2e1cce5c755eb7c13edaf7d40a00018d31b560161e78`  
		Last Modified: Sat, 14 Dec 2024 01:57:36 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:47bc859f55f9db245257b3b17d652eee49f211b992764b0fec2277265ed7344a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6739597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d570845a7db5be47595635ee9bb3fdd047a7fecc1e30215d5afed3c6428e6719`

```dockerfile
```

-	Layers:
	-	`sha256:6b29678fc99ed60155d9d871f3c4c34bb9dec5da5e5237b815c13fca4ff7a76b`  
		Size: 649.2 KB (649237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c4e60a891c71afa08ce421e8993816a47de7c527e7b35a7bf085b4b69a87c8`  
		Last Modified: Sat, 14 Dec 2024 01:57:34 GMT  
		Size: 3.1 MB (3093268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d0863ca84eb84f340328a736baff8a3074c49e56f55899b1c13805aa2bdebb`  
		Last Modified: Sat, 14 Dec 2024 01:57:34 GMT  
		Size: 2.9 MB (2937456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7c709b06feada4445d7300f173047969a20938fde33fca5003a0c0b627eaa8a`  
		Last Modified: Sat, 14 Dec 2024 01:57:34 GMT  
		Size: 59.6 KB (59636 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:9ab576f3681d42c8a74f13018f46641bc12ba1b8cff9b1e887b82cdfb0d10063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66832815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780b101a19664f9498c387e09cb471a2d3057449c606fdf8b10cd1bc7ba7e072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Dec 2024 00:49:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Dec 2024 00:49:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Dec 2024 00:49:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d101dfaa1d966308871d898b0114ad10de26e2de2362bee857980900cdbcab`  
		Last Modified: Sat, 14 Dec 2024 06:00:34 GMT  
		Size: 34.7 MB (34703357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2399ae6285dbe54310639fef4eaa4c7ecf4afce5cf263d7a4da9c096ca6c6c2f`  
		Last Modified: Sat, 14 Dec 2024 06:00:30 GMT  
		Size: 8.8 MB (8752448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3d65e9f0b6ee3ee32880d37e579d48fbc4590695df130be3d6ed39808dd6b1`  
		Last Modified: Sat, 14 Dec 2024 06:00:29 GMT  
		Size: 1.3 MB (1265027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcac1fc9b7c58fb9f972485ad34fccae926a1d112e7c60ed2dab109ac1c1741`  
		Last Modified: Sat, 14 Dec 2024 06:00:32 GMT  
		Size: 18.8 MB (18756208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284721e9dec4ef035ad06ffc09e1aad97bec89916e486ef128d5d0d3cbb1df91`  
		Last Modified: Sat, 14 Dec 2024 06:00:30 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93f7ac7e76ef4ba8d8fe3ef62f300d0c65688f2442758f66b0b18a90d366730`  
		Last Modified: Sat, 14 Dec 2024 06:00:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e193fcdcbd15d1cf7b43755b587be306c6559e86a5084bbb9d9a407543d26c`  
		Last Modified: Sat, 14 Dec 2024 06:00:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b415d756dc67342213804a0f80b60c79a9cadca9d5acf0470efe0541c9d77c`  
		Last Modified: Sat, 14 Dec 2024 06:00:32 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3fa9315d72e5b772f3938ed3f81400adee35d9dec67fb9fad57050a956586cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6817857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d71a60af83781d229c4964bd67559d2ad17b7deb3cba1707c62c0fdac4a990d`

```dockerfile
```

-	Layers:
	-	`sha256:9b5e7bad5855f486a193387f56d17ab465b2fb23405b6f670b511f0245001dd4`  
		Last Modified: Sat, 14 Dec 2024 06:00:28 GMT  
		Size: 652.0 KB (652032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d03de4d3cdfd75c1b53a6c98cb584eed122c7cccd85ece26282ce0bf57acc2`  
		Last Modified: Sat, 14 Dec 2024 06:00:29 GMT  
		Size: 3.1 MB (3130995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca2d82994fc1fc6b26203ccd0dd7beb698cb6bdc2bfa78bab29c4ac9d46f92d`  
		Last Modified: Sat, 14 Dec 2024 06:00:29 GMT  
		Size: 3.0 MB (2975195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ec4306a7e4580de2c30ae8f0cf0748e4359966615a5d491230d492642afa97`  
		Last Modified: Sat, 14 Dec 2024 06:00:28 GMT  
		Size: 59.6 KB (59635 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:38c9d3135f1449b9d4596a87aad26432ed1bb88ec50b3b8789a966c9db1fe4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64074226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5bd3cdb773bdfe7b95be729d0a1897b0ba6d200100940c5f7c86f948737125`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Dec 2024 00:49:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Dec 2024 00:49:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:49:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Dec 2024 00:49:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Dec 2024 00:49:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Dec 2024 00:49:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:49:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:49:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Dec 2024 00:49:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765286748c319957bb3b0e73796431f9c08faf549f7ad94cf5f221425c91dfdc`  
		Last Modified: Sat, 14 Dec 2024 01:59:35 GMT  
		Size: 33.8 MB (33779165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5dfe6296580487b7f0a7d54f8db30523eb4219ba66996dd44a6f72fd3d5c11`  
		Last Modified: Sat, 14 Dec 2024 01:59:35 GMT  
		Size: 6.7 MB (6744373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99169e168f99b9d442ad51aea4d43a6c4285bd77df9c0d2124bc0be3ef94436c`  
		Last Modified: Sat, 14 Dec 2024 01:59:35 GMT  
		Size: 1.3 MB (1323344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f411c4ac16620ec1397154447346ba6d2e5503466971d94f53ad61079eaa051`  
		Last Modified: Sat, 14 Dec 2024 01:59:36 GMT  
		Size: 18.8 MB (18756071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff5c22dc5db3cb3d622dbd1697089d5908630b9135ea8a45f0df0cfaab5369e`  
		Last Modified: Sat, 14 Dec 2024 01:59:36 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3137cf69f981a2fb4da9fc390126462c9cea18389db5d9cdefd1be70b0f42a`  
		Last Modified: Sat, 14 Dec 2024 01:59:36 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a7a58173f4b43ff572f550571c8e391cab84037b30b51eb2184d0226566591`  
		Last Modified: Sat, 14 Dec 2024 01:59:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d929503939650c3e67f7bc6733954e4a26c774f8a7069d5aed18d9225f28f91`  
		Last Modified: Sat, 14 Dec 2024 01:59:37 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:55036d413872f6dcf748f5fac51072a2e38dee5dfcb934e377b9b71161040f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6519111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c0a0b5d6d8b22db265e3146db5cfe85adb980a91ffd24b7745b63c91609ab2`

```dockerfile
```

-	Layers:
	-	`sha256:246d052bdb996da7f2093e42d3c6b3223bf019f3b33b1342f2f372466d3e3a0d`  
		Last Modified: Sat, 14 Dec 2024 01:59:35 GMT  
		Size: 649.2 KB (649209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62a60e375b4ea9b9eb0fbf50707ee6440251b87660a7044db2a27de66491d84`  
		Size: 3.0 MB (2983052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93acc87293034b4c6591e8e0605ae1cbbd24761839191bd4e278094ad945a29a`  
		Last Modified: Sat, 14 Dec 2024 01:59:35 GMT  
		Size: 2.8 MB (2827270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad5e5589096f7cf531467c72c8c9d1e52d613980b76130a899b34aa10255c8ca`  
		Last Modified: Sat, 14 Dec 2024 01:59:35 GMT  
		Size: 59.6 KB (59580 bytes)  
		MIME: application/vnd.in-toto+json
