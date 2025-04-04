## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:b3bc6940c1e5ecd90f70cc30627d252070155230f89d36a953245551ea308ac2
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

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:0b14ece7fd496eb5b2863bb6e4fe22ffaf3c592701da86a7447a5431a0324ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75405117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9102c2d6068549954e6638cf96024aa97630501d0738d62ade4144fb2b926c4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9809225fc17d770339a70608b78bdab58f6de1686d55e8c98e7a288d6df91d1`  
		Last Modified: Thu, 03 Apr 2025 22:14:50 GMT  
		Size: 42.8 MB (42835299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99c583726cf22f0903d7baf5dfb5beaa2c836ab8e923b70dcf74c3aa47398be`  
		Last Modified: Thu, 03 Apr 2025 22:14:49 GMT  
		Size: 8.3 MB (8311665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3784a9a77ecbc6e1f9ee8bd3ee43a29e32e2da2ff120fb9393b3f7d03e19be09`  
		Last Modified: Thu, 03 Apr 2025 22:14:49 GMT  
		Size: 2.3 MB (2279302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a310652ea89954de139bc2e74450f526df935a4ea6d4e46a7edd8cf531b45f`  
		Last Modified: Thu, 03 Apr 2025 22:14:49 GMT  
		Size: 18.3 MB (18334854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0afa40971e54b1fbd3133e092be4048a2a8f8feb38d30b4f6b1bd4310923f4`  
		Last Modified: Thu, 03 Apr 2025 22:14:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0a25f3596af947714922a778ddb25607bb5a2c5a84c0dd8576cdf66abef89d`  
		Last Modified: Thu, 03 Apr 2025 22:14:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30e1b3c466bd8b0901f89499fa157d1a2b044d3cad3362d3faf4f6588aac183`  
		Last Modified: Thu, 03 Apr 2025 22:14:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af93964ee2be1db48e04dfa973277e9fd2f838456ef2a940f7fdddd101494412`  
		Last Modified: Thu, 03 Apr 2025 22:14:51 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5404a13c42ce60ca34f5cd7b2ebf072f2389af75de589cee1f8ad38987a4b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6726508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c290911bc0bcd60cdad0f5cd3099d1200331b751ebd3821e6442b2318978db44`

```dockerfile
```

-	Layers:
	-	`sha256:9ae03c01a2192c608f3d624b8f8b32696a736e16b6ab1cf8868347ee0141612b`  
		Last Modified: Thu, 03 Apr 2025 22:14:49 GMT  
		Size: 657.2 KB (657208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b043982a0e3db0087ef0319a982bfeb6343dbc9819c3113fc8a3c79cfd3c3a3`  
		Last Modified: Thu, 03 Apr 2025 22:14:49 GMT  
		Size: 3.1 MB (3081276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5aa329cb48767a9a36a3d7b8adc69a9127102f7998b05ecaa8fd021c3f069cc`  
		Last Modified: Thu, 03 Apr 2025 22:14:49 GMT  
		Size: 2.9 MB (2928081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:811be7b79b5cd90041c708c37ba0d2bb99927e687ecd661de6fa116da5203828`  
		Last Modified: Thu, 03 Apr 2025 22:14:49 GMT  
		Size: 59.9 KB (59943 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:00e46c0f9811c9f7f87109d6a23112ec61cfac3c0568e2735af47498c177a558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63444602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175802cd8b27ca1aec9cdf2f8083fb14bfcfd693f534583a1c5ee03a15d90c31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a55b2f5e488e823fbd111f0939605cce2da33278258122d3a707572be392a7b`  
		Last Modified: Tue, 01 Apr 2025 23:56:40 GMT  
		Size: 33.4 MB (33418452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e16ef0db499d929b930eb0f9e97af956663e0391ef4184e140ffdc530cca44e`  
		Last Modified: Tue, 01 Apr 2025 23:56:39 GMT  
		Size: 7.1 MB (7097976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688eb3f72eb5c1a7ff998aa57bcc12e8a4f1db143ca937c9b587a14835040118`  
		Last Modified: Tue, 01 Apr 2025 23:56:39 GMT  
		Size: 1.2 MB (1226986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c565d6268a3a498527804dd76e4fb22f8ba101ad3cf5983352b0878c9b9177`  
		Last Modified: Thu, 03 Apr 2025 22:07:17 GMT  
		Size: 18.3 MB (18334710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe528c51bd748b56d75357eccaf8a6164f55ea4bb2ac4b3e0618b703df18ef`  
		Last Modified: Thu, 03 Apr 2025 22:07:16 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca96eae03cfdaf66be337834a2b37a05d8fe3f5636e594b4d1824069685d47b`  
		Last Modified: Thu, 03 Apr 2025 22:07:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11ec0ed6fece74b7095070d9443a2d52baa18105b7d191cd6afc323c48c8471`  
		Last Modified: Thu, 03 Apr 2025 22:07:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cec29ca305900b7008ba3a101628830fb7951fc98b3534a11d32cf3bd32ba2`  
		Last Modified: Thu, 03 Apr 2025 22:07:17 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a3396b42aa6018eb79ee47cb3d1f3bd9e66c77fec7225e9dc5c9298d02223ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b828c59340788fe7833b3c7c64e09e9edae4e5e5fef0d1f18feb4579867e83`

```dockerfile
```

-	Layers:
	-	`sha256:79a5ec114ffa3d15b75f23367f5467e769901d4490cc2936e874374160b72965`  
		Last Modified: Thu, 03 Apr 2025 22:07:16 GMT  
		Size: 59.9 KB (59921 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:3a41939493ce9725b73ca0d772a968483c48501c7dc0aaf120a9279b71d25069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62682404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07f184b4ad6ec1960b8fd5c8ed34dad21fee4f22faf67a2ea196171e8fed18e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124771d2b310197ed572773255f7f440a032492dc60c539838bd69751e3052e`  
		Last Modified: Wed, 02 Apr 2025 00:03:44 GMT  
		Size: 33.4 MB (33371537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ca856bf647875419538da62eaedb7b98b18de4b61a870e02eb67c5b08fdc81`  
		Last Modified: Wed, 02 Apr 2025 00:03:44 GMT  
		Size: 6.7 MB (6742211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588c1066887ebf38b6da1beb13dd1c34230700b4fe2519e2ab6b14ab4567e025`  
		Last Modified: Wed, 02 Apr 2025 00:03:43 GMT  
		Size: 1.1 MB (1134778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ae76d7b68a4cf869dfde27d13b04590d922702464ca62c78a211657ff602d2`  
		Last Modified: Thu, 03 Apr 2025 22:09:49 GMT  
		Size: 18.3 MB (18334012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee736caee8cea73dc6ca57ffede807240c165075f627b7b81a5889b2bb52087`  
		Last Modified: Thu, 03 Apr 2025 22:09:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325625f29d96d950721dbc6001e88073ec5867b5267e206f6539b1a37f260db0`  
		Last Modified: Thu, 03 Apr 2025 22:09:48 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4263ff0e5b735bb52b61daf3f866ee0cf8e96bd694f8a1269f7654970d3c78b9`  
		Last Modified: Thu, 03 Apr 2025 22:09:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab1427f52ce0da484cdf10726e89eb75d40e8da690cee1756740c93a1698ac`  
		Last Modified: Thu, 03 Apr 2025 22:09:49 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:00194c209c4a50acbb37a735197705209aabdb35bdf3536708c4257cbfeffa73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6493228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52968d14decffea1116537c4c15b60b9f7654c9c885e95802a8f28358d314d42`

```dockerfile
```

-	Layers:
	-	`sha256:932a35c378467408914c9efd91de1feaedc4f5641595dc23b119dc62f60b2191`  
		Last Modified: Thu, 03 Apr 2025 22:09:48 GMT  
		Size: 653.4 KB (653353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35efe0bfcf1050f55cc05f0815360157c5c75d3c05304e653415d23d9af92060`  
		Last Modified: Thu, 03 Apr 2025 22:09:49 GMT  
		Size: 3.0 MB (2967130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a07e71fef47995b77ab57fe0c20885b152d6b275871b9fceea93cff679fb51`  
		Last Modified: Thu, 03 Apr 2025 22:09:49 GMT  
		Size: 2.8 MB (2812610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29599192e40a6162052b6f72e2605c623db6d6f74f5f483f353b4ab13fcf303`  
		Last Modified: Thu, 03 Apr 2025 22:09:48 GMT  
		Size: 60.1 KB (60135 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:582d88b22e505b42c29fc090ba6c4f00362b03ff83d5cc1b1f1879cc95f50eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74510592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7362c2156d648168f87c6aca3a9aafb183864d516618d88d832783721e0b24ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8c869b1d672b88a21301fe6b0ea13adbd5ba0af312ad6032564938fcecb7b2`  
		Last Modified: Wed, 02 Apr 2025 00:03:58 GMT  
		Size: 40.8 MB (40822105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0eb100648560b3c265f54d33eaf250227be88d6ed127792c2b331ecbcd3bef`  
		Last Modified: Wed, 02 Apr 2025 00:03:57 GMT  
		Size: 9.0 MB (9034850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42657e19f3cd3a504ea681ed24f5d8756533644090e8f8a74225403042e03c1f`  
		Last Modified: Wed, 02 Apr 2025 00:03:57 GMT  
		Size: 2.3 MB (2323912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa93422202d8878d5e764267e153b958a5f70326af274b4121cb27e0cec1132`  
		Last Modified: Thu, 03 Apr 2025 22:15:59 GMT  
		Size: 18.3 MB (18334947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df64d4542c5e2e8fddea4bc64ceaa13a799791184b5314e3e261ba1ecf2a101c`  
		Last Modified: Thu, 03 Apr 2025 22:15:58 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1541afa0914c1c726d183ad53e74f8561f5652dc38636faa5bcc3a2d2dc71aff`  
		Last Modified: Thu, 03 Apr 2025 22:15:58 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499cef224ee4d8a6c24fec742f42192a2d45fe4602aba670b695ac16fff5582`  
		Last Modified: Thu, 03 Apr 2025 22:15:58 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a979c5fa957fcdfb14c0dd10e9f83f584f54c44b4f4e2724ea4c5982c309e1`  
		Last Modified: Thu, 03 Apr 2025 22:15:59 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8393e97eb2f44ccdcfe5e7e6ba6afc80ea2ff796fa4513765c824dedab07ce7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6835836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc14191c630e52d657df59116a1fe74abeaecb99b46c6a78aaf062d0309af729`

```dockerfile
```

-	Layers:
	-	`sha256:430a6975644067ab3aac2f23e5a0a8869c02c2ea98e7cc31b38bfbeb011fe7fa`  
		Last Modified: Thu, 03 Apr 2025 22:15:58 GMT  
		Size: 658.0 KB (657999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6251dcc018ec70bab13c9bb0c80f08921b730e8fa448b525aae425594a076814`  
		Last Modified: Thu, 03 Apr 2025 22:15:58 GMT  
		Size: 3.1 MB (3136085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1786ae2d2546f0dd299ca3407e2f7a90ca5adc2db18c7723d2d0d796020dd01f`  
		Last Modified: Thu, 03 Apr 2025 22:15:58 GMT  
		Size: 3.0 MB (2981571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8da1c22a491b75b48b4a960f6c81e08506d5ad049a2a093d734439b2aec005c`  
		Last Modified: Thu, 03 Apr 2025 22:15:58 GMT  
		Size: 60.2 KB (60181 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:b6dff74d673c57b3ef65bae7245eaf9d90faab32b39e7489a361bfea29eab945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64872127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5166e7e3308ed8fb73ba8f0a4dd3027fe0124393815b6e22ac280c186c659f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d22468f9121d92253771992144090c98f60cdccd9f462b6bdc056ec5cbbe409`  
		Last Modified: Thu, 03 Apr 2025 22:14:59 GMT  
		Size: 33.5 MB (33517263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d3292dc3353620315c2ac355b30ff0c41ea2b47cecb164f1496b996fb23a1e`  
		Last Modified: Thu, 03 Apr 2025 22:14:58 GMT  
		Size: 8.3 MB (8324833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2585c6dc8ce9305efa1c62c4c44a470ba582ae0dfc619f2ddbd42bea97a8fb1`  
		Last Modified: Thu, 03 Apr 2025 22:14:58 GMT  
		Size: 1.2 MB (1230633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1293aa54b846b73599104a2d70a2c0122cc4cf3dedb8b292152a6111e5fbde26`  
		Last Modified: Thu, 03 Apr 2025 22:14:59 GMT  
		Size: 18.3 MB (18334025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d36e062a950e958daac403022655387bbc03df48b8578f1ac78041e2159a06`  
		Last Modified: Thu, 03 Apr 2025 22:15:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d2a0971e3974831a705513f719c55025c852825143fc3d97574255331fbf5e`  
		Last Modified: Thu, 03 Apr 2025 22:15:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701ceac9276bc40549991a35631466faa3537aaa4dc8e329729e6d146805ffbd`  
		Last Modified: Thu, 03 Apr 2025 22:15:01 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5676e6d8d94bfa64ef78182ed9e175930fd410bf6d3ddd54111821efa8540ce7`  
		Last Modified: Thu, 03 Apr 2025 22:15:01 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d1c0e4579e73aaa7382b0318bd3da6afc0919d784b8006e1fbf59e67fd2f64df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6699703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a37b077d13e3c76e1bce9738ad7d38c26f58408b1c48ec29d1ed26ab53ead89`

```dockerfile
```

-	Layers:
	-	`sha256:4c5b5ca69616f35decb787a19352f1deafe6c04ab684f1f1cc2cd7da86381ca1`  
		Last Modified: Thu, 03 Apr 2025 22:14:58 GMT  
		Size: 652.6 KB (652557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c402edd59daf72956f7696a1a80e19a113a1722f537377fab7fdeffd36b1ce5d`  
		Last Modified: Thu, 03 Apr 2025 22:14:58 GMT  
		Size: 3.1 MB (3070222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6ddee200a82b1588165d8c4ccd951e10171ea600ebc139d22d58761ba2585d6`  
		Last Modified: Thu, 03 Apr 2025 22:14:59 GMT  
		Size: 2.9 MB (2917031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9690090a561e96496c63da93ce495da8ed5850fda1acd159a55513ad4020e0`  
		Last Modified: Thu, 03 Apr 2025 22:14:58 GMT  
		Size: 59.9 KB (59893 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:a279d30add125cbfd74ad22a19c9ad5ae7435f5f7ab7a2cb5d76a48e26e420c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66003479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7581bddd1f17925a0fa4fbd56da9446704d9773fd99e168c78429929d8ba75ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e09c3b192c12cca4292b0519597bea0529568d6bd5b2d1c078672778dd5da6`  
		Last Modified: Wed, 02 Apr 2025 00:05:07 GMT  
		Size: 33.9 MB (33898567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73d6376b3f923151192f99d4ff0900fc2a124fef487477ad646fae2789f851b`  
		Last Modified: Wed, 02 Apr 2025 00:05:06 GMT  
		Size: 8.8 MB (8848328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05199de0356e528bdd0375c44ec1b54ff02904293dd8430a7f077eefe19cc87`  
		Last Modified: Wed, 02 Apr 2025 00:05:06 GMT  
		Size: 1.3 MB (1346521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9645c2faa8b6a420c8b43fa107f12295087b1879eeab49c7cfe0aab3ef181a0`  
		Last Modified: Thu, 03 Apr 2025 22:17:20 GMT  
		Size: 18.3 MB (18333967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8645a0d216f0154f6afb14e42382c9a4ba890667458fc85d82ca0c7ad41cbfd0`  
		Last Modified: Thu, 03 Apr 2025 22:17:19 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48e45d95c6456007370fdad4fe1ded851d6284da8d2b50a4d830dd4882ec156`  
		Last Modified: Thu, 03 Apr 2025 22:17:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aefea3e79da4b95f6ce0c0b8898bc2ff242ff97bc71045b18a8aaa9ec532782`  
		Last Modified: Thu, 03 Apr 2025 22:17:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4089af64c3022c2038a7d71ef3dc7e5efb9e22ce2a8f231bacaf089549d3fcb`  
		Last Modified: Thu, 03 Apr 2025 22:17:20 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3bb8b0c8efe5931a10d30a4cc9f0b44e5031e9ee0752905f79f6767353aac903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6731507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be26af16c08758a897d2fbb6eec97e1681ad22bb4582618c848ee8d6b0d4113`

```dockerfile
```

-	Layers:
	-	`sha256:6060f28bf0897eed874de0c6d965e350abfdf1b5955dde9bba009d2c39e55bca`  
		Last Modified: Thu, 03 Apr 2025 22:17:19 GMT  
		Size: 651.4 KB (651400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9577b7fe91cd68c7092d60cc2886f35efb2ec8e3c07fbbf72ba8953da131ba62`  
		Last Modified: Thu, 03 Apr 2025 22:17:20 GMT  
		Size: 3.1 MB (3087314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f6ee20e3a43c6863754ebca53a2716f6d8168b8de624558d1790a32dffc0fd`  
		Last Modified: Thu, 03 Apr 2025 22:17:20 GMT  
		Size: 2.9 MB (2932788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc121c73e17804e02f07d6bebaaf6e93e47778b71d671f88c7eacfab1e6cfcc8`  
		Last Modified: Thu, 03 Apr 2025 22:17:19 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:7ff6541ff890b18f5d3648ff6f834dfdb0fd4341b5784427836536725ea5881f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67689666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5896d6caf675c48142f8f27411702199cc73b9f1ba2026cbc25ecbf6cc361b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d174e7cb9aeee95e3f6d1a16883b54f2b2c3a01758251a8f3b67830e863d160a`  
		Last Modified: Wed, 02 Apr 2025 01:05:10 GMT  
		Size: 34.9 MB (34876429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bf4b61f3f0a6cfa05907c859822d7aed7eaa682bf5881a9f7f89b507914649`  
		Last Modified: Wed, 02 Apr 2025 01:05:06 GMT  
		Size: 9.9 MB (9858935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38450cd746523c751db6769bc9d0dfb4f0466bd51db8375b278ca1abcddd481b`  
		Last Modified: Wed, 02 Apr 2025 01:05:05 GMT  
		Size: 1.3 MB (1266438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370a6afa4f426b3d9a8fd8a5d7b8dc32dd13d80f481942b13cef28193406ee9`  
		Last Modified: Thu, 03 Apr 2025 22:22:28 GMT  
		Size: 18.3 MB (18334676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b96bd073a55d8e56a9c6c2f4d0d4d6f583b9c5b610c0011d6ad07ccfc8aacf1`  
		Last Modified: Thu, 03 Apr 2025 22:22:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91a8448d50966228a4dc0dcc139c0d3d46997fc5540b7b70d14021acd02e4fb`  
		Last Modified: Thu, 03 Apr 2025 22:22:25 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc1010639b9d889e4435cf2d30e5f82812956d31adaa7acdd1d0eba479a404c`  
		Last Modified: Thu, 03 Apr 2025 22:22:25 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8569e33273086ebff07745b786ac33bb9af3da0dc8187047c88f2014b2677ce8`  
		Last Modified: Thu, 03 Apr 2025 22:22:26 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f9c92db50228175fb8ce8ba10f79960119b30d3b9ae6d3bfa862cf9f2bf6bda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6809621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4f01f7b913f81cbf2177ac59a3c3b2fba12552cba265970d01d8a63bc83231`

```dockerfile
```

-	Layers:
	-	`sha256:5ea86a568ddc46c6bdf64def5817f3b6bbee450075ca1a649392d1158e85056a`  
		Last Modified: Thu, 03 Apr 2025 22:22:25 GMT  
		Size: 654.2 KB (654192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f1ab38425a49130db7c333542e4f3a23be87cb92f040a85b3207e96913c3ca`  
		Last Modified: Thu, 03 Apr 2025 22:22:26 GMT  
		Size: 3.1 MB (3124969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d658414021bb40e49641478fde50b1e52c57f841856165147de60c8da00c7726`  
		Last Modified: Thu, 03 Apr 2025 22:22:26 GMT  
		Size: 3.0 MB (2970455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be4d658687bb82d5487f73be4a837a1451c8f1aa15f0ad62e0782198a382a28`  
		Last Modified: Thu, 03 Apr 2025 22:22:25 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:9b5eaa9b96233f9d31499344f7cbe4b47851f60d0e55f7ee3fa52e5087267260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64587069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d42d1df7f69523f9f8569f947131cc767b6202ccf4863991c082031284b4f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Apr 2025 11:05:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_VERSION=4.0.8
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Apr 2025 11:05:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Apr 2025 11:05:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Apr 2025 11:05:21 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Apr 2025 11:05:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Apr 2025 11:05:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 11:05:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Apr 2025 11:05:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Apr 2025 11:05:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4a428caebdd01dbb06f3d86bb2b92b865ad2d9fa9b228e0c9f6975129fca1e`  
		Last Modified: Wed, 02 Apr 2025 00:05:14 GMT  
		Size: 33.9 MB (33948141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a523212391c92f54c599cf792ba6fed8af8db9297bcaccd5b1a08de994502`  
		Last Modified: Wed, 02 Apr 2025 00:05:13 GMT  
		Size: 7.5 MB (7510931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aaf40ef8985e91c2900bc12ce6c4cb089ffb5251a04129a6f6782e50fef707`  
		Last Modified: Wed, 02 Apr 2025 00:05:13 GMT  
		Size: 1.3 MB (1324679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1ff162dc1309fcbf302b57e677050bfa8cf9e9b7fdabfde9ebee671998088e`  
		Last Modified: Thu, 03 Apr 2025 22:17:54 GMT  
		Size: 18.3 MB (18334001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1336082446128bc4b8cecf75c5a35600d6a23da33e1a03086f5d285c340f3d0`  
		Last Modified: Thu, 03 Apr 2025 22:17:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7feab54e0c38635ed1049d4f5e7ebb6b24d083f31cbaa0f162e6b11950cfacb8`  
		Last Modified: Thu, 03 Apr 2025 22:17:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6889bc9e3bad39bbd92a274d519a1d8cdcbd2833b2b7c69b871c9955df1596b6`  
		Last Modified: Thu, 03 Apr 2025 22:17:53 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e641522b5b30c928170ede7b134fede502f513c2409844f08e16b427578a8c95`  
		Last Modified: Thu, 03 Apr 2025 22:17:54 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c938d2ad8446526c17872effda1a690aa210278dccf4389eb3e2e301f6b14470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e21d9458594c144ab0e237ef0efb1e458a8eba12223867718feadc5a77b44c`

```dockerfile
```

-	Layers:
	-	`sha256:82ceb964210e24d59ae56a7932cd279417fa1a39ac824999cc97e89f00d20c5a`  
		Last Modified: Thu, 03 Apr 2025 22:17:53 GMT  
		Size: 651.4 KB (651366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2efbe849cb7d8a91ef33267dcaf3459abfdb42fa800b5191b77a7881ac89271b`  
		Last Modified: Thu, 03 Apr 2025 22:17:53 GMT  
		Size: 3.0 MB (2977281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c1e500d16fb329e9261119822390e551ec444792f0d317eb2ec421f7280b2c`  
		Last Modified: Thu, 03 Apr 2025 22:17:53 GMT  
		Size: 2.8 MB (2822785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e29f0fa78753883dcfe4f0ac887ff51e4b90878ca616af2b08f3845db312892`  
		Last Modified: Thu, 03 Apr 2025 22:17:53 GMT  
		Size: 59.9 KB (59942 bytes)  
		MIME: application/vnd.in-toto+json
