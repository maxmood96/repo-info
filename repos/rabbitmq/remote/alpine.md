## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:490af7c4acae73602c64ffeb288e32628421d25a8d36f74072057402cfe82518
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

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:a60dbc6e25be2f4c3dcecc53f4c0b1e344003b2ba39e99254cdf4d8d3e11c025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73735240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4083c19b838ffe05a78a06339983593cc139d6fd4d27c9eb855875a1efede9dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Aug 2024 14:59:48 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_VERSION=3.13.6
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 15 Aug 2024 14:59:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 15 Aug 2024 14:59:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2dba0fad19da65a6995710208cf09460d514ac3f1455b7ba99e2e0d3603e3a`  
		Last Modified: Fri, 16 Aug 2024 22:04:16 GMT  
		Size: 41.6 MB (41565062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c182b78ccfb39b313891c70bea49a4df63f5579ccafe8781ed70d6d49a74146`  
		Last Modified: Fri, 16 Aug 2024 22:04:16 GMT  
		Size: 7.6 MB (7578121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d776c6598c5615eb39941a18a6badbee0c66d9360e0f9e3a6cd969772819916`  
		Last Modified: Fri, 16 Aug 2024 22:04:16 GMT  
		Size: 2.2 MB (2241427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727cda4dbbc42f91382a8e390ad807523e78503de7168c04c68b9e2e93d2a553`  
		Last Modified: Fri, 16 Aug 2024 22:04:17 GMT  
		Size: 18.7 MB (18725990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937e8bc5e54fc9d46500945cd54f89819f7f7358ac8a232326be030b4d1e18a8`  
		Last Modified: Fri, 16 Aug 2024 22:04:17 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e95df9947a3f49ae307d8b9d7c18f8168cd8c055d9e36211e6dcc3c6184a78`  
		Last Modified: Fri, 16 Aug 2024 22:04:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ffb7cde121b6c4faa796cfd99a3d131bf1408a50774a09d88c66ae1d31b884`  
		Last Modified: Fri, 16 Aug 2024 22:04:17 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae151ec638449ea4a7894151dd594f9358793465c31637bf541ec3b5f3d2f7ff`  
		Last Modified: Fri, 16 Aug 2024 22:04:18 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f5d90fc095f383c914a550200d14fd88f36d75739d36c953d4f32f3f33852518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6427469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a510d9719bc6837818c8ad016377b1b336eb6e18a67827113b1aa790ae7280b`

```dockerfile
```

-	Layers:
	-	`sha256:0be5a2567bcbde23a0566a12f40e2bbae73a07b46dd7527051076f2adcabfc4b`  
		Last Modified: Fri, 16 Aug 2024 22:04:16 GMT  
		Size: 640.2 KB (640162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b6b66d939a5a471f704fc57fe887dac0bfe8850b3754362fa79fee8c213db71`  
		Last Modified: Fri, 16 Aug 2024 22:04:16 GMT  
		Size: 2.9 MB (2931565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df06fb7afdd21fe2fb0434b1d15e32583d338a49d17a48aa62b5f8bb872b3a6a`  
		Last Modified: Fri, 16 Aug 2024 22:04:16 GMT  
		Size: 2.8 MB (2794092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b06dd3f593291b3d05c4eface3499181136b8943b9ceddbd1e69b3a3fed7163a`  
		Last Modified: Fri, 16 Aug 2024 22:04:16 GMT  
		Size: 61.6 KB (61650 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:ae806192b199c702be98242670abdcc4a326b064d25dc31557ccad08dacc28b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62914882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c91aec22339145fbed8f8bf850e42bba02dd1640e2c1438ae1def45133e154b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Aug 2024 14:59:48 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_VERSION=3.13.6
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 15 Aug 2024 14:59:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 15 Aug 2024 14:59:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a399bd99a39f9ffaa2b2dd7afa04c47f84cc6b608140446be981097b934d8f6`  
		Last Modified: Fri, 16 Aug 2024 23:27:57 GMT  
		Size: 33.2 MB (33179643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a8360038b0019ddc952778909181044a00becf16fbcf904c051750ece94cb2`  
		Last Modified: Fri, 16 Aug 2024 23:27:56 GMT  
		Size: 6.4 MB (6405900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a2e4a057854428f8a63e907dfe8f6cb669869651c05310cc1dea0b46e40ba1`  
		Last Modified: Fri, 16 Aug 2024 23:27:56 GMT  
		Size: 1.2 MB (1236482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b344f719ea111c41fec97e01e8330f890a5d5fb7d47e0cc4b74cbd75bdb4298`  
		Last Modified: Fri, 16 Aug 2024 23:27:56 GMT  
		Size: 18.7 MB (18725918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6cdee283766e323d6397ad512b6fe266d520a15fc1841b7aee3fe08e7fbe31`  
		Last Modified: Fri, 16 Aug 2024 23:27:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389f7e49d5b88bae08dc8bb19d48e809e233ce42f2d64378c6d0f4eedc33ce3`  
		Last Modified: Fri, 16 Aug 2024 23:27:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1036cce20e189aef62adfc333819465bbd3e566d308460104df32f73e91664d9`  
		Last Modified: Fri, 16 Aug 2024 23:27:58 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062904dde797c7f0e575fb02f9a4322a610ddca0e7cdc8e20b1e8499a1d11286`  
		Last Modified: Fri, 16 Aug 2024 23:27:58 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2ef95cda9dfadc15a6b7f8721e69eb85584a5c1ce4287c9113344f3bf4ce1a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 KB (61618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c9cbb7a52ffe7fee741eb3d889ffdf4b2c1d191dfc941639fc623a1f410c59`

```dockerfile
```

-	Layers:
	-	`sha256:006c1675902f9c63c4e07728d87d3fe1409bc5e8b2b639e130ac8ed77be854e8`  
		Last Modified: Fri, 16 Aug 2024 23:27:55 GMT  
		Size: 61.6 KB (61618 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:a13fd6b8bd4af00a9bdec9b990c544ce3622a1a895a4dac34b45cb2a138ead10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62156575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7a14c3d95d47f736020c8f930dce713801d9294deb6e8d0414265448c2c0c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Aug 2024 14:59:48 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_VERSION=3.13.6
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 15 Aug 2024 14:59:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 15 Aug 2024 14:59:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a982534696144ceb7d200537d306396b09f6637e6757b2a9de2f1dab8708d3ec`  
		Last Modified: Sat, 17 Aug 2024 00:54:29 GMT  
		Size: 33.1 MB (33087010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c5f6bf838b2f2d43d5fad5daa6fdd20957bb236949a0921ac9a5a37be47bf`  
		Last Modified: Sat, 17 Aug 2024 00:54:28 GMT  
		Size: 6.1 MB (6106894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab49839e095324037fecaf8073095462d04abcf8ef94a3d9dd6b642053b1fa6f`  
		Last Modified: Sat, 17 Aug 2024 00:54:28 GMT  
		Size: 1.1 MB (1140442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc717912ab298b81cce8a4334a5026411e72831a15793a68e0570a41a3b6b1f`  
		Last Modified: Sat, 17 Aug 2024 00:54:29 GMT  
		Size: 18.7 MB (18725523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085a76e5a8fc771dd376ff0b9c772f0e835ef82a1ed32a7ab7cb6005628baf25`  
		Last Modified: Sat, 17 Aug 2024 00:54:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0aa7e66a2aad5a805a99fbde33b85cb892c2c89362f0c5cd2e90cada18fd`  
		Last Modified: Sat, 17 Aug 2024 00:54:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a353ced83bb8cef2c08b8ff96e6f7602f30968508c6999ac167feff3c0b885`  
		Last Modified: Sat, 17 Aug 2024 00:54:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5f32b5ef9e6a4ef3ccfed3b6cbfa13748acb70602870610828bb16b28568c4`  
		Last Modified: Sat, 17 Aug 2024 00:54:30 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:15d1942e06bba66191d0d6de1bf5e9680d6898e81f206cfcd4b6555cd1f0e9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6221158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5596fd6e1a7527827f3f83890a141e402d77c797c8c642011d9336f8de32ce`

```dockerfile
```

-	Layers:
	-	`sha256:fc93e72996dafab63c1c9c4e16996149c9b67936819669b777dae82f3cc5ddf1`  
		Last Modified: Sat, 17 Aug 2024 00:54:28 GMT  
		Size: 636.1 KB (636127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9e1021eac564121aa5c3733c77a03cfb0c0335dc7b9aba7dfd15fd46db82b9`  
		Last Modified: Sat, 17 Aug 2024 00:54:28 GMT  
		Size: 2.8 MB (2830893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8f2f102f0a53c608bcb759d33d54782feab253123f24494caba5603f70c180`  
		Last Modified: Sat, 17 Aug 2024 00:54:28 GMT  
		Size: 2.7 MB (2692301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:512304499be9b3813a80f2b9a58696c5d74adcac65bef672d8a8c594ca23119b`  
		Last Modified: Sat, 17 Aug 2024 00:54:28 GMT  
		Size: 61.8 KB (61837 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:1d1091397b5ec9f433658e18abb9de0456ae89007c23e6de3fc55a4d170ea6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72028237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d2e8f39b9ddb016770aef7a1e08cc343f2dfcc88c8425591b73e9aaa9ebe8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Aug 2024 14:59:48 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_VERSION=3.13.6
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 15 Aug 2024 14:59:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 15 Aug 2024 14:59:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ebcf3fc865f7b70630f40a496af3e4f5e8899252513db86d9ed6898a6502f3`  
		Last Modified: Sat, 17 Aug 2024 00:40:49 GMT  
		Size: 39.7 MB (39685252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943739027bc55d6480260d07dffa2e33c88464e97042fdbb05125bc2b44e7727`  
		Last Modified: Sat, 17 Aug 2024 00:40:49 GMT  
		Size: 7.2 MB (7200490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e68d00f43ae338a7a382fd8f3e6e9f5e5f500bef4b4cf55695f4ef0fc4a61b`  
		Last Modified: Sat, 17 Aug 2024 00:40:48 GMT  
		Size: 2.3 MB (2327824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25ef6cee078e07962dbd4363d34e8cf18e25ef858612118b3230af858bbc91b`  
		Last Modified: Sat, 17 Aug 2024 00:40:49 GMT  
		Size: 18.7 MB (18725993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c9a9cf83bfd2171ade90ca3f5a21c60460e8b81ec653d6ca95f95a3f665f69`  
		Last Modified: Sat, 17 Aug 2024 00:40:49 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7466a9dcee861c36ad86890ca445eb55b58ba127d18ae9a440953c549bcdf1d8`  
		Last Modified: Sat, 17 Aug 2024 00:40:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989c33ddaa67fb0fc2e4e58ae94ca7942c8164292ea4ecc35df989fda3638ffe`  
		Last Modified: Sat, 17 Aug 2024 00:40:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd60467e40190fabfeb9dba6fa45adbdcb9d49964ba7faca25df7008220dd254`  
		Last Modified: Sat, 17 Aug 2024 00:40:50 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c4a3a01ebacaec4b12f637b6daff3e7ef1b85a473ff27666d920d11365efa787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3698d151eade5283876ea77e87b4940ebf89da168cae8a176086da10937cd3b`

```dockerfile
```

-	Layers:
	-	`sha256:acd7463282933e7d6c4298a831ca8925cb5886485872df7b0c826fc5d88478e0`  
		Last Modified: Sat, 17 Aug 2024 00:40:48 GMT  
		Size: 640.9 KB (640850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4797ae3d293876ed68ab996e6fa3d6309152ece9abc5c30b63cf55f4c6925eca`  
		Last Modified: Sat, 17 Aug 2024 00:40:48 GMT  
		Size: 2.9 MB (2948820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05732a3de25166a6f57ab88fffa6fd85e3d9cdc915b54a7fdd4b8636769e8242`  
		Last Modified: Sat, 17 Aug 2024 00:40:48 GMT  
		Size: 2.8 MB (2810234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f488983b833f4985ab0b0dafe40d4d4398eec94e144a9f823cf539fbcad1ace3`  
		Last Modified: Sat, 17 Aug 2024 00:40:48 GMT  
		Size: 62.0 KB (61950 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:cbad64b19680e994c26cc1ffd8b6d82081899eccedbbf3898e03f42e23f71d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64295088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12578d455a2e8d967ec259884726e77ec4271e5cd49df6949ab207a40792bde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Aug 2024 14:59:48 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_VERSION=3.13.6
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 15 Aug 2024 14:59:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 15 Aug 2024 14:59:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064cfccc8cf8da99fb926859cc4d73277b51df4b4fce96ba5d42c5da85f6f40d`  
		Last Modified: Fri, 16 Aug 2024 22:04:01 GMT  
		Size: 33.4 MB (33355334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d7eaf24ff357241a016ab529ca936df5f18ff2010fcba46a57d66ecdd9581b`  
		Last Modified: Fri, 16 Aug 2024 22:04:01 GMT  
		Size: 7.5 MB (7505534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9422a3b008e8b4fa57d033aa208aba4bcd852922e0bcbcb30af1321925d8ccfa`  
		Last Modified: Fri, 16 Aug 2024 22:04:00 GMT  
		Size: 1.2 MB (1238814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5c9201d2df75cefdb6054b7b507d90542e541adbe0e43ec2c88107fa15573a`  
		Last Modified: Fri, 16 Aug 2024 22:04:01 GMT  
		Size: 18.7 MB (18725584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b9f2565d5d14fc79f56f4bf3d750225c82631050837ced8d478a7efe43c5b5`  
		Last Modified: Fri, 16 Aug 2024 22:04:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab59bda6852188fcfa2f52e985c76017aae6784ac391bbdebf1cc0a67b295e49`  
		Last Modified: Fri, 16 Aug 2024 22:04:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8bd08ac332f08d880d7666538c59e267bdf9a5bc10445aff1d580fcfdc4da5`  
		Last Modified: Fri, 16 Aug 2024 22:04:02 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b247598a5a560d240f5353ee9a30e83d775efdca41dcf81848c3dde83cfbb42`  
		Last Modified: Fri, 16 Aug 2024 22:04:02 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1720debc2f8b7802ff7c9b559db6c39cdaac621f5bf64abee2b49017d4cc9bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6403134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db80dafbbd35cc59da458b78a919674d6bddeacdd81b6502e678203ccd12217`

```dockerfile
```

-	Layers:
	-	`sha256:08ab181e6b2155305749a3b544e22a5329e86fc4092907cfde5607dd158919d0`  
		Last Modified: Fri, 16 Aug 2024 22:04:00 GMT  
		Size: 635.4 KB (635434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c89257956735d7df70012a03ee4304c8164560425f7caee50f26604096f4f37`  
		Last Modified: Fri, 16 Aug 2024 22:04:01 GMT  
		Size: 2.9 MB (2921783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca38f618d721bf7db4a91eadaaafe01aa6f004e4ff69d0763be637d57cf6cff`  
		Last Modified: Fri, 16 Aug 2024 22:04:01 GMT  
		Size: 2.8 MB (2784314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a6ef7d43828c03a34d4556ab938fbf9a43ef6e1dcead967470e096eff4c6284`  
		Last Modified: Fri, 16 Aug 2024 22:04:00 GMT  
		Size: 61.6 KB (61603 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:77d8b96a0ea134ca1b7236c3dae988b4e27433245c0f6c6096c7c69a5e404c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65255301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71de22709114a0247e8a0e4db6792a7ed6ebce7598e582b7d58153add49340d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Aug 2024 14:59:48 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_VERSION=3.13.6
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 15 Aug 2024 14:59:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 15 Aug 2024 14:59:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac555ce06cdd1b1803ad1cccc536261847bc31284daf67faf261da2b56ca355c`  
		Last Modified: Fri, 16 Aug 2024 23:45:21 GMT  
		Size: 33.6 MB (33611323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146bf248658271bde35bd185d35b925e146475d0f47bf2c2ff39e655a69e6358`  
		Last Modified: Fri, 16 Aug 2024 23:45:21 GMT  
		Size: 8.0 MB (7992691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e0cf12e6994981d1f02a7d184b25b4d3de3cd9d4377d5de69830be34dba021`  
		Last Modified: Fri, 16 Aug 2024 23:45:20 GMT  
		Size: 1.4 MB (1352388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52763aa464c0d7705c919ab9a81526a7c8fb32b22df9e5d3ab270b78e7d50293`  
		Last Modified: Fri, 16 Aug 2024 23:45:21 GMT  
		Size: 18.7 MB (18725591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d439c883d6a0636718787fc5fb6fa482cf4484a631b724673f0cee1e1f0f4be`  
		Last Modified: Fri, 16 Aug 2024 23:45:21 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b19e2e486d21f879f8aa5d281d61d60fca5538f38426580540cb8a855bf762`  
		Last Modified: Fri, 16 Aug 2024 23:45:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e63ae25c1d2f6dad79a22e7855efa9d99643ad9222168a115624d6359ee3b`  
		Last Modified: Fri, 16 Aug 2024 23:45:22 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9e4bb078850fe622759d748e644141089d952bca03ab4470744801923d7d9f`  
		Last Modified: Fri, 16 Aug 2024 23:45:22 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:57bd3eaa211099f0273aad242729df1634f4935b521c24bf440eed4b6546d81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6399875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd80703f70b529209aa335160f7214a0615e9da8b2d9cf45ac07e5a493c0325`

```dockerfile
```

-	Layers:
	-	`sha256:aff82971bc8968ba8e78b36d970ad805f7a632b766a19beb430516c506404424`  
		Last Modified: Fri, 16 Aug 2024 23:45:20 GMT  
		Size: 634.2 KB (634171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772de70b94681da3db098d9faf5b9664350b8a44f85a69f06959b6c0bab0d6a9`  
		Last Modified: Fri, 16 Aug 2024 23:45:20 GMT  
		Size: 2.9 MB (2921298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d7b42ee4da65a4f1e65238d9b9537b0e248de9d5d31feeb999913eb87bc78f`  
		Last Modified: Fri, 16 Aug 2024 23:45:20 GMT  
		Size: 2.8 MB (2782700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0e69271d91cd38d221bc5d43b0acc8a8ada795f8f4c3184859fc0e5ea9b4403`  
		Last Modified: Fri, 16 Aug 2024 23:45:20 GMT  
		Size: 61.7 KB (61706 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:3274ada2b89236cb12ce45d04db4a17d3c3e054b983d328dc182d3abc0e38c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63932132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8571df589d20685ab546e72c5c946fbc35d1dd79c6b98529ac2dce94959fc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Aug 2024 14:59:48 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_VERSION=3.13.6
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Aug 2024 14:59:48 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 14:59:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 15 Aug 2024 14:59:48 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 15 Aug 2024 14:59:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 15 Aug 2024 14:59:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 14:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 14:59:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 15 Aug 2024 14:59:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a527cc511f2d572f132f6232b3cf44cf6ae418c3ef0042941289893d4dd1f9bb`  
		Last Modified: Fri, 16 Aug 2024 22:18:17 GMT  
		Size: 33.7 MB (33690256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1c2ce462bd75938edb634ca1387ea76e515ee50623fbde60dc184654112e8`  
		Last Modified: Fri, 16 Aug 2024 22:18:16 GMT  
		Size: 6.7 MB (6721508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9891f93d3c72bee99ddce304390764506bc773f244a54073fbc314929c36836`  
		Last Modified: Fri, 16 Aug 2024 22:18:16 GMT  
		Size: 1.3 MB (1331940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b5c6f1a0bb4d6bac1f03ffb415606f236e2a2f688fd0e00a81325b3481958f`  
		Last Modified: Fri, 16 Aug 2024 22:18:16 GMT  
		Size: 18.7 MB (18725609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2ae313038f0e80a17e12c97bc1c62de2aa92b4f193fedfdb32c919b6bd06b`  
		Last Modified: Fri, 16 Aug 2024 22:18:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db701614badaae12118c2a67d32a5a08c291fb8f908fc9ded8b7ddc041b47b48`  
		Last Modified: Fri, 16 Aug 2024 22:18:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a6bfdbcfb49a4385b54d997f84ac3e08aa36f1a2c691ba766070380b9f98fd`  
		Last Modified: Fri, 16 Aug 2024 22:18:17 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc76b3cf94bbdbdd3cc73bb85136c1ff8d88e0bbc7d127431e00dc64a2e92738`  
		Last Modified: Fri, 16 Aug 2024 22:18:18 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3652d76195ce0328b7ee17e1d6679a98a5a36a45283b39b3c8f4e34843c213d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6233921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446ceaed4b8f92f93bb7922819cb39c95690d03b002e20882c65b2a551cfc461`

```dockerfile
```

-	Layers:
	-	`sha256:fc51ea8618e31375c1132717c63095b688a48d26e3b038613536d9cfc930384e`  
		Last Modified: Fri, 16 Aug 2024 22:18:16 GMT  
		Size: 634.1 KB (634137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e7923c0351c67249d327aede8e560944e5c8b78dcc9d2c340f8c0102b811bc`  
		Last Modified: Fri, 16 Aug 2024 22:18:16 GMT  
		Size: 2.8 MB (2838351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:784838657025a318e80d73f758cf64bc5127a28ad555273b72effa8cae33a528`  
		Last Modified: Fri, 16 Aug 2024 22:18:16 GMT  
		Size: 2.7 MB (2699783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e88d790be67e94d9839fa3f8ebbdb07be93adfaff5a96d7eaa20cab307e6ae7c`  
		Last Modified: Fri, 16 Aug 2024 22:18:16 GMT  
		Size: 61.6 KB (61650 bytes)  
		MIME: application/vnd.in-toto+json
