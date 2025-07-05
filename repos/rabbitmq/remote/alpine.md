## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:0f82816b33cab89342aefee162a1a748b2ae0ed69db790d7cc7ebec0e516c441
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

### `rabbitmq:alpine` - unknown; unknown

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

### `rabbitmq:alpine` - linux; arm variant v6

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

### `rabbitmq:alpine` - unknown; unknown

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

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:913a63f279b72f6aa7c63b721473099da9ad7bf91e616702be324d32656f6145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73170659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225b6414c625b256a434a4e982ad9240be59733a84a02fab0493519d7b70c071`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
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
	-	`sha256:e783232d0624e0402e7029206e38e0490da619d3a7d5454a579c1cc6ac2a35fa`  
		Last Modified: Fri, 04 Jul 2025 05:13:49 GMT  
		Size: 28.6 MB (28606372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a2dc52913b59e4a04c7bd2db5b01d0dab5c29f3b246a15640a28f0c2a6aa1c`  
		Last Modified: Fri, 04 Jul 2025 05:13:46 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3ee789c3ddd8d31862f4c7a48f2e705da8e130c714d80c5f420f327e18c749`  
		Last Modified: Fri, 04 Jul 2025 05:13:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11b50138945095a05b3bb847dfb53d97785344abb54f21838ff58c340653b5f`  
		Last Modified: Fri, 04 Jul 2025 05:13:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e92a0c783bf118c2a55828cd9d3ae74c1622aade1a8fca0d876611182a08c70`  
		Last Modified: Fri, 04 Jul 2025 05:13:46 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fb6bad062fdd9fc56d7a9ca6bd70d1a82db873a8177885ffc8020a35f16584cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6547365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be452e7b7a9201b7cfc2d1a7fd8a633bce95345adf42da035be61e083131eca`

```dockerfile
```

