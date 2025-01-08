## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:9c2cf13ac49ddd9e76fa909800e86ee5385752ef2d875972a9c4124b4d179c2c
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
		Last Modified: Tue, 07 Jan 2025 03:23:18 GMT  
		Size: 7.6 MB (7597212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a555ece717a38fbc478fdb27c25bef64418173064d0825b5a076a00398945fd2`  
		Last Modified: Tue, 07 Jan 2025 03:23:17 GMT  
		Size: 2.3 MB (2277950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4143d74abba219f8df3a4eadaf9d0c77d36d0e8f40a74b51a3dcee8161ee53c1`  
		Size: 18.8 MB (18756221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cbe1ace192b83070648255b698be09df87d1586f85487c589f9bcdb3cc699e`  
		Last Modified: Tue, 07 Jan 2025 03:23:18 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf4043ad72149ea39cf0ddfbc09e0068ea5db0a16e7cdef987590bd6bc5fc08`  
		Last Modified: Wed, 08 Jan 2025 01:53:14 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba35350993bf3986c67773b242e977f36fa717bd07b9af3458106b242bfff1a`  
		Last Modified: Tue, 07 Jan 2025 03:23:19 GMT  
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
		Last Modified: Tue, 07 Jan 2025 03:23:18 GMT  
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
$ docker pull rabbitmq@sha256:46bf57eba25e0a36ace5b7e9638e5725022d6714f459de8ed92a0c2392617a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63047107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b74bbd4d6f89e840a7506121373256df0684f804ef879e768d35a00c587657`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 06 Jan 2025 19:11:15 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Mon, 06 Jan 2025 19:11:15 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 02:28:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 07 Jan 2025 02:28:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 07 Jan 2025 02:28:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jan 2025 02:28:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 07 Jan 2025 02:28:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
ENV RABBITMQ_VERSION=3.13.7
# Tue, 07 Jan 2025 02:28:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 07 Jan 2025 02:28:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 07 Jan 2025 02:28:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jan 2025 02:28:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 07 Jan 2025 02:28:15 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 07 Jan 2025 02:28:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 07 Jan 2025 02:28:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jan 2025 02:28:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 07 Jan 2025 02:28:15 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7237beb15ac3b33bb6dca28a3e8c9dee356a72f799b501a00c291adadc2974c2`  
		Last Modified: Wed, 08 Jan 2025 00:37:09 GMT  
		Size: 33.3 MB (33283911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7ee1cc014d97440f46ba8a7e3528fdd51bf06c32d2d3688b17e4f31cdaa0b6`  
		Last Modified: Wed, 08 Jan 2025 00:37:08 GMT  
		Size: 6.4 MB (6418902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30071f18d8014a09d5b98d7c3aebbeb1c94e11b949ae7bfa3ea8ae9aaf6bc886`  
		Size: 1.2 MB (1225396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda0a9e4f892ec3306de3df65b0066ebeb5aed530aacb157292b5889f646866e`  
		Last Modified: Wed, 08 Jan 2025 00:37:09 GMT  
		Size: 18.8 MB (18756114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4236dd2f57a611ed8c9f8927e9d5c8d21e73c541b06fe11289b304dd71a93f3`  
		Last Modified: Wed, 08 Jan 2025 00:37:09 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a51f1a2cbb1d88ca91a1443d28602dbae15862b6ef5c2b14bcb79fc89385bbf`  
		Last Modified: Wed, 08 Jan 2025 00:37:10 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fe60c4be4f2f0a4897e4ccd215d514f019ccd3c588b7b347cb606f2aeeb8ba`  
		Last Modified: Wed, 08 Jan 2025 00:37:10 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a15283c60751a3b5b8d47fa44280c02864e5b2fc49a8793e3c884aff8565b9`  
		Last Modified: Wed, 08 Jan 2025 00:37:11 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a0386ab8ca6530f9a42922d9c18f4c43602a3afa28986054fd44856e247a7ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 KB (60579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cbf0cbe1332ee57b8bd88554920008cb8205d6edb71cbd5445bc35afa0ec7e`

```dockerfile
```

-	Layers:
	-	`sha256:03d58322387b669cad4f2638c8ca94fb04fc5db0d72ed2cd535cf576f34d6192`  
		Last Modified: Wed, 08 Jan 2025 01:53:18 GMT  
		Size: 60.6 KB (60579 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:6310dc76cd1d62a575b2082d1e91ffc7aaa0fe80ddba9fcd795c117d97b0d728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62323927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dd974f38ab0bc7da67eff0c5b7008fc302ef05972df48e3d6ad1303bc9bbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 13 Dec 2024 00:49:14 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
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
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d41a3579267d72724a123ef52737453090ab899b52188ec3151a4b66f1702c`  
		Last Modified: Tue, 07 Jan 2025 17:37:20 GMT  
		Size: 33.2 MB (33219223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc76ed6ee71fcf5fe1733330a618b09d4e6ac61ce797bbbe16d3b0e5b14a7271`  
		Last Modified: Tue, 07 Jan 2025 17:37:19 GMT  
		Size: 6.1 MB (6120488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9a35a3f2a39ad29c0350e68c9e2c8c1ae0f91cd756914626c8a108ebbc481`  
		Last Modified: Tue, 07 Jan 2025 17:37:19 GMT  
		Size: 1.1 MB (1133176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d8a898d5dcb9bf36e3d9a7203350331859438a0db21081a71b183199c8620`  
		Last Modified: Tue, 07 Jan 2025 17:37:20 GMT  
		Size: 18.8 MB (18756048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df64991c26cec975ca2456c8b6f88fa2021d2da3ed3146cf14f5076d4b60abd`  
		Last Modified: Tue, 07 Jan 2025 17:37:20 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15c45ff3acaa16ea55a16198e110e46eb33dcb55ea5cb9f337e567749104775`  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa18d131b9c31c5a352e5990d117c4c2e46c0aca135150ee7e2e73c87db6f1f3`  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5d44554c328e4733a6f4cf7a77dd2fe129b2f9cfd1580d3d6174d1459af4e9`  
		Last Modified: Tue, 07 Jan 2025 17:37:21 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4d882cd3026ee56bd433d2e330fe077fb06ab64c8150146fdff23ae03700e6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6492212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef355b61d34d6ee51927f8717a9809026ab3c6659076cbe5bdca7b12ea53459`

```dockerfile
```

-	Layers:
	-	`sha256:974dd63bfdaf187f5219e7588b8825ac9fb49546fa4b2a07da1055e6b0b00682`  
		Last Modified: Tue, 07 Jan 2025 17:37:19 GMT  
		Size: 651.2 KB (651207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dd040a9a54414fdb861fcc02fad74b6ff2455be15b5597ce30dff1ae3dd2f43`  
		Size: 3.0 MB (2968942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c9dc0c16a3b66221d2c26a9b3275820059ecf092d265dd5fcc32344a524e90`  
		Last Modified: Tue, 07 Jan 2025 17:37:19 GMT  
		Size: 2.8 MB (2812298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b0ca1488549959e98d0302d29ddfe7d209a2112c003becfb5c8928a0bfde27`  
		Last Modified: Tue, 07 Jan 2025 17:37:19 GMT  
		Size: 59.8 KB (59765 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:92e9634b06aabca3f319e1b974c006e840e9a5339b4952458a54da5e89b69283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72213686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f287f2fa691389bbe7616b84a948e7ea98dcd578d1077087dce27506418bc66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 13 Dec 2024 00:49:14 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad84355b218b39155bac05ef827041551dd2aa90c327edc6bbd90fa6d787cd2`  
		Last Modified: Tue, 07 Jan 2025 14:48:02 GMT  
		Size: 39.9 MB (39915048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bead00b48fd161f1109d43d9398d3a2749ec702c850d9797c5f695a156e1518b`  
		Last Modified: Tue, 07 Jan 2025 14:48:01 GMT  
		Size: 7.2 MB (7235079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4239044cf28d0980e56fba406a6b9017c232a27950d1c7913dc923aee4030d`  
		Last Modified: Tue, 07 Jan 2025 14:48:01 GMT  
		Size: 2.3 MB (2322581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c85fd4c93967670ef693d6416da6b7ef457abfa8080b040f7864103ae8f19ca`  
		Last Modified: Tue, 07 Jan 2025 14:48:01 GMT  
		Size: 18.8 MB (18756222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49fef107433df53bf348284afabe202647aa6efc734b85be407c4326a18a56b`  
		Last Modified: Tue, 07 Jan 2025 14:48:02 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01be404803ed65f88ac2993d28aa3afb61cc76e76970bac1336bd3bed207d6d9`  
		Last Modified: Tue, 07 Jan 2025 14:48:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a1229296215815f6a9b5a8a20a969aa2588ba808bf5bcae26f2f4564f406fb`  
		Last Modified: Tue, 07 Jan 2025 14:48:03 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99feb9c3012f2e2c5fb082ff0a9b7a4e13f50f58d29af9300300fe84a0eb78d7`  
		Last Modified: Tue, 07 Jan 2025 14:48:03 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d18ec4404d37414d6635cbc5a3f131cfd5eddba2a64edd60a4b03509eca52450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6834804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8dde281ad12d7e2709cfcaa70fed7e13b2a16cdd2e0c5b4d645138308f6dd5`

```dockerfile
```

-	Layers:
	-	`sha256:e5b44af4c94b28228423f33651072f4bf88fc1a8cd9727815a8ae82db41e4f7f`  
		Last Modified: Tue, 07 Jan 2025 14:48:01 GMT  
		Size: 655.8 KB (655849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be04d69d27b5ac44043222b8fdc3bbfe1debc444281dc96359ebd19aed8536e9`  
		Last Modified: Tue, 07 Jan 2025 14:48:01 GMT  
		Size: 3.1 MB (3137893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b6e46faa88b738dd678e481aba4ca85130ef6c286fd24dd974236684e1f32c8`  
		Last Modified: Tue, 07 Jan 2025 14:48:01 GMT  
		Size: 3.0 MB (2981255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:774e923eeac7bfafaab389d72ef086a95af072dd265218a1f27f6fc0fc512b0b`  
		Last Modified: Tue, 07 Jan 2025 14:48:00 GMT  
		Size: 59.8 KB (59807 bytes)  
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
		Last Modified: Wed, 08 Jan 2025 03:05:41 GMT  
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
		Last Modified: Tue, 07 Jan 2025 03:35:37 GMT  
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
$ docker pull rabbitmq@sha256:c38ed861130026bcf15089a66b816208aeaae2ddc19e7b570aed291ba635cf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65422405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812d1e4021a9ccf7fd9b0924bbf2da378868afc0ee5983e29216899d54483ce6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 13 Dec 2024 00:49:14 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75e9bf6c2eba8a1269d802bd487d4265d1037ec04480d03be2c4ab23e7f4c19`  
		Size: 33.8 MB (33750038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512694eb868b49aa61492517f120d056b48795b928a2ef54772fa2dd4c134a8c`  
		Last Modified: Tue, 07 Jan 2025 09:13:29 GMT  
		Size: 8.0 MB (8001663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438bebd02ee5aea9c35e64605dde35fc3e20cc8250c9f898c003cae8284c948b`  
		Last Modified: Tue, 07 Jan 2025 09:13:29 GMT  
		Size: 1.3 MB (1345132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f9dd85527c145460f119be56230f6344f424a1e6822f2dd8b5c90a6a8fd9cc`  
		Last Modified: Tue, 07 Jan 2025 09:13:29 GMT  
		Size: 18.8 MB (18756079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb80f938c33ab776cee79370685774ac73fc267c241aa676ea7f4d109ec41ed`  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3efd8e219cab55fb5cc735597516d96297994e235f65934c4584bdc4d3af39`  
		Last Modified: Tue, 07 Jan 2025 09:13:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e55b0f7e153934d46b39adc8bb0d0493954c09890fbcff094adfe33b4f79ce`  
		Last Modified: Tue, 07 Jan 2025 09:13:31 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195404c34398403accd617ee410ed65fdcb48bbcb4ca6febda590f81a1501aa3`  
		Last Modified: Tue, 07 Jan 2025 09:13:31 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:731fd34bc2923ab6a44424f6b7e1db474d1882e7a0cf59ab46f6e10ed346c3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6730498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0942e5e6cdb8a158feb07c6376538f0ef08616e66b3a322f46655e582a37e398`

```dockerfile
```

-	Layers:
	-	`sha256:90fb6b5368c82b1c00e2473a7f43bc86add7df13b02eeac0570da720a69c727d`  
		Last Modified: Tue, 07 Jan 2025 09:13:29 GMT  
		Size: 649.3 KB (649256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dc986827f08d8a896195234aec40d590572f4dce926f52ea7ed170379e47b70`  
		Size: 3.1 MB (3089128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a918559af0ebf9e2f0009cfd027b42a57efba5bf840d2eb3378696cb167bbdc`  
		Last Modified: Tue, 07 Jan 2025 09:13:29 GMT  
		Size: 2.9 MB (2932478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db4ec2a915da01531096e32ede716a713b66f95585e2c59a964c0ab091c5d739`  
		Last Modified: Tue, 07 Jan 2025 09:13:28 GMT  
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
$ docker pull rabbitmq@sha256:12e4cf3e7102426f32db85c623254d020f95dd00656006cb8fae3e008195c40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64064052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff7880418e8b59db088a8162925d68860632ec5fcf5ebc59b1f48d46d971e59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 13 Dec 2024 00:49:14 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d609f80a5bf59592c8a7e0d9e3c7ba8d3efb4feeeace9a4ad6e4bd2fa61befea`  
		Last Modified: Tue, 07 Jan 2025 14:57:49 GMT  
		Size: 33.8 MB (33779044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400588b47b9e3e94bfaa0140cc5b701de8ff1a2ef98f970d32c96f4a73fa8b5`  
		Last Modified: Tue, 07 Jan 2025 14:57:48 GMT  
		Size: 6.7 MB (6744382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186e3d59874bda690fe281426b35e7a7f95e15bc8c818057d0056734d91a0e3`  
		Last Modified: Tue, 07 Jan 2025 14:57:48 GMT  
		Size: 1.3 MB (1323342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269583e901314efd209e79fcee1bec3476acd0b68be67b0de196f2611ffbfe8c`  
		Last Modified: Tue, 07 Jan 2025 14:57:49 GMT  
		Size: 18.8 MB (18756082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b5911f2a4d205f4fc63ade3ca0eb8e3412153cf8314421a00437297be79c1f`  
		Last Modified: Tue, 07 Jan 2025 14:57:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb4982f9828d637cc00995d65dc4360c23fd40836df35efe52514a681cc0c76`  
		Last Modified: Tue, 07 Jan 2025 14:57:49 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b685b0f9adeaf968a5697b2ef5814419c7c90479046a21076431da3a197fef`  
		Last Modified: Tue, 07 Jan 2025 14:57:50 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a61c1f37265003e609139708d3a575f75b200cde2380c8d0e5a119aff5fdb9`  
		Last Modified: Tue, 07 Jan 2025 14:57:50 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9dbc25dfbf449910bb21be30d0bfae5fefc2be23ad50c4d0a22208a8d1612918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ef096568f1ef9c562fad9dc6a626f05f6c179a6c1d0877215ac42a4fd85596`

```dockerfile
```

-	Layers:
	-	`sha256:6b381163f29eeb7944445502b12f926b2efdc5a52a70dd9991aa26e60a4ba115`  
		Last Modified: Tue, 07 Jan 2025 14:57:48 GMT  
		Size: 649.2 KB (649228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6089becac8c539ba311ff2de60bb2ea414d07652690cd320d009c76b5fe35c2d`  
		Last Modified: Wed, 08 Jan 2025 01:53:39 GMT  
		Size: 3.0 MB (2979101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ecddc202fb8b142475d3885312b0de8dc35c594e8909a3e2f97497072ef205b`  
		Last Modified: Tue, 07 Jan 2025 14:57:49 GMT  
		Size: 2.8 MB (2822481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c48b529fb1c23281e3688f04cd7569eba2039c31fbeaf202a234ae5934a9e1`  
		Last Modified: Tue, 07 Jan 2025 14:57:48 GMT  
		Size: 59.6 KB (59580 bytes)  
		MIME: application/vnd.in-toto+json
