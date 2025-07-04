## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:f5e6901ecb59ecbfa2134ea5019bf189a1bfbf10e808d71d1556eaa95df968b9
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
$ docker pull rabbitmq@sha256:bdc190777a84725314fe8b62c70f17978b88c2c6d6f2f6b20b592554ae9580c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85922782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048099d1b2672f1c3779a59a2a7e9e4d716aaa802e0d4459f396173e64c94300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Jul 2025 17:05:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_VERSION=4.1.2
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Jul 2025 17:05:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Jul 2025 17:05:34 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbb2983d688e9d69fec89f8b27d60827c984283dcf29c490b31f615c892a014`  
		Last Modified: Thu, 03 Jul 2025 23:16:32 GMT  
		Size: 42.8 MB (42829456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cece7c9582f9cfa977b90be1484c8fdee511c72ea5348b3d7a65b824ea551e`  
		Last Modified: Thu, 03 Jul 2025 23:16:29 GMT  
		Size: 8.3 MB (8314121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ff3b7ac55efc02b3dadfd1b9b52fbe07044a038f662fa73a3ff30665472b1b`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 2.4 MB (2374092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68189c13f0e33cafe91a433fd891a2a892b84a6d0ce6de966bae8d08e38105a2`  
		Last Modified: Thu, 03 Jul 2025 23:16:29 GMT  
		Size: 28.6 MB (28606518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38f258188d4f3c33b98dc04cd4feaaa5bf4bb1b41454153eed28e91303ce588`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e3eecf446b667dcb98e03511e7c95ed77490672952e7944405d35022005c97`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d21a72854cbe08c7235cee914aa7dad1b0a3965dcbaf6ca0076028580b2766b`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06039e082aabc3ee29eab98ba4eed813453f35891da9fe9253e3528ce2e2f60`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7e73bc1c41d92a31e9e6397543afcb988ea28a685f4b2ec1affaa33f673f0357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6783066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b4cfa988cf645db82c2d876648cc80946d28aa7d1e94fc1e3036b4fb453b7a`

```dockerfile
```

-	Layers:
	-	`sha256:c6044c853853e53b9182798a0dc8105e1236fe2faa39d35998751ca76cc029a6`  
		Last Modified: Fri, 04 Jul 2025 00:52:48 GMT  
		Size: 671.3 KB (671316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd94b8762b07982d3bd2724cc968a93cfaca690d94d2118d4f01c10f43e38534`  
		Last Modified: Fri, 04 Jul 2025 00:52:49 GMT  
		Size: 3.1 MB (3102656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cf7b8886dfd37da5fac8e9b5ed570f623416994a5b19f1eb1b65f22b949b857`  
		Last Modified: Fri, 04 Jul 2025 00:52:50 GMT  
		Size: 2.9 MB (2949137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263bc1f4ff8e6ef46dd5d308ea4a92b9568013f8812f95281e718fbb837878f4`  
		Last Modified: Fri, 04 Jul 2025 00:52:51 GMT  
		Size: 60.0 KB (59957 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:eed5909ed14d9c66bbf69b462439849dd29527bbe44aafefd87222c636cef5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73983812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2e05099272ea337d3f65b921abb8ebeec1b0ba265ddabc5a857eaf42a30dab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Jul 2025 17:05:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_VERSION=4.1.2
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Jul 2025 17:05:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Jul 2025 17:05:34 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69d534da3a790801ea8261728479a42a3323c5e330cae07abe621497b43597`  
		Last Modified: Tue, 01 Jul 2025 22:17:04 GMT  
		Size: 33.4 MB (33443998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fa21bd4410973499a361c466fc20724261eda59e5ffdc57d566a28eeabd18c`  
		Last Modified: Tue, 01 Jul 2025 22:17:02 GMT  
		Size: 7.1 MB (7100791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daea1c4aebe56c9b41a05f140e503b18b746d2f4ec37fd579614e1b3036cc3c2`  
		Last Modified: Tue, 01 Jul 2025 22:17:02 GMT  
		Size: 1.3 MB (1329819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd45b753d62b66549043b5bdec853cd2a3386897043e5c8346ac8b8a84a84b3`  
		Last Modified: Fri, 04 Jul 2025 01:31:03 GMT  
		Size: 28.6 MB (28606522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4fc5353ae379d1509656484d32de9ec765d31628f3c3700611bf29374464cc`  
		Last Modified: Fri, 04 Jul 2025 01:31:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32d9bff03b917e980c7a32a2e13ca34d6b73ac14b005675d507ed1f79248c75`  
		Last Modified: Fri, 04 Jul 2025 01:31:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e602a84bcb390537ffe526cb1dd21d69884ad90f62ac63492ca67c8cb1a90`  
		Last Modified: Fri, 04 Jul 2025 01:31:00 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf6e244570b06c8528a504617b577d42c815f8df4b4ee169ecb91933d264444`  
		Last Modified: Fri, 04 Jul 2025 01:31:00 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1c5cccfd138faebf80d01f2704aafd90d53a9730d209766692762d8ba20ee0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d428ee5e75d02ed693e166d6bcf6e8cb84a7c953e64173ea1f1cbfcd3c6df4`

```dockerfile
```

-	Layers:
	-	`sha256:efee49ae39f1454f7ef885a41da83daef45da8a9acdbc4ec188ef41a3a96b092`  
		Last Modified: Fri, 04 Jul 2025 03:52:48 GMT  
		Size: 59.9 KB (59935 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:37ebde3fb657fbd793c4272e469157d5a52bca774a229b3cbb692d4ecc52da48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73107892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c26d5da3fcc7172d105db6d191faebeec494fb71ff6ea593a77f412a5edc9c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Jul 2025 17:33:36 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_VERSION=4.1.1
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Jul 2025 17:33:36 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Jul 2025 17:33:36 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e43c61ae1e0c744fe16280bfbb4c2a71a2399a9c17323b5df80c162c89c2cf8`  
		Last Modified: Wed, 02 Jul 2025 08:23:02 GMT  
		Size: 33.4 MB (33369580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6752d59198a7b89d7a81c2ed90466d73ff551433eac23239b3d4198028ce5843`  
		Last Modified: Wed, 02 Jul 2025 08:23:00 GMT  
		Size: 6.7 MB (6747038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cbc2a49e9afa32470742db49bdfb3aa4d4e1cd9ab94f6289caf2f6a60ec19`  
		Last Modified: Wed, 02 Jul 2025 08:22:59 GMT  
		Size: 1.2 MB (1226747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2631be89e76e789fa08a61dd498702809e3e544848279fa70e3ef03fc805f`  
		Last Modified: Wed, 02 Jul 2025 08:23:02 GMT  
		Size: 28.5 MB (28543600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197dcee48d9fd4de094358331b908d3cc649eb2ffb58a4077e647467b01e0c2`  
		Last Modified: Wed, 02 Jul 2025 08:22:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb5c72e05ebf7e72b6e4847f254b13bf95af3e1adba5dfe36c1a4e0c35a733e`  
		Last Modified: Wed, 02 Jul 2025 08:22:59 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f04128dbb6d78c7a6cadb9cdff61fa3966f43a9f381c872e12376972945774`  
		Last Modified: Wed, 02 Jul 2025 08:22:59 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831d91ce69289f539541547a20ce471f78edf35ca2c539c7be721c43ab7aff02`  
		Last Modified: Wed, 02 Jul 2025 08:22:59 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cfb50e929bbc4913250011223e8400eb991aa99b381c39170dc080de30951ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6547362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91321d9f29232f8de094d8c2034e4b83dff5993154b1aba82cffe50cdc4a965a`

```dockerfile
```

-	Layers:
	-	`sha256:c8cfa34935d3590197e682831248af2bde5097ae3e2b1893f0b0fbffc8c239fe`  
		Last Modified: Wed, 02 Jul 2025 09:52:58 GMT  
		Size: 667.1 KB (667104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c51e851781754ac6c21be051dcbfa04bcbf82c0b2c89a4510f5783434b3be3`  
		Last Modified: Wed, 02 Jul 2025 09:52:59 GMT  
		Size: 3.0 MB (2987477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bfa114300d421f619ad02f0126e9069bf6ac87d2fd9af13df3ad2e151df2740`  
		Last Modified: Wed, 02 Jul 2025 09:53:00 GMT  
		Size: 2.8 MB (2832631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e1ef21bf55091b0b4ea5d28cc110797bd7082c5833bfd821ee09c6fdf53578`  
		Last Modified: Wed, 02 Jul 2025 09:53:00 GMT  
		Size: 60.1 KB (60150 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:cc6feced318a164345eb52f0917fcbba3103f91bf1397e67a1b85bcffd76e7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84987079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a58ac771daa3789b7044afb82bd7600c9b3665a23c83c44cf8c3f6a4ca5d75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Jul 2025 17:33:36 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_VERSION=4.1.1
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Jul 2025 17:33:36 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Jul 2025 17:33:36 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443aa9a9a7970f643866e967891d76a24748fb8b2bc6aa19d90dbcf385fe14c6`  
		Last Modified: Wed, 02 Jul 2025 03:21:19 GMT  
		Size: 40.8 MB (40842436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6265ea57c4ee219cb075cd03bfdd8cf00c9acdba51422fc9f73d3e97e742878`  
		Last Modified: Wed, 02 Jul 2025 03:21:16 GMT  
		Size: 9.0 MB (9037846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c33eb1a33bb4633c1ee87e75ad3ba53462d03e0a47b074ad928e01e7de3fdda`  
		Last Modified: Wed, 02 Jul 2025 03:21:15 GMT  
		Size: 2.4 MB (2424749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc39974e8cc52ad8fd956f4b735e80f0b61787fbb0ba0abc32d67033bf4d0a22`  
		Last Modified: Wed, 02 Jul 2025 03:21:18 GMT  
		Size: 28.5 MB (28544360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3015066831cd1246e41d096f87c276581e4781f1890076c52fe6a87bd11a5776`  
		Last Modified: Wed, 02 Jul 2025 03:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ec7ec15af37a496f6c3147319fad1a1c009dde5c4293176e65238dfbc520ed`  
		Last Modified: Wed, 02 Jul 2025 03:21:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaf7a22afa6f3875f447068b7f079bd050c74de955e1843cf2a18550dc6d70d`  
		Last Modified: Wed, 02 Jul 2025 03:21:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7222ebee8ee0d5240bd13cf69c3a49224194ba8b78a48ec7c4a345b473c07647`  
		Last Modified: Wed, 02 Jul 2025 03:21:14 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b48f12e000b530e0b5c719874c000dac31c4463192b1dceeeb0ec86c6d6bb171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6891364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5623a388e3b0cbd99713cf245f9ea016c8d4c118ee3b66f40736b3c83e906bec`

```dockerfile
```

-	Layers:
	-	`sha256:0704be729d548fe9f5381f3dd7b187a0c875058cfb73d78d3864522efcba8d2d`  
		Last Modified: Wed, 02 Jul 2025 06:53:27 GMT  
		Size: 672.1 KB (672104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84deb2736c18e84d7540497db75d2a7178581929851717087dbbc611421bb91a`  
		Last Modified: Wed, 02 Jul 2025 06:53:28 GMT  
		Size: 3.2 MB (3156952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c08a55050175c135cc36e03aa890399600815fe27dfc7f07ac4385d94c93b0`  
		Last Modified: Wed, 02 Jul 2025 06:53:29 GMT  
		Size: 3.0 MB (3002112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f6ef004ca030bfef4eb43afc4087f0777e072e83989d1f2d674db51228e17d`  
		Last Modified: Wed, 02 Jul 2025 06:53:30 GMT  
		Size: 60.2 KB (60196 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:cff8d2720ae22bcd39960c6b5e32d71fb8a705c9d725e1bf5cd1538d38026ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75409468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c393df6af572d95b1eb66f9dea1372316524baf47f61db6913d949adb09ccbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Jul 2025 17:05:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_VERSION=4.1.2
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Jul 2025 17:05:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Jul 2025 17:05:34 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eb66142c4a07c9c5d2145dcf47f6677931f5023bc50081750b1607875251a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:44 GMT  
		Size: 33.5 MB (33525796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662a3f9a72fba47ad135fd9cb39e0cee5a1299f445bc18c841b9c65fa6510539`  
		Last Modified: Thu, 03 Jul 2025 23:16:35 GMT  
		Size: 8.3 MB (8327311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0764779a0718ee4f52681accaeba85992e06b6e582be8abfb9edaf850288c61b`  
		Last Modified: Thu, 03 Jul 2025 23:16:35 GMT  
		Size: 1.3 MB (1332255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c4f5e26d4665cdd1c78325d70909465076e8bc3b8c2c4e90a9405525f30b32`  
		Last Modified: Thu, 03 Jul 2025 23:16:40 GMT  
		Size: 28.6 MB (28606326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e13160304982a1d7a81a1714ebe1a68acababff7afd946780c71d0045941a5f`  
		Last Modified: Thu, 03 Jul 2025 23:16:35 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02e9045ff762c6cb61eaabe939d2d447983f264a0236962a1fcecbbbd7c981`  
		Last Modified: Thu, 03 Jul 2025 23:16:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770c92443e38625bd99265c8486a286a2e33e4279f70e839cd47c51e37bb0902`  
		Last Modified: Thu, 03 Jul 2025 23:16:35 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527cee7769d7b8b67cbbb396e453595903cd8696ea3b69ebf8aad3899cd38848`  
		Last Modified: Thu, 03 Jul 2025 23:16:34 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d02e0820eec3fcf23428255c99418b4aeb8bffa63060c177d2227d634d0a456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6755906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c9602cf103ab55b0116d6f1c9296b70714ad41502a55621e1742acb364de48`

```dockerfile
```

-	Layers:
	-	`sha256:dff70e9cc0adb3a4300ce469281176042f786f6abf4e8cfefe24e71eb2d9e26f`  
		Last Modified: Fri, 04 Jul 2025 00:53:07 GMT  
		Size: 666.3 KB (666311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fd130dc6b4203865c5f75b9af88e646700d68769a66903e57c52a44d7ef75ef`  
		Last Modified: Fri, 04 Jul 2025 00:53:08 GMT  
		Size: 3.1 MB (3091602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd75718131ced5525f642e1831f5981a0b680a9d6cf0e45d3c8454bb77394f6`  
		Last Modified: Fri, 04 Jul 2025 00:53:08 GMT  
		Size: 2.9 MB (2938087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5efb4c9929a247be985575db22a4205f6577c489f8b033adf25aa6695995be0`  
		Last Modified: Fri, 04 Jul 2025 00:53:09 GMT  
		Size: 59.9 KB (59906 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:6c0a7564228375fafcee901d76fc1815c2cb5c107023cfca0fd2cd6595f2d63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76487967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f69264d9ca84f80799807214ca9456b1cb5303f6c08292e56806ca7a4a197b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Jul 2025 17:33:36 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_VERSION=4.1.1
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Jul 2025 17:33:36 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Jul 2025 17:33:36 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0393fca0edb4033a2e954531026d4202757951a702bf1761bc61d92f02437e`  
		Last Modified: Tue, 01 Jul 2025 23:45:00 GMT  
		Size: 33.9 MB (33910859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af386c32bf112ab246aeeb13e1114cce31427b8f97bd28a5460158553bee2b9e`  
		Last Modified: Tue, 01 Jul 2025 23:44:59 GMT  
		Size: 8.8 MB (8849236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd04b6ea80198aed22c0958d50c03fe77068dc745a12e206f8c9225d5a69107`  
		Last Modified: Tue, 01 Jul 2025 23:44:58 GMT  
		Size: 1.5 MB (1452398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a16fc30078a783a18cd4f66bca3ffba9724180b0f4b629212d6609545c427b`  
		Last Modified: Tue, 01 Jul 2025 23:45:02 GMT  
		Size: 28.5 MB (28543537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e2caa78a451e3fe7340514245f6ebc572c40ec4d4001746812873f5eceedc3`  
		Last Modified: Tue, 01 Jul 2025 23:44:59 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a2ead943e72c7551fc603ce15c2524bb47102cf35e6667694958df99dfb2f5`  
		Last Modified: Tue, 01 Jul 2025 23:44:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dc9defa162cde6c293631170ba29f3372f5109539901bcd6920d91fd4b6884`  
		Last Modified: Tue, 01 Jul 2025 23:44:59 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69fd9c407ecdc6918e06ebe5935256ead3082628f7a422d044cf9eec3f8d879`  
		Last Modified: Tue, 01 Jul 2025 23:44:59 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:67fcc67eae3838abff520fd00dedeee2e257005b531153b13258a9e6188a379c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140cb9d88f83ba928d15bc8106d14f7f734132154a76e319865b9f9161b0cb0d`

```dockerfile
```

-	Layers:
	-	`sha256:aa4ab6736b7d9a94ab051f8d7714f194c1583a5572a21d53a7e2b5463fe78bd2`  
		Last Modified: Wed, 02 Jul 2025 00:53:33 GMT  
		Size: 665.2 KB (665151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ead7d12fc6e71d6b2ab08fba421b349c79149cce7ff5386fb2b1b1f5820c29`  
		Last Modified: Wed, 02 Jul 2025 00:53:34 GMT  
		Size: 3.1 MB (3108706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5b445e0a3ba1f5d7303bb52c06efd9a32b8fa8420d4f753f432a4756a74b313`  
		Last Modified: Wed, 02 Jul 2025 00:53:35 GMT  
		Size: 3.0 MB (2953854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f8a431e9c8aaa3b467fc81e249347d09b299a8cd0a4f16b3794dff0bdbfd60`  
		Last Modified: Wed, 02 Jul 2025 00:53:36 GMT  
		Size: 60.0 KB (60019 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:17b8aa2c73ec30689dbd2a63e55ec9a0bbdc6412534a7969232e4d81f5c5090b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78163953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d36181cb762a1c2a1d52df93d730e19ba50f908d8570a35bb44e8ad71fffc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Jul 2025 17:33:36 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_VERSION=4.1.1
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Jul 2025 17:33:36 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Jul 2025 17:33:36 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a90c2238a837d0df3574a4aaf683ddfc7dac73851f4d76bdaca1c033eae8d0`  
		Last Modified: Wed, 02 Jul 2025 00:58:27 GMT  
		Size: 34.9 MB (34874535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb6b6c85481954a81335dc28f76c051c5e4013e72f09fdcc5b1007233b6ce1f`  
		Last Modified: Wed, 02 Jul 2025 00:58:21 GMT  
		Size: 9.9 MB (9863432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e94a0bc3f9fb79de0d464e4f687118266db5c846bf50411e5bf18e17924dd4`  
		Last Modified: Wed, 02 Jul 2025 00:58:21 GMT  
		Size: 1.4 MB (1366298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a170ee2d4efa5dd4f49ffbb4f6c18efcde1a3fbbbf4b3f5e9c98636608ec8215`  
		Last Modified: Wed, 02 Jul 2025 00:58:23 GMT  
		Size: 28.5 MB (28544122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8fa80ffad0dfe4b0c22d90875383cd56ae426184d98ab7f8ced418ee3ae367`  
		Last Modified: Wed, 02 Jul 2025 00:58:20 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7380b7ef99308a05da2c0274757f9a0d0814ec97190bc54c9d40b63f5c1f6fc6`  
		Last Modified: Wed, 02 Jul 2025 00:58:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8964800366a2cd0dd0c6f427fa33e1e54c6931ffd57a8fd485295f9a5260839`  
		Last Modified: Wed, 02 Jul 2025 00:58:20 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd13e30d6468b96a2ffa5dd011be6767f4387388ce15692166e14e69278ba38f`  
		Last Modified: Wed, 02 Jul 2025 00:58:20 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a8034c6949bab475431a74eb1e26f58fc9b4e26546621e40c248821dec664c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6867057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295495e95ad58c7b611de5dfde40e34c7e68018b69d266e49250b109f53e6a05`

```dockerfile
```

-	Layers:
	-	`sha256:0ea32c721dde8f241f16b5cb52da963659adcfe484542163c0abdf0d2947e37d`  
		Last Modified: Wed, 02 Jul 2025 03:53:05 GMT  
		Size: 668.1 KB (668120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb5ade8bb30e78c61c0254b3372dc0b3453a241c3ea67f2bcdf897bafac480b`  
		Last Modified: Wed, 02 Jul 2025 03:53:06 GMT  
		Size: 3.1 MB (3146879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d1f4281a50e86135c048029ab9dc2297119661e618014c1fbbb5e5d99cbcef`  
		Last Modified: Wed, 02 Jul 2025 03:53:07 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f366e7d85bd77643603451769b37eaddbfaf0265281d0f74915d7fc88dc3d25c`  
		Last Modified: Wed, 02 Jul 2025 03:53:07 GMT  
		Size: 60.0 KB (60019 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:77b5aad220d8cd54a16d686026f776bfecf0c640f1ccc434ee6d76756d732ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75082376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab432c3e2d827654812774c99aad436bf587fb127c7c5334ed7c7bf77bd85895`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Jul 2025 17:33:36 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_VERSION=4.1.1
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Jul 2025 17:33:36 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Jul 2025 17:33:36 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717e4a9df273bdeb7d68f276df3e9bff87ed5525abc70822b3733f3bfc7153e`  
		Last Modified: Wed, 02 Jul 2025 01:35:21 GMT  
		Size: 33.9 MB (33945909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfa2835c01912e1b3af5612433b672c2d5c3b7de6f571e3f0eb3689021a1431`  
		Last Modified: Wed, 02 Jul 2025 01:35:19 GMT  
		Size: 7.5 MB (7513209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82608b3d1e70bf6c2341b992ff916b2a8fe1f510d5a8aca27c770dab682efccc`  
		Last Modified: Wed, 02 Jul 2025 01:35:19 GMT  
		Size: 1.4 MB (1430447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a59ef73af479273fbf5268a622202829a080999dce1711f102d517364cba06`  
		Last Modified: Wed, 02 Jul 2025 01:35:20 GMT  
		Size: 28.5 MB (28543532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283d5c2c023f8411a9dc281c10b4ad4d8640b92015baa4285ebba564573460e8`  
		Last Modified: Wed, 02 Jul 2025 01:35:18 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2318352ecc7482c626e5dd087cb76ce0a37be86f0700d5a5c22a773809f0902c`  
		Last Modified: Wed, 02 Jul 2025 01:35:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548a3bb355b80d2f18ab2cb2c8edb73caa9e8d8430700af64bfec877b9f9824`  
		Last Modified: Wed, 02 Jul 2025 01:35:18 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1e461792c3d92cc5e2fd4e277f82bff00142b49bcab7c02b0c3e7c7cd643c6`  
		Last Modified: Wed, 02 Jul 2025 01:35:18 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d1b3b94ae58d05dd1a63b257b46cc81261a1d5049934499cc4ba011a73e96aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6566537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f249510084abcb7c7a40621bc8ef561b6837f767f01d73b843154d1db0d1710a`

```dockerfile
```

-	Layers:
	-	`sha256:2a75994628e6dd0328614ef800c4d5511d3f222b8e681c6a0925c77fee4f3cd4`  
		Last Modified: Wed, 02 Jul 2025 03:53:12 GMT  
		Size: 665.1 KB (665117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e6c6a62f5a46bc87b02ec037835b5c163c7bb3c5cd744356c397b1a28448be2`  
		Last Modified: Wed, 02 Jul 2025 03:53:13 GMT  
		Size: 3.0 MB (2998143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f0a04e26d476d9d5dc25d9dffc3534b7a9097f1a546d8da4d8c0a1fee1f3b65`  
		Last Modified: Wed, 02 Jul 2025 03:53:14 GMT  
		Size: 2.8 MB (2843321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43aaeaa29c04fa33ee04372bfb5e6718ca7f0a4dd775fabcebd1629d1a9a2469`  
		Last Modified: Wed, 02 Jul 2025 03:53:15 GMT  
		Size: 60.0 KB (59956 bytes)  
		MIME: application/vnd.in-toto+json
