## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:62b2cd5d2e0159597dd50fb792db80faf689a9ecf7fa409ea194e56063be0387
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
$ docker pull rabbitmq@sha256:2aa877c3af99e0e7549e37fef8c00bbbe765d4f64a189511e6cb52c5c4e19051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77579303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7de8e381883f16573d15edd25121489e9637c04e86a253844e8a9e33c51849f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 07 Jan 2025 02:28:15 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e060a22d1c843dc9359408adf2aa91ac4420cb27d00adb80516c6557115783fb`  
		Last Modified: Wed, 08 Jan 2025 18:24:05 GMT  
		Size: 45.0 MB (44989842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c83bd7141ed8ae9e5f919d3482716cfa227e48ffe24e42d791a21a16ebfc73d`  
		Last Modified: Wed, 08 Jan 2025 18:24:04 GMT  
		Size: 8.3 MB (8309069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6350ddeb70e1339de0601c11645b9e4306fe5c117482be3eb0d5de5ae819c0b7`  
		Last Modified: Wed, 08 Jan 2025 18:24:03 GMT  
		Size: 2.3 MB (2277954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd69e2874684ed4f806c217ca890991f5a8284065c1007d62b60b7bb830e31`  
		Last Modified: Wed, 08 Jan 2025 18:24:04 GMT  
		Size: 18.4 MB (18358972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fe08f7c61c0b259f8952d617edce249d7b0307ee89c226fdd6aed3679bf87`  
		Last Modified: Wed, 08 Jan 2025 18:24:04 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3883ffae718a06e51554ae30cc83e0cfa1052f682b8cca129ffe61e0e28794a`  
		Last Modified: Wed, 08 Jan 2025 18:24:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb40ef1e1c9d26c06fec6c9581a88bffd5ec2805bf6f19504d093d61d637ae`  
		Last Modified: Wed, 08 Jan 2025 18:24:05 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a22572c4658033032ed4b68ada1614c7c6db8f5d96db2ab1017e6afb091d8a7`  
		Last Modified: Wed, 08 Jan 2025 18:24:05 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7393cfbaffb66a3c2bad01bbb17691fad2a5173c047303261e17052fcfd69b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6728289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bee6b1b4cd5eed38c74f320e65fa1db1170f5d84a5c97b0250e949b19438cd`

```dockerfile
```

-	Layers:
	-	`sha256:f6b4a6d51eac6f3f9a24e1c51ae8018ae32179d6e9c1c7b0510acd2d359e2ade`  
		Last Modified: Wed, 08 Jan 2025 18:24:03 GMT  
		Size: 657.8 KB (657762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99fe6df6962225b5caebcef6cfb3dd11e60157dc7398816212be7e774e01c78f`  
		Last Modified: Wed, 08 Jan 2025 18:24:04 GMT  
		Size: 3.1 MB (3081579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9bec6c968473821b5f23506abd60bb2d3808a0a9283a3ecc58ff51fff218eb`  
		Last Modified: Wed, 08 Jan 2025 18:24:04 GMT  
		Size: 2.9 MB (2928075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55affa980d3ae04f5bfb639f591252535a0bdc402148c629efab99518f015365`  
		Last Modified: Wed, 08 Jan 2025 18:24:03 GMT  
		Size: 60.9 KB (60873 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:747a0be88449c165c748872287b8bfa10b0b458d44bfc3d061661272ae17978d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65637912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054158241b15b9f4a3c4676dd0f47008acb300ac88cf54b9466046b659e93dcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12da3bc0dc164fc2dc721268ac149ce9cddc3284a62e1d569ea117dceae224a`  
		Last Modified: Wed, 29 Jan 2025 00:29:55 GMT  
		Size: 35.6 MB (35595987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fa176b1a735adfd55984d81cbabb837e4cbecfaa887dd27917a7d89a9b9d5b`  
		Last Modified: Wed, 29 Jan 2025 00:29:55 GMT  
		Size: 7.1 MB (7092057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfed2ab5564ded1e752bf96138db235940094f6c1fd2937cf139056f0d4f73ef`  
		Last Modified: Wed, 29 Jan 2025 00:29:54 GMT  
		Size: 1.2 MB (1225407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f414435790272d4feb9d2e748efd181888a2398f9b460b34dee00f17d5e6f6d9`  
		Last Modified: Wed, 29 Jan 2025 00:36:27 GMT  
		Size: 18.4 MB (18358834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d691fe82359a5ed59fb1d007ff50974610d52faa9bb90e2933e2cda7f0cba3`  
		Last Modified: Wed, 29 Jan 2025 00:36:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62eaaa04a45f1c08895d47c45e18c5bb5e5adf435bb522e4d57483472bc5883`  
		Last Modified: Wed, 29 Jan 2025 00:36:26 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d326cd277fa94c610ee1a690ca454be508397c2f934df9fe04ee1311371d8ac5`  
		Last Modified: Wed, 29 Jan 2025 00:36:26 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399f432423cfc4ab49dd0ab3fc411bc32f6231c43221214070ff34a63e52ab21`  
		Last Modified: Wed, 29 Jan 2025 00:36:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1f49f1da50b340a8671222ff172b3a7c045d5c3b2b746e115dbfaedfd0450be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ab4ab70343b0b59c68092ade568afd10eb5750d4701525b87615e8a3f9cb7a`

```dockerfile
```

-	Layers:
	-	`sha256:12133002eefefe691da187d09a6ad030cbfd3ca33b88ebe988c017eea5a5f977`  
		Last Modified: Wed, 29 Jan 2025 00:36:26 GMT  
		Size: 59.8 KB (59836 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:c870c546ebc26b3f36482dc3a957b29406140a177766686fc2cd81c42929d1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64845401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643c23bba17765c05ce61a6366533d03acf50f4213176d6dfb4b97d3c44a97b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc117e19b463aa9e5ad3a39d9124a4f2ca0099e98efd9c3385529c44b8334dfd`  
		Last Modified: Wed, 29 Jan 2025 00:38:50 GMT  
		Size: 35.5 MB (35522617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb952143b00c8375516413bd9eccb48aeaa5f6efde247c8a2b3b39316449eb16`  
		Last Modified: Wed, 29 Jan 2025 00:38:49 GMT  
		Size: 6.7 MB (6731707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0a1a7d8050b79a5a909b117dff600785f0afac98b30ecb34010d6826a86cea`  
		Last Modified: Wed, 29 Jan 2025 00:38:49 GMT  
		Size: 1.1 MB (1133181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174794a1df054f599cd5583ee9c85146c461dca7490b285b3a7bae60744b551b`  
		Last Modified: Wed, 29 Jan 2025 00:41:14 GMT  
		Size: 18.4 MB (18359040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c19bc359e11b45b0714bc1407db9a680b2192daa7cf2b30159d1199bdea6ce8`  
		Last Modified: Wed, 29 Jan 2025 00:41:09 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1dec433b3ac6891cafdd15710c30440b76371f710c589e37bf249a3f73c5ca`  
		Last Modified: Wed, 29 Jan 2025 00:41:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4dd7f2ae8ccab70a06559fa1d946ce931b96dd1cee7ba87ec0ca874eea0128`  
		Last Modified: Wed, 29 Jan 2025 00:41:09 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfefa96194ccd088fdd06ce146be1d93d52082d570acb896c5cf0b543545cc`  
		Last Modified: Wed, 29 Jan 2025 00:41:10 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7f98f2a31ed4db957f6dcc27b1e38cdebc309bc8988b953fc06c0fdce17fff55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6494313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899963e2c80019d05371a1fa2bbaa74e15a47660751c445b39764a5898feb2da`

```dockerfile
```

-	Layers:
	-	`sha256:3e02c316cd5bc24a6d6d170ba3a018bdd2741239d8f110840dbb9529e22e29bb`  
		Last Modified: Wed, 29 Jan 2025 00:41:08 GMT  
		Size: 653.9 KB (653927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2bd1763f6facf6fc02b3148254e1e1d7a18dac7a8523223af6269339a63d44e`  
		Last Modified: Wed, 29 Jan 2025 00:41:09 GMT  
		Size: 3.0 MB (2967731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3777ae275d946f0f600ee38fa370f2d3084f6c00ba3c17502d507a7d9122aaa2`  
		Last Modified: Wed, 29 Jan 2025 00:41:08 GMT  
		Size: 2.8 MB (2812604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e264246963169560e1be4eff4d5677e40a78af2c40bc460e4c7a61cc31d1d3e8`  
		Last Modified: Wed, 29 Jan 2025 00:41:08 GMT  
		Size: 60.1 KB (60051 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:46929c5ec7e6d9e359e962af44876c6ef038228bc20885c9f97dd1e9f83c8ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76701849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae44ca94690e91a664d3b52f8e633149ec7e37fc1e9e2a8c9a5c94422215a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8f58a9acff87800b0001621a0abebfc3c9256c4c94a48a3a7fbcea584c0906`  
		Last Modified: Wed, 29 Jan 2025 00:50:53 GMT  
		Size: 43.0 MB (42994244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f1ae3712c034843f3ef3ad2102e119cbfc862fe0ee876934366fa40b1acc70`  
		Last Modified: Wed, 29 Jan 2025 00:50:52 GMT  
		Size: 9.0 MB (9031962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b652fcf3bb55aaa67496f9cccaf3d151c4085e26948a6d515ab1581a0397d`  
		Last Modified: Wed, 29 Jan 2025 00:50:52 GMT  
		Size: 2.3 MB (2322584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e6e9b92ecb6c11962ba107f458c6d2ed9d05822aec6de027f9bfdf79dd7792`  
		Last Modified: Wed, 29 Jan 2025 00:58:55 GMT  
		Size: 18.4 MB (18358954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9c2b80c4988201a62193fe3d34567b55ad2e1199d87645a624e17d6516489`  
		Last Modified: Wed, 29 Jan 2025 00:58:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7d1d63498f896f53f0ef9efa7d0720a606852a770d46f70faa25e0554f8827`  
		Last Modified: Wed, 29 Jan 2025 00:58:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9d8a21b4d94fdfef762c5ff747e44e9cb4b1ffb6d36d745a7134e10be4f953`  
		Last Modified: Wed, 29 Jan 2025 00:58:54 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6010d0d8083a866abca03c563674b4f27fc2ae7df76258d03b4ba247b291875`  
		Last Modified: Wed, 29 Jan 2025 00:58:55 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:85474863cb9fe796ae0832a80d47fd996eef2e0bb1394350b97f0666b89daee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6836921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b15f9109416f3aa4c49ad0db3336afdb2a00be9fdec04487253819140228c6`

```dockerfile
```

-	Layers:
	-	`sha256:21d7c6114bfec98d787bf609131cf7e9e29c0adb11ffb27ce4cad1878c29fb1c`  
		Last Modified: Wed, 29 Jan 2025 00:58:54 GMT  
		Size: 658.6 KB (658573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6326c1a4d43ab9a2828d69c185efcd0ebd6ca30f37d368baf26fb3de6412fe56`  
		Last Modified: Wed, 29 Jan 2025 00:58:54 GMT  
		Size: 3.1 MB (3136686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a5d979975296ab60a2cbfed880e959a296798e0e0deb0ae52829650ac04a6a`  
		Last Modified: Wed, 29 Jan 2025 00:58:54 GMT  
		Size: 3.0 MB (2981565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b95077383418843039ec72d3a6e6c21a0aed754da3b17ba1296c4b83736a805`  
		Last Modified: Wed, 29 Jan 2025 00:58:53 GMT  
		Size: 60.1 KB (60097 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:d5084c782019adf378b5f3ce047ec559428abc829a9fdc414af9417cc38e169a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67059780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916714d5dc35bd53fdea2dd52070bd6b26c35c1e82e6816db29e9ed12a671db6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac738741d5e9616fc8b3e37ef5bd70976e668c25ab1a95bbd50f997a7b262df`  
		Last Modified: Wed, 29 Jan 2025 00:34:12 GMT  
		Size: 35.7 MB (35685702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc009ff93fa8ca1a06ab03a8f55377a4635c01fa3ff38cf2952abbbeab46980`  
		Last Modified: Wed, 29 Jan 2025 00:34:11 GMT  
		Size: 8.3 MB (8320845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827a96678ba7a6bc87eaea3c5ce8362ebd8b533cce24e3e3588b5265a44a969`  
		Last Modified: Wed, 29 Jan 2025 00:34:11 GMT  
		Size: 1.2 MB (1229387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc456d6e5fd139d88e30b0bdb2bb2022ef1f423b04020aa2c58e877d82c5d136`  
		Last Modified: Wed, 29 Jan 2025 00:34:12 GMT  
		Size: 18.4 MB (18358972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6ab84dea7414b9c89f724bc8e0cad9987001a4a457ff2cb9d00c05215b521f`  
		Last Modified: Wed, 29 Jan 2025 00:34:12 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e93bcfac30ebf470f4c29a13382c911046be718a1d08779091eaf69181bc7d3`  
		Last Modified: Wed, 29 Jan 2025 00:34:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4612e56d9e1a46b550d75f23aa12ffb2e882826a4b6f35cc69561d34c50c24c9`  
		Last Modified: Wed, 29 Jan 2025 00:34:13 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a395e455db63b80cbccf1ea88daf95aaeac5d0a536b82c0b58d0352e75e600e`  
		Last Modified: Wed, 29 Jan 2025 00:34:13 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:07693bb4ea424a0d50a2491632a29b5698e788e3c50f58c6a83c587d2583af8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6431618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d8b480124b0b249897483eec1cc48da823878aecb362873dc188a2f3d12b18`

```dockerfile
```

-	Layers:
	-	`sha256:4868cded215471cebe80a3c7448523079f403953dbfec6a14eef487ab6b67a76`  
		Last Modified: Wed, 29 Jan 2025 00:34:11 GMT  
		Size: 533.6 KB (533587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba61b74f7cfcd5904eaae2dae8aa731cedcd7da53300b98501fd8e9ea7ddf449`  
		Last Modified: Wed, 29 Jan 2025 00:34:11 GMT  
		Size: 2.9 MB (2921199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6984b96d5cafd345ed37673cc21f82db2cfa755352d98b400ae7154b634bf053`  
		Last Modified: Wed, 29 Jan 2025 00:34:11 GMT  
		Size: 2.9 MB (2917025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a690880428859dc44b8933e8035eb78a11dd2f43227263ac322745bdc0f48932`  
		Last Modified: Wed, 29 Jan 2025 00:34:10 GMT  
		Size: 59.8 KB (59807 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:67261d2dfe9e91d180a4bd0b60050e830e3617902a316477abfb3d66d67ff999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68209866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a82cfe173608d19fc9b1679b185ac27e134e0bbe51398fe56c6515475cb33d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 07 Jan 2025 02:28:15 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53e5bb36b5dc0ab79ffe8362486b61d2e230bfc5f65e0c863695410ff3fa79e`  
		Last Modified: Thu, 09 Jan 2025 00:21:40 GMT  
		Size: 36.1 MB (36085885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53da1405ffcec279092e19a4e2871dea98e230594da7ab4f75c6fe2a6acd7c17`  
		Last Modified: Thu, 09 Jan 2025 00:21:39 GMT  
		Size: 8.8 MB (8844419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b34bba648bac3e531bcd2875754e6a724f60adb4e6b90ba2cfcc89f8a246da`  
		Last Modified: Thu, 09 Jan 2025 00:21:39 GMT  
		Size: 1.3 MB (1345127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48378faf713277fe62639d257c1231c9a0fd6293b96efbf85f0dfb3e0cf349a1`  
		Last Modified: Thu, 09 Jan 2025 00:26:00 GMT  
		Size: 18.4 MB (18359086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82c30e5e4eb56faac4332bf3784ebc47bf268f8320c11a6436a892c6dfd149c`  
		Last Modified: Thu, 09 Jan 2025 00:26:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d670272438de41a17bfbe816437107fa63d14a6b324790b188d44bf8004832b6`  
		Last Modified: Thu, 09 Jan 2025 00:25:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ddac9fb85f38938afe12eaa3eb0568be4f2038c32dc96327ede681ed6b04bd`  
		Last Modified: Thu, 09 Jan 2025 00:26:00 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fddebf6c3b7264acce55ba08884d2f3f6777fdf049fe6ff41f85dbdb6b71d9a`  
		Last Modified: Thu, 09 Jan 2025 00:26:00 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:eefc28a462ffc07046bfe6256c07fd9fd92cb8266d610fcc21b9ae4cffd7fe52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6733282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06691df451757eb3a02691d774d5d4fa32e258599cbe11007a446b901a18141a`

```dockerfile
```

-	Layers:
	-	`sha256:90ab5a2c2eae652293c44bb70e09681aec8fd09f98d075671570468d67ab74cc`  
		Last Modified: Thu, 09 Jan 2025 00:25:59 GMT  
		Size: 652.0 KB (651952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1ebda393777ae7145f3c2eb079d3248613addabaafe3fdd4172ea85c6d5366`  
		Last Modified: Thu, 09 Jan 2025 00:26:00 GMT  
		Size: 3.1 MB (3087613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee2e47aaa69d845df01b8c0f422471948e18123fb547384a230bd2d165192aa`  
		Last Modified: Thu, 09 Jan 2025 00:26:00 GMT  
		Size: 2.9 MB (2932782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe620c1468eb1a05071a63555587ba8ba3b43bd246963eaad60d881a6fd8eb83`  
		Last Modified: Thu, 09 Jan 2025 00:25:59 GMT  
		Size: 60.9 KB (60935 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:1dcf6aaf8f9ffe3a5653fb2e60af48f19a20ca8de836b65a7cfde7aaf5307e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69858660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd327a34fcdc223067cc7745b081754eb8e52c2289bd8c2f79be7aaaf0bb4d24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 07 Jan 2025 02:28:15 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Tue, 07 Jan 2025 02:28:15 GMT
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
ENV RABBITMQ_VERSION=4.0.5
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c184a89710c8bf6b4bd56e06ad64c34ca66c111bdd470b3d64ae635ba9654367`  
		Last Modified: Fri, 10 Jan 2025 23:11:02 GMT  
		Size: 37.0 MB (37028486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedb918ea46e955df9ad502d010c6961d291010c1cf928ac046aedf3e2ff9f89`  
		Last Modified: Fri, 10 Jan 2025 23:10:58 GMT  
		Size: 9.9 MB (9854297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4728a0f84ea00a6aeadb4cd0f01ba9ef56b0abcde3a385cfc858d558b11145`  
		Last Modified: Fri, 10 Jan 2025 23:10:56 GMT  
		Size: 1.3 MB (1265051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e74cc32308c95ba208fb10165d701b7d5afb376d5aa8fe0678df234762986`  
		Last Modified: Sat, 11 Jan 2025 00:28:48 GMT  
		Size: 18.4 MB (18358828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73482a413608db3038fa2ba40fb90dd6367b5a99b35a1fd0d9df053d9e761c6a`  
		Last Modified: Sat, 11 Jan 2025 00:28:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0fe1f8168995e4625bb47a956935263cfdca6fdc97e26553d2a8700f932325`  
		Last Modified: Sat, 11 Jan 2025 00:28:45 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d126e703452af2bb78a672b1753139d4c2878e941653816682a07c98f5c1c0a`  
		Last Modified: Sat, 11 Jan 2025 00:28:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9f8cbd44036bc0f83c6cfbc82dcf516cbac9ee1bae6187c4162ebf0f202bc8`  
		Last Modified: Sat, 11 Jan 2025 00:28:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3fc11c6e928079885cdb335a8af1b77f29723b2f01bdec3c2e0eb888cf7ba7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6811396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d26b4258284a755b38002060a230c7b0952baf9fb0c456cb4fa0c8dde2dd20`

```dockerfile
```

-	Layers:
	-	`sha256:fda786ab69ee3c594d6a6c31c964ea0a0417ce1bb44f848f56e9237ec5969e0b`  
		Last Modified: Sat, 11 Jan 2025 00:28:45 GMT  
		Size: 654.7 KB (654744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d81cfbae2f64bcd6ed088c89f68a1c68a90f5b740a9db4098d620b3c2722e6`  
		Last Modified: Sat, 11 Jan 2025 00:28:45 GMT  
		Size: 3.1 MB (3125268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f266233d6ee64f2c16c01da2f4c89ca10f97760167a06b477b50ff2376d87aa9`  
		Last Modified: Sat, 11 Jan 2025 00:28:45 GMT  
		Size: 3.0 MB (2970449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8a3984ed3796ff782b26549e22332ad1627434e770e43ce87939655d381499f`  
		Last Modified: Sat, 11 Jan 2025 00:28:45 GMT  
		Size: 60.9 KB (60935 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:48b116265e30c9b7335cfbc9830fa08c47893b03266e9bf47c380edf7e758133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66758846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c4e83eab42ad9e1f6f108b13818aed470c8bf71e7f330fd2854b82825dfe78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e7ec3661f28c633af65628e75c3aeff0fe6522edae893cf76aec6201e6770b`  
		Last Modified: Wed, 29 Jan 2025 00:56:05 GMT  
		Size: 36.1 MB (36099367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860e3671b3afc5e90689bb1bde6874463a54558112dfa07f347ea89ea2b2e4d1`  
		Last Modified: Wed, 29 Jan 2025 00:55:59 GMT  
		Size: 7.5 MB (7508437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564a1cc54b81f6890533accf323d81cfd5067c96dd971eb4f0dbcf28d24e9e04`  
		Last Modified: Wed, 29 Jan 2025 00:55:59 GMT  
		Size: 1.3 MB (1323335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1bf8cf6407dc0aa7ca22e884564b283c72fe56e8a046ca475e3ec59aab5852`  
		Last Modified: Wed, 29 Jan 2025 01:07:07 GMT  
		Size: 18.4 MB (18359093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb598c16278879ec943cdc6b0696fa639e12447a8007b93d8ee3b1aa63ad020c`  
		Last Modified: Wed, 29 Jan 2025 01:07:07 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1046cf2260e9604dd454b0934da282556eaa03948b04ee262f1856e7504614b3`  
		Last Modified: Wed, 29 Jan 2025 01:07:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ba506203ce0e70cf7f081340feefcf7109d86174b74f2927bf82007ff0acb0`  
		Last Modified: Wed, 29 Jan 2025 01:07:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4791d009ca776505d6cd9f3e97bedf9d37944fc2d0a4c440873e8912ed8059c5`  
		Last Modified: Wed, 29 Jan 2025 01:07:08 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d11b5e463111f71b5cdcd1cd2fdaf1937c1b1238883f72f4f5833b618db2fae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6512459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48389b2ae2c7dbca191e112f0e990400be4689d9e05f9a6528b1fd0d55750442`

```dockerfile
```

-	Layers:
	-	`sha256:a537f192cfbfc0aed07e278dbe660b59b95897af6a53a1936c96ace6c148fad0`  
		Last Modified: Wed, 29 Jan 2025 01:07:07 GMT  
		Size: 651.9 KB (651940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f018d9ea71699c7dcec7fca1ef3d11ffbce0293bbcf6a0691dc83606c483235`  
		Last Modified: Wed, 29 Jan 2025 01:07:06 GMT  
		Size: 3.0 MB (2977882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fb1e01bb0bef0a91691a13db911ac96b69957749f90155683f51d4b5f51c4a6`  
		Last Modified: Wed, 29 Jan 2025 01:07:06 GMT  
		Size: 2.8 MB (2822779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec95e95f71f705d0f2383a0a81a7c4de621fdf15c1abc3c4475c411b77f4ba40`  
		Last Modified: Wed, 29 Jan 2025 01:07:06 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json