-	Layers:
	-	`sha256:2bfb08c56c02387565ceee682e8c791584dfec34821114e3fb38f41e7d8a6bb6`  
		Last Modified: Fri, 04 Jul 2025 06:52:56 GMT  
		Size: 667.1 KB (667107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:387e14bf60f680faf80ff3dc47edba34d8a32d479e4c124bc1fc53b2e43139f1`  
		Last Modified: Fri, 04 Jul 2025 06:52:57 GMT  
		Size: 3.0 MB (2987477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:886fd9c25c94b807e4bc4f89f2a0334d0adea81396371b476e2cc6a4e38d3489`  
		Last Modified: Fri, 04 Jul 2025 06:52:57 GMT  
		Size: 2.8 MB (2832631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fd77e23238a2d71683369f759fb13abb73a66570b1736278ef5ea62403ee95f`  
		Last Modified: Fri, 04 Jul 2025 06:52:58 GMT  
		Size: 60.1 KB (60150 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:639b28beb9a4cd5d2037f1dc53458a44230c3f6de6a477d0d4b05c0125c42aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85049307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d089064798e9624f3c3ba97eeaf7abc63c2d0e783be0aae5f17e33ecbbe898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:be886272c2828a2691ade03c266a7cabb5c7d559ab0e0184bf111eb2e5e0b042`  
		Last Modified: Fri, 04 Jul 2025 08:03:27 GMT  
		Size: 28.6 MB (28606591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e25bf386f117a15084084e3e7a8c3bf6996c26a0f7785a71d095c1470f6d9e`  
		Last Modified: Fri, 04 Jul 2025 08:03:24 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f028c5c3463243c6822415a6bb6b301e9dd239edac9c8625d604a4b13f5481`  
		Last Modified: Fri, 04 Jul 2025 08:03:24 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd56e97d5ca772da1be7fa62b0f12679f4867cfb663806d53e0c8a9f9bf9d0d9`  
		Last Modified: Fri, 04 Jul 2025 08:03:24 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c651bafe47e3c45653b099f42bf717e69c853c6eb01363ae66926fc9d9afa6d`  
		Last Modified: Fri, 04 Jul 2025 08:03:24 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e01048dd9c7b98e687c8d6293eab132aecaf4a43b0f130c253acfd6a00f18480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6891367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968f3b9f81718b9960d5febd77ce52e03337fa4c11e9b9439c982af2e3aa6ec4`

```dockerfile
```

-	Layers:
	-	`sha256:838f678e03ccfd4e514581716ada7b452230d800ddb043b7b30504b4531a3732`  
		Last Modified: Fri, 04 Jul 2025 09:53:00 GMT  
		Size: 672.1 KB (672107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d938166d197b0c2e16a0e61a840ac04768cacb3ec682fbb893867c198f77e3`  
		Last Modified: Fri, 04 Jul 2025 09:53:00 GMT  
		Size: 3.2 MB (3156952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cf187305aab28a57899bf839ca5f62fdf4ab62dbb89d100238b34ce07233aa3`  
		Last Modified: Fri, 04 Jul 2025 09:53:01 GMT  
		Size: 3.0 MB (3002112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:505daba093e9e2641670c01762a5aab25e19155af7552426c4f3a0a99f30bff3`  
		Last Modified: Fri, 04 Jul 2025 09:53:02 GMT  
		Size: 60.2 KB (60196 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

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

### `rabbitmq:alpine` - unknown; unknown

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

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:e335d2662d21b31e1fa808ef4749196701c37efd3d6d1eddb392baa426acd7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76550774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942758a32fa5be683d61cb9d62e30800f867fbeb1af49c8d5261d3e1c6bb8055`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
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
	-	`sha256:15c4365419ef89e69870376dcb3207e8a1f796ca5e29d4e2db4dc06381091999`  
		Last Modified: Fri, 04 Jul 2025 06:45:03 GMT  
		Size: 28.6 MB (28606347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abd32580ac0d4fed5fc59d7cd06d2c3cac82edd902ababd705695925e931bfe`  
		Last Modified: Fri, 04 Jul 2025 06:45:01 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e3aee99ccb9f55e848731df5c46c59740909029a1c1aefb44d0e44224f9247`  
		Last Modified: Fri, 04 Jul 2025 06:45:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f3fef35a72a4458450cfb39925f759db1abf66efedf74129f2e6d1c3ecec01`  
		Last Modified: Fri, 04 Jul 2025 06:45:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10409a79f76591a953dd59f1bb29de23e0bbd1b8a871c1346b4fc50b626363f3`  
		Last Modified: Fri, 04 Jul 2025 06:45:02 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1ab148c3fcdaf0e6e348994ffb70e460da6b7e0fd74f59c204e0861abfebe06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0828d861676c1beb52e7d9da66c88c629b5c3dedea2ad205fc692e8fe496c8`

```dockerfile
```

-	Layers:
	-	`sha256:ce15373e548982391f04523c58e32f209d4282d724cf242b949262e21d856f5b`  
		Last Modified: Fri, 04 Jul 2025 09:53:10 GMT  
		Size: 665.2 KB (665154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0ae8e073975ba77823eac288a271a42f27e785f06e945b000e5f0ac7f6ad7c`  
		Last Modified: Fri, 04 Jul 2025 09:53:11 GMT  
		Size: 3.1 MB (3108706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a76579c6be21be238a0a7026684ea4ffc72bd156d2dc5eefd19e3d92a519fb`  
		Last Modified: Fri, 04 Jul 2025 09:53:12 GMT  
		Size: 3.0 MB (2953854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33fdd832cc788d218272ab741841db70f1e88e1b8e6b2533cb70af96abb15c2f`  
		Last Modified: Fri, 04 Jul 2025 09:53:13 GMT  
		Size: 60.0 KB (60019 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:0706e51bae8a06cf4b7883e14b75f07d907d972e7400185e11cf5fddc54ddd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78226278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93528bebd469418f2c6194304d287fc8dfdf0939362d9c8e4addc2f6a977683a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
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
	-	`sha256:ecfc01aefccd89e31054a5d2ad2b83fd31ca2d10a5801283f6d7862da121b4d4`  
		Last Modified: Sat, 05 Jul 2025 05:19:57 GMT  
		Size: 28.6 MB (28606451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e6367c1ecf955bd40ccbcebb6d488a06576ea8d4602fb70d76421403825ec8`  
		Last Modified: Sat, 05 Jul 2025 05:19:53 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfdaba868cedc31b2b261f28ce476e41332afc6f84c2c120248b7569375b8aa`  
		Last Modified: Sat, 05 Jul 2025 05:19:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f3fcfce85eafe8bea4e5fcdac061e0447bd02ef4f6e77095e3f9c7e0ef5540`  
		Last Modified: Sat, 05 Jul 2025 05:19:53 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abcf1cf05cdb27d791c9f808cf639a74392251f560b56dfa5f673e834adca74`  
		Last Modified: Sat, 05 Jul 2025 05:19:53 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:96a86eb533cd7ffa954a3643ccabd88adc3aedbc45aebf4ccbe19abf43ec4dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6867059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64db2b2bcd6e2468f76fcfde6922664ff7258a960162e05e6f0289157279e277`

```dockerfile
```

-	Layers:
	-	`sha256:4c79bc40925d59018a16e01697c0852a76dd9b91a29ddd69a0117509f61a5bfa`  
		Last Modified: Sat, 05 Jul 2025 06:53:03 GMT  
		Size: 668.1 KB (668123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72509f526c3309a1091c70dbcbf1d2fda0131e31e37db4e5b186abb0388791b0`  
		Last Modified: Sat, 05 Jul 2025 06:53:04 GMT  
		Size: 3.1 MB (3146879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6901f38dc733dcdc7d3afbe39582b3fbfa778f70d79c8bf028505dc85455ac9e`  
		Last Modified: Sat, 05 Jul 2025 06:53:05 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a49ec6f211160040e5fb0670cbf9337ce99927cdb9f76f7463c86455f0345e08`  
		Last Modified: Sat, 05 Jul 2025 06:53:06 GMT  
		Size: 60.0 KB (60018 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:abaf3df84625d2aef0c4c851c0da442523ff05b0b321f93128918617d0fbd044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75145244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81023509ee21dc3f22be3bf02a394416488aae59c02fb6f02006747e47fd10c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
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
	-	`sha256:91db571264cedf48d9631c9b576c698b4123fba68975d13cfd124174aed894b8`  
		Last Modified: Fri, 04 Jul 2025 04:39:17 GMT  
		Size: 28.6 MB (28606401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ab55b5dfc655b77592f48d3f4ad066acf631ec35cd80106912177b65a2d14b`  
		Last Modified: Fri, 04 Jul 2025 04:39:15 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294dcc79dfc5a13ebf7c74e5582c2aac688bc2afc5e0514c0893f7b386690330`  
		Last Modified: Fri, 04 Jul 2025 04:39:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fe642c8ac2fb3ce63e28f39b24012fddcb79fd6d4fcbde6f0e3d2ad1b9a32f`  
		Last Modified: Fri, 04 Jul 2025 04:39:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b640c7431319dbdc0f5b514c74665db3f1b008dd7258b92ba93dba80257765e`  
		Last Modified: Fri, 04 Jul 2025 04:39:15 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0e3824e43dd6d8ca98f853a0960d8e075557c2ad3bd6793a0fd391355d615a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6566541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43eb7d95f5bd723b4ca1e886cad00e402733d25dac19f622ee8add2ba8c5b2e`

```dockerfile
```

-	Layers:
	-	`sha256:95f5b706eb8972527737447ec1310c79017ae12dab8dde730c8665865019ac1e`  
		Last Modified: Fri, 04 Jul 2025 06:53:19 GMT  
		Size: 665.1 KB (665120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cf3e0b05538679e08b305f3f327f36d6722787f7f3cbc99e36ce57460ca5c6`  
		Last Modified: Fri, 04 Jul 2025 06:53:19 GMT  
		Size: 3.0 MB (2998143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:140e6058ab8d29dc2f2b854d4359b5cea184bd7f2168c2d920cc841ba20662a9`  
		Last Modified: Fri, 04 Jul 2025 06:53:19 GMT  
		Size: 2.8 MB (2843321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b4ca1dc380986cc64285d831ff5eb2709bfb0e7f1e9b074836b550080d87ae`  
		Last Modified: Fri, 04 Jul 2025 06:53:18 GMT  
		Size: 60.0 KB (59957 bytes)  
		MIME: application/vnd.in-toto+json
