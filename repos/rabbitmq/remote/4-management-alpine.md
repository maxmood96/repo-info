## `rabbitmq:4-management-alpine`

```console
$ docker pull rabbitmq@sha256:b8169028ea0dfd5963ecea451efbdc049d0d39b83ba8af2faa5d4d42865e8202
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

### `rabbitmq:4-management-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:b82cc38cd89c6fb426eb7c017bc40b216615e2217bfcdd9e343200a7c21a28d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97161921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709e6a9c3d1b46d98d363d5928af99b1b80931269585a622f7ef7ecd7ac09422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:32:46 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:32:46 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:32:46 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:32:46 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:32:46 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:32:46 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:32:49 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:32:49 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:32:49 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:32:49 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:32:49 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:32:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:32:55 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:32:55 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:32:55 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:32:55 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:32:55 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:32:55 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:32:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:32:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:32:55 GMT
CMD ["rabbitmq-server"]
# Fri, 31 Oct 2025 21:12:14 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 31 Oct 2025 21:12:14 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732b0208544d0f24fed13173f97bd3cac88585b2da9bd65b6804c0a843fea535`  
		Last Modified: Fri, 31 Oct 2025 20:33:26 GMT  
		Size: 42.9 MB (42860345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d498dd8ac22cd265208c03c7e6311925d6a0eb92c5b6ea0fe1ce45beb9936e`  
		Last Modified: Fri, 31 Oct 2025 20:33:24 GMT  
		Size: 9.1 MB (9143878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd961c9618167dd8fd264699e3e4da22348d84b73e23243ceb7510d29de3744d`  
		Last Modified: Fri, 31 Oct 2025 20:33:22 GMT  
		Size: 2.4 MB (2374338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b61556cd43d1e1fe261d39b1d5a54dd7a3cfadd3030540394f1cf84e46cea9`  
		Last Modified: Fri, 31 Oct 2025 20:33:24 GMT  
		Size: 25.3 MB (25266396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a61d3360c9c4708025373372ad2d49acdf2db72e1547352313d3b1112bc56b`  
		Last Modified: Fri, 31 Oct 2025 20:33:22 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f66c2be4940ad059b0043b5a514cad4aaf974940c8cf5be5be9cd43a686715`  
		Last Modified: Fri, 31 Oct 2025 20:33:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f150c3e52aa4712ed5a5114b66f1d4c5d16b906c1b762c4eab70a46e91d4c30`  
		Last Modified: Fri, 31 Oct 2025 20:33:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce3b8c399608a8d07cc961750494aa5fb169e33129ad285af7a5f7c5ea572a4`  
		Last Modified: Fri, 31 Oct 2025 20:33:22 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d585f8cc1a3afe35a3e5dea0092281a277ca5cef2e1c9d7a11b6cfae44f98535`  
		Last Modified: Fri, 31 Oct 2025 21:12:32 GMT  
		Size: 13.7 MB (13712769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4a8590dad3aa1a024389c71db1e50be9c88125a39901fcaf401e7105e6fa22c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1661182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fd23d3da6bd7665a33209f1d4403371e444ad5d51c3a289837c46784de6436`

```dockerfile
```

-	Layers:
	-	`sha256:c9da6b4a51eda6a5f7c6a7d85c350cde67558548b8817c55152120e48b629d88`  
		Last Modified: Sat, 01 Nov 2025 00:53:31 GMT  
		Size: 1.7 MB (1650004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d57e30bb485227d20696eb3fe1a23f3fd39e3dcc9c649a6e85f7cbe15959c6ff`  
		Last Modified: Sat, 01 Nov 2025 00:53:32 GMT  
		Size: 11.2 KB (11178 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:2fcdb7dc4c9106f1e75e8ee59aa579a99f022af58f1f7c903f73b5b11ee1a9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85725122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3011545315e6535aa244303a87cfa6b0199186f48957911a6c8179a945219112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:13:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:13:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:13:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:13:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:13:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:13:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:13:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:13:19 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:13:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:13:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:13:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:13:27 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:13:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:13:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:13:29 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:13:29 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:13:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:13:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:13:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:13:29 GMT
CMD ["rabbitmq-server"]
# Fri, 31 Oct 2025 21:10:02 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 31 Oct 2025 21:10:02 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece8897542c4f43ee106cfdc468e1d0a2bd94977ac55ef96a086318cd503a83c`  
		Last Modified: Fri, 31 Oct 2025 20:13:47 GMT  
		Size: 33.4 MB (33443033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992bab801038429dab8bf295689d9eb3ba5f6e789c8605a3168bc5d0ea3bb9d7`  
		Last Modified: Fri, 31 Oct 2025 20:13:47 GMT  
		Size: 7.8 MB (7788799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3876edb01d71588c3ad65d90bb81d446da11df4d95c66fdd829a82f8e54560f8`  
		Last Modified: Fri, 31 Oct 2025 20:13:46 GMT  
		Size: 1.3 MB (1330060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d3191bb1096264ae3a623fd6e17a89ae2aa93368a490215483205397cfcd82`  
		Last Modified: Fri, 31 Oct 2025 20:13:49 GMT  
		Size: 25.3 MB (25266207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d685bfd4fafe0a6c1fffa92ae642a7cce9653b0b574677a73c60999cff9f07`  
		Last Modified: Fri, 31 Oct 2025 20:13:45 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c87e5fe8e0c37981abd69463e1b7ad58cf6963a229f9e6d40a79e7caeb0e3c`  
		Last Modified: Fri, 31 Oct 2025 20:13:45 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab84621939bd9fcc32679c5eb09c32b229302bf753a1b1e87ec2f223440b9112`  
		Last Modified: Fri, 31 Oct 2025 20:13:45 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6160cf4408f82db86e3196439e645668d3bb1d33e6b198c7cf2cca1ac0db33b5`  
		Last Modified: Fri, 31 Oct 2025 20:13:45 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574b517fe1df3f4e4a6aa9a7e4bf9b72f2be350c9b8b6ec7ed59e8d5784e5442`  
		Last Modified: Fri, 31 Oct 2025 21:10:23 GMT  
		Size: 14.4 MB (14391195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4dde30a6762e9e205e0c15c7c24597ed24b86b31a131e12d6a853ec9184bdcb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 KB (11045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d0947a17c00716f4e9503da4d0791ffd265e1c4223ba738c9187fcc9e6b5c2`

```dockerfile
```

-	Layers:
	-	`sha256:fdc2dd5568f997c9b19f04e00de62464e2e27c436a487a18fdfbb4e8a238f683`  
		Last Modified: Sat, 01 Nov 2025 00:53:35 GMT  
		Size: 11.0 KB (11045 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:1d9145906dd24f5ff4c6bbd74dc7853c7e97b3c03f28b0b66283bc96f664272b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84556068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbe489474eb24f1996f2f546714cfe7357e28f456844323043922faae3cd315`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:15:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:15:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:15:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:15:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:15:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:15:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:15:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:15:55 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:15:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:15:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:15:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:16:01 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:16:02 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:16:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:16:02 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:16:02 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:16:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:16:02 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:16:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:16:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:16:02 GMT
CMD ["rabbitmq-server"]
# Fri, 31 Oct 2025 21:10:46 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 31 Oct 2025 21:10:46 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f39122e09741def5a9a347fdf0b6f869ba4339b9922929c9737317e81a8312`  
		Last Modified: Fri, 31 Oct 2025 20:16:33 GMT  
		Size: 33.4 MB (33390768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644c2cda1699b58bae97011c5025bcd708d1f3ce8f192a568a33beccc5bfb60a`  
		Last Modified: Fri, 31 Oct 2025 20:16:28 GMT  
		Size: 7.4 MB (7390535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e030fecb675a2e11d9b22136c5a6b8e44b65fcb0c54b3e7dab44bb4172e6ecf3`  
		Last Modified: Fri, 31 Oct 2025 20:16:27 GMT  
		Size: 1.2 MB (1227041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca5b5ff4ab88491d981963813be3b5de1ba76fa388f50a797a45c4a4358d8`  
		Last Modified: Fri, 31 Oct 2025 20:16:28 GMT  
		Size: 25.3 MB (25265867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7371c2567cf18ef8fc34ccce36d6b7cd528b571aa862e06a50f01b4518eb0c`  
		Last Modified: Fri, 31 Oct 2025 20:16:27 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa358c951a6830a7c4e1bec712a99b849d5ac971a9ba84b817277aea1fe32d7d`  
		Last Modified: Fri, 31 Oct 2025 20:16:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8984c1ef7cc49fcc7a1c06d4e425a7a65082bc39c20a0ce312646b679b09475`  
		Last Modified: Fri, 31 Oct 2025 20:16:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afc1dec73b72a7e764abfef3d524ac540531b577a9758d5152812ed5cad6227`  
		Last Modified: Fri, 31 Oct 2025 20:16:27 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4eb9e16a96da2ca01aa85b33af4c0ddcf7d3f5115f02de67585175a60bdcd`  
		Last Modified: Fri, 31 Oct 2025 21:11:09 GMT  
		Size: 14.1 MB (14058559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b35b6e1501250bb2acded6d26cf6fea699ce0593c5766613419557678aeb0fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1662294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ea0e3b7b411496e3a2a863f2b38a29fc12bfadbd93ae4861502df50ca93bc1`

```dockerfile
```

-	Layers:
	-	`sha256:1b87cffd9ce7c91bcc5f028c98923fd152322b8d1b785bec47917fa18723bbba`  
		Last Modified: Sat, 01 Nov 2025 00:53:39 GMT  
		Size: 1.7 MB (1651035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3db5974531dfc14257a3f3bd592f7f905bb19591eb92fca6eb21e72c327dc2c9`  
		Last Modified: Sat, 01 Nov 2025 00:53:40 GMT  
		Size: 11.3 KB (11259 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:73c03e2d15cb89800c033fca6680d76ce1e73112d20de92727651c7212f68efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96252415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b89d1561c176213bbecea42f07dc7d72e3c24e7679aaf07cf3f9ad23ce5d11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:15:11 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:15:11 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:15:11 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:15:11 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:15:11 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:15:11 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:15:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:15:13 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:15:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:15:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:15:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:15:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:15:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:15:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:15:20 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:15:20 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:15:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:15:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:15:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:15:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:15:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:15:20 GMT
CMD ["rabbitmq-server"]
# Fri, 31 Oct 2025 21:11:14 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 31 Oct 2025 21:11:14 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a946dae3b29de4499b3e9db8fa0f2d3059e3805fd8797e41ee9b49d8ab2664c`  
		Last Modified: Fri, 31 Oct 2025 20:15:48 GMT  
		Size: 40.9 MB (40852068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc3b20c8b207fe25c5a905463a1dd6177d187c2aea0c5c659f2953a1dff6089`  
		Last Modified: Fri, 31 Oct 2025 20:15:46 GMT  
		Size: 9.8 MB (9824235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fce4720e0c88ede043a6685b150cab2af1cf1a026f966042cbfa42a5c7cbc4`  
		Last Modified: Fri, 31 Oct 2025 20:15:46 GMT  
		Size: 2.4 MB (2424786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce15a6aa1b5d02b995704b9dd00e4035d1093cba77b668d1ee04f3b537c4cdb`  
		Last Modified: Fri, 31 Oct 2025 20:15:49 GMT  
		Size: 25.3 MB (25266418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c9506bc5d5f42e7c5a3a643769be2e8c6f78cb746736d2326a9d19b6088807`  
		Last Modified: Fri, 31 Oct 2025 20:15:45 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960cc215c73c76fcf4146818c4dea3c5a06e3f0f9a97b2ca43f3bc44033a84cd`  
		Last Modified: Fri, 31 Oct 2025 20:15:45 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb18b08c4bd9e018064d0cadd9153ca8aa64d728ad6b00ac583cb7ff829cd3b`  
		Last Modified: Fri, 31 Oct 2025 20:15:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8c4919d681146c61c610b584fd7763491f14eba0d44028b2508494968d150`  
		Last Modified: Fri, 31 Oct 2025 20:15:45 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c4d4740a79039385a48fccd62065a2ba25b4ef20ac277b52594e8e6310dd31`  
		Last Modified: Fri, 31 Oct 2025 21:11:29 GMT  
		Size: 13.7 MB (13745094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:539387784137654bbdf9cd717afd2800aa5d41a3401aba26822e746805f35966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1662167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29808cb7202ed0cf15f98d93c9b24cf25239f49c0f8b8d4fbaa8ad35790217fa`

```dockerfile
```

-	Layers:
	-	`sha256:600aedbbd66d1e1eccad8aa5dc0a39b76c18201aca1ec4e1b0a2d33cc4688cee`  
		Last Modified: Sat, 01 Nov 2025 00:53:45 GMT  
		Size: 1.7 MB (1650883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3744bd45c49ddd3f6258bbf75806ea19e54efd09b31f7d930db1de0f0b0855ef`  
		Last Modified: Sat, 01 Nov 2025 00:53:46 GMT  
		Size: 11.3 KB (11284 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:d2f3cb6f4272ed0c1cfcbe7b3c89acc7ea8af2503bfe4ebc647613fa37ba67cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88152044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1ed03eae475c0ea6c95bbc312e07b1267f1fcb6445cf556f5ea4b1737fa454`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:14:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:14:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:14:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:14:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:14:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:14:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:14:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:14:15 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:14:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:14:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:14:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:14:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:14:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:14:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:14:21 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:14:21 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:14:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:14:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:14:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:14:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:14:22 GMT
CMD ["rabbitmq-server"]
# Fri, 31 Oct 2025 21:12:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 31 Oct 2025 21:12:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee08550e729b6612c1251b2eaf00247f9a6b1d6baa20517a22018ac90d021dec`  
		Last Modified: Fri, 31 Oct 2025 20:14:46 GMT  
		Size: 33.5 MB (33542335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9378f3fc50cb6216cc88e86e0b6b77402c2c3c276e92108244e37010a1ecc756`  
		Last Modified: Fri, 31 Oct 2025 20:14:45 GMT  
		Size: 9.2 MB (9159103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac60a76d27c1b5690e1cd9e25d017d07fa3407a9add304f401a955029ce42c6c`  
		Last Modified: Fri, 31 Oct 2025 20:14:44 GMT  
		Size: 1.3 MB (1332478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f77b2a4e403f5a398659a620a5c9a010d9a20ca4883e3361d7d8e5e8ad8a6de`  
		Last Modified: Fri, 31 Oct 2025 20:14:48 GMT  
		Size: 25.3 MB (25265791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2e3896da60749a415d9a0df99b9391c411b0d8d5cffb0d839ab49e3f2566f2`  
		Last Modified: Fri, 31 Oct 2025 20:14:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689361d2a21e6f7164806ceb04116691b28faa7164e60050c004b93519e82a9e`  
		Last Modified: Fri, 31 Oct 2025 20:14:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c988ae4cc1f631438af0d07d57ffc62079ce704735beda1b3dfa5746effd60`  
		Last Modified: Fri, 31 Oct 2025 20:14:44 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6942f89adffb4c1eaa4364082518b9a1bae64101b3b2bab6dd82c3396b956f`  
		Last Modified: Fri, 31 Oct 2025 20:14:44 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f2b897484047226df200d3850f2cd16638db3990076221919c472cfad6a8ae`  
		Last Modified: Fri, 31 Oct 2025 21:12:30 GMT  
		Size: 15.2 MB (15231663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ddf352c4834c0621660c81ecea0b4d5465f87956331247c0a80b55f334904ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1660955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19360367d20b2fe13a0a0bda45d12e51762119f34fc5dafa888ad217be7d1ee`

```dockerfile
```

-	Layers:
	-	`sha256:9203c8bb3f9c96a8fa0aeee3f469249af22b12e080e5da31ad52cf617311d96e`  
		Last Modified: Sat, 01 Nov 2025 00:53:48 GMT  
		Size: 1.6 MB (1649807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2948f68af1fcbd00efca8a2db74c459036438d7a708ec7f37cd91fe90fd27ed4`  
		Last Modified: Sat, 01 Nov 2025 00:53:49 GMT  
		Size: 11.1 KB (11148 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:b5a662d41e02e6dd10d4687f17c8411893572858528827ac01115cbd160c55ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89541498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e51fe43e444e3a6c7a5907963250e2c376cd2f8e69d5dfc1a7273e1fdc5146`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:20:58 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:20:58 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:20:58 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:20:59 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:20:59 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:20:59 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:21:03 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:21:03 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:21:03 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:21:03 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:21:03 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:21:12 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:21:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:21:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:21:15 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:21:15 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:21:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:21:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:21:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:21:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:21:16 GMT
CMD ["rabbitmq-server"]
# Fri, 31 Oct 2025 21:11:56 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 31 Oct 2025 21:11:56 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde3b0587238eafb4757f1505ee9693980a934e68c7f7abcabe5dcfdc544831a`  
		Last Modified: Fri, 31 Oct 2025 20:22:05 GMT  
		Size: 33.9 MB (33925474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb1cae72f876f7e77ebe4db3c09a4bb5b6e826cffe0e37b6b043e62f47a44ba`  
		Last Modified: Fri, 31 Oct 2025 20:22:02 GMT  
		Size: 9.8 MB (9774072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cdff811b99fdab5bb1c04dded6d014c3612bcc44bf1cea5fc9ee09bad2e422`  
		Last Modified: Fri, 31 Oct 2025 20:21:59 GMT  
		Size: 1.5 MB (1452616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5605c5ba6654595ad2e8202fb1bb3829acad6884f0a9a1ef98145dec0212112f`  
		Last Modified: Fri, 31 Oct 2025 20:22:01 GMT  
		Size: 25.3 MB (25265867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41287f194fd7915aa7bdc32fa37b866a5c37f70ef9be6d1a71025427ef25f926`  
		Last Modified: Fri, 31 Oct 2025 20:22:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797e693acc3369faf32068aee8c5aa75c5cc412cf7f9ce5dd783cf93637e04ee`  
		Last Modified: Fri, 31 Oct 2025 20:21:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62efc6b1c57df28d871195aeef22848ce2b9f7875f03d6dbb8babfeb751e8c3`  
		Last Modified: Fri, 31 Oct 2025 20:21:59 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdbe0030b7110c49ea3ac8a50aa33f76d138817fe4fd890406ac14a658232c0`  
		Last Modified: Fri, 31 Oct 2025 20:21:59 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50ffa037264137fc0ac3f3a71ad2a0221a853308e91202f047b8f37c2e4b11a`  
		Last Modified: Fri, 31 Oct 2025 21:12:23 GMT  
		Size: 15.4 MB (15389476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cb40cc036da719f4770a1788454c51de1a10ddad5c2df9cd2304b4a65bc7c451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1660478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec5e389b88b11efcb07446b1690a4bb6d6d026c6af1fdb2272eca8a31039797`

```dockerfile
```

-	Layers:
	-	`sha256:6f05820c7745166167846b4003bf1ee68aa87b0292ff4a4084896d7a6fb580c3`  
		Last Modified: Sat, 01 Nov 2025 00:53:52 GMT  
		Size: 1.6 MB (1649254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68376320dd2435da1823b5d3ecdaedc8340006d6fef2442ee0ad690e2c57551c`  
		Last Modified: Sat, 01 Nov 2025 00:53:53 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:2e2412ba2be3f32f76216ff61d87755f232e612d6881c4543e800fa86b54130e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90815381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9803f539866b2ad0489f641e3571fce82b4890f965294aaa64b60661249d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:00:41 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 23:00:41 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 23:00:41 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 23:00:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 23:00:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:00:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 23:00:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 23:00:55 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 23:00:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 23:00:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 23:00:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:01:34 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 23:01:43 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 23:01:44 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 23:01:44 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 23:01:44 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 23:01:44 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 23:01:44 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 23:01:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 23:01:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 23:01:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 23:01:45 GMT
CMD ["rabbitmq-server"]
# Sat, 01 Nov 2025 03:05:15 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Sat, 01 Nov 2025 03:05:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10134cdd10881c5b8872bd6a22cdee3d4f7947cf07d56bcfcb67b233a15d9c12`  
		Last Modified: Fri, 31 Oct 2025 23:07:28 GMT  
		Size: 34.9 MB (34893302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc84479dee5ea17251ec65d2bf63013f46012984d82cfc0dacc6fa4e7eb030c5`  
		Last Modified: Fri, 31 Oct 2025 23:07:26 GMT  
		Size: 10.9 MB (10906600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdf1244b1015e4f3abc2025a38925d773a84d3d23c8714af5da707a897f52e2`  
		Last Modified: Fri, 31 Oct 2025 23:07:25 GMT  
		Size: 1.4 MB (1366493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f4fc003ebbc648006e42a148cf719e3feedb9f149b92374c03280473701263`  
		Last Modified: Fri, 31 Oct 2025 23:07:26 GMT  
		Size: 25.3 MB (25266245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d2996778974410b330bf379c00903a3c4ce56446833a9a35bc6536e6a847ac`  
		Last Modified: Fri, 31 Oct 2025 23:07:24 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f45fce4291972f5f7b9e2062982b27b38e93f4c4fdd45f7295fc1b4a5754c1`  
		Last Modified: Fri, 31 Oct 2025 23:07:24 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b03d9a6ea73b622b2b8f9cc00a18a440a39bfa753b3e610d5d4c090005e4e5`  
		Last Modified: Fri, 31 Oct 2025 23:07:24 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbca45694e03cab13dfd5bd528aeb3d3f90eb8147368710ebbb3ab1902a19ae`  
		Last Modified: Fri, 31 Oct 2025 23:07:25 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db5799ab7f4cf20256aeb24d63eff42b011ae75fc428c0c50d14a68ca258cd1`  
		Last Modified: Sat, 01 Nov 2025 03:06:44 GMT  
		Size: 14.9 MB (14865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d9fcbeaed220a26d20d95422ef7a48f43adfd009c6cafd97f16d2149c77f1762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1662089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae8d077ab26644e0236e6a9b6e5f75bd65a64f3d45da29d0a6a70a107f4bf36`

```dockerfile
```

-	Layers:
	-	`sha256:cba9c526d4b0fe29643c49ae09330757a6c7251ba3cead20f03cf54d9dcd4a35`  
		Last Modified: Sat, 01 Nov 2025 03:52:56 GMT  
		Size: 1.7 MB (1650863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1220ffbc2a9fd39157b7d726b872f05df70bdeb24a45266298e9e683794fc8f1`  
		Last Modified: Sat, 01 Nov 2025 03:52:56 GMT  
		Size: 11.2 KB (11226 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:32416029ea4a650291f0f18d956703696f737ce1311483e9d702833e5ef2d648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88059621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f2108856fc1540b9cc64b1aa51be077b9f02bf2ff82ad98eada410f017a8d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:23:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:23:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:23:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:23:58 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:23:58 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:23:58 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:24:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:24:02 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:24:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:24:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:24:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:24:16 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:24:17 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:24:17 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:24:17 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:24:17 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:24:17 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:24:18 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:24:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:24:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:24:18 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:24:18 GMT
CMD ["rabbitmq-server"]
# Fri, 31 Oct 2025 21:11:27 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 31 Oct 2025 21:11:27 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151f10fe2d5970a93b2c09548b23918d27bebe3e729d40d18d105c927642f22e`  
		Last Modified: Fri, 31 Oct 2025 20:25:04 GMT  
		Size: 34.0 MB (33968406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbcef3ee149023b862d4a5c01ed000b7fe1681669f9d8c804eef402cca769ab`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 8.3 MB (8347157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc7a38ee1fe3901818cf81de72c1870a6b79011fef3b3611a15bf1da29e0956`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 1.4 MB (1430649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735665edefcf2aad4d55873503deef537e0b49d462265a8b17fc79f095b37578`  
		Last Modified: Fri, 31 Oct 2025 20:25:04 GMT  
		Size: 25.3 MB (25265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742e635b9f74cfb089d934abae9fdfe3b17ce487a6dfee24efaf182551ae3167`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986382df115e6dc31f54750e52b580a296073f3a0dd12ce90362757849e340b`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b932a6beae64243460533130ac7459630af3d0d44a748cb7d6c9be9f8ebe42c8`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c0e48355b01996594567359c479d344d831f665c938466c42aca4ad450b5ed`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc0f62dac12621febedefc1746fef389a08c924250e89ffaf2da01132e7a5b3`  
		Last Modified: Fri, 31 Oct 2025 21:11:47 GMT  
		Size: 15.4 MB (15396521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:41ad6834ab2ff0d708525729e0d92f73b442bb311a534bccc5b1a9196036b970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1659884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a413cd0e534fa9b7e697a45af9f907d5f2637cdd753b0fa24d1db63c437fedc`

```dockerfile
```

-	Layers:
	-	`sha256:98dcd96f3525e7fb35288b9ca192d54810533d07ba49d96799f9b79a755c85e0`  
		Last Modified: Sat, 01 Nov 2025 00:53:59 GMT  
		Size: 1.6 MB (1648704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb7881e1f4c93dd3943a6bdbc7c3a6617b870f50b146ab2284e6c0fb04e7b8f`  
		Last Modified: Sat, 01 Nov 2025 00:54:00 GMT  
		Size: 11.2 KB (11180 bytes)  
		MIME: application/vnd.in-toto+json
