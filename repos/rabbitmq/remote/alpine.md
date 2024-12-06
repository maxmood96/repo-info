## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:5998f659cf218779f5b69ae8f125ea5278a273ca5efc1ab6587d166c528cd978
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
$ docker pull rabbitmq@sha256:30e5a3529b200cae41ce8226bd5f1b096d7942ea8325993510bcf12c58b381ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77334019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d83b8e465f91c06bd2379b518fcbc060dcc48c3371b0acd84eee397b78e1b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddaaabf9224ed9eaf7441170c4bcdb4e2e59b979d7fdca7a53e60f5d68fc6cc`  
		Last Modified: Fri, 06 Dec 2024 01:35:15 GMT  
		Size: 44.9 MB (44853332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa43f57328c902eafae5ddb8c2ba9ee6a513ba2972027baefecabb4f4f76c58`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 8.3 MB (8284894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c186a83774a6d9fccc30931093c5aba3e11071d7ef29b8d57e9d964bc8a14b0`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 2.2 MB (2234424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e30764cff116c607e970410dd2cf8015573ef0be359041909bc1e0bd09c71`  
		Last Modified: Fri, 06 Dec 2024 01:35:15 GMT  
		Size: 18.3 MB (18335716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2fc5ca9f8494504cd0553cd7f1d4fd796549acf12a7e4a08b1996fd4d9c415`  
		Last Modified: Fri, 06 Dec 2024 01:35:15 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bfaf79c4807c674b400161c99ca92895c5ca006df756436399f7dc6ea3e68e`  
		Last Modified: Fri, 06 Dec 2024 01:35:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dc778a90ed792e1547a80904eda79f6b60e5f2275c4e1221d5f9395beb5c3`  
		Last Modified: Fri, 06 Dec 2024 01:35:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4931c5c16e3b23eb718b71a75dbefcb42b25cd5829828985789dbf940e3d259`  
		Last Modified: Fri, 06 Dec 2024 01:35:16 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fd6c9f2b72dbb9a577c40cbc09a00bf6b6433780a1f070d557357318c14acc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6446313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a31da3a65d2f2f306a73c60f263529c2f24c98ea1c5bfa96d03e3af243dead`

```dockerfile
```

-	Layers:
	-	`sha256:b7633661cc98b6eb64e46f5424a8fad4c1c4adb887d6c2020b9249994905fa35`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 652.9 KB (652862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b58795b31930c995a1e59a077c1efb0abcdb0461e66c17e062381fa6aa59800`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 2.9 MB (2943279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61474e30b1b00a438b4a2c19af8a691ec7ff7560c4ed5e131ffb634ed43f261b`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 2.8 MB (2790314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:706a62c789f9ddf295ea9921c5a456496add4ab8ab9529aeabd51d31417fcf36`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:f2b52f5472061afcf660b7bcdd83a01355b04d57316f88b661cb7498186cd1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65507185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0964687826901a0449aa82483cf78d50c873295f6cecbafa1ad1a510a45e249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0794134a942e6e60d162d1d4334920e93fa78671a8367c4559f8e7f53c908c13`  
		Last Modified: Fri, 06 Dec 2024 01:37:58 GMT  
		Size: 35.5 MB (35493110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0736249ec07e66aab59f47d0cb5852197a49c0d9dc34189a98fb4f5bb59fe2`  
		Last Modified: Fri, 06 Dec 2024 01:37:58 GMT  
		Size: 7.1 MB (7079938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36d63138351898593b25cc098a1e48188c0cb1900ebd04f658a2a8f21f1a495`  
		Last Modified: Fri, 06 Dec 2024 01:37:57 GMT  
		Size: 1.2 MB (1230015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a342dcbf697f3a01b54c25544e51eb4824166634172e3ea5d4364aa9a2f93abf`  
		Last Modified: Fri, 06 Dec 2024 01:38:28 GMT  
		Size: 18.3 MB (18335774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c038a83e3fac0f1444a66b06b557c1267d019295c9f8d5d66798cdd67b65f2e`  
		Last Modified: Fri, 06 Dec 2024 01:38:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba49a562e829b78cc5ef7426ff1774ab963210b15b74d27a622b63d072e94fb9`  
		Last Modified: Fri, 06 Dec 2024 01:38:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eedcadd2169474b9be3b8ac054be1353132c936d84567746665c73a4be8bdc`  
		Last Modified: Fri, 06 Dec 2024 01:38:28 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2dd7ed8c54749c775a9427bf49820e049c0ebeaa9c41f6ecdafae686faf529`  
		Last Modified: Fri, 06 Dec 2024 01:38:28 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f5589f4ecf7ee54ac34663efa1ee965bb26c0eb2b1cc6c4d7043e356795163c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b99396439b1be91d2ae95babdcee0c82ba1a89124224d79773991e3cab9e97`

```dockerfile
```

-	Layers:
	-	`sha256:820dd68b9b1aa93787c83afa865886e1bfd97a980a1dfeb4931d8e4545e95f4b`  
		Last Modified: Fri, 06 Dec 2024 01:38:27 GMT  
		Size: 59.8 KB (59835 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:c32fa1dc347ac36ac2469f34770a4131d2e125e9b24964156a5650d902e54181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64680545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbc1d59ac345d837730fab1234ab778da1e2a81ec4ed8d088cd6fba4b909bd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c91cb83ff3375ca2e418d9ef94159d7dbe1b5ffd9b455e4211c0a78df52a302`  
		Last Modified: Fri, 06 Dec 2024 02:24:29 GMT  
		Size: 35.4 MB (35397778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b084a48a82704b20ee9a1b18ab20df3f98fb7eea5dc2965918b9f047a0e10f`  
		Last Modified: Fri, 06 Dec 2024 02:24:28 GMT  
		Size: 6.7 MB (6716582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af5b70f9a274183bbcc0d2f592d9638c2dd50ef4cb6f25c2d814c26864d1687`  
		Last Modified: Fri, 06 Dec 2024 02:24:28 GMT  
		Size: 1.1 MB (1132958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7e0eddd08ad70b1d2e57cb35a3482e66475466847ec8c7039a7aed555af3d3`  
		Last Modified: Fri, 06 Dec 2024 02:28:32 GMT  
		Size: 18.3 MB (18335998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72ba3f7edcd80eac49eb2341720039def401538eef1b49661294c6239c9928`  
		Last Modified: Fri, 06 Dec 2024 02:28:32 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942da215f54771fd661dcd90bf13496a1a645831fbe77a238d378770429c4475`  
		Last Modified: Fri, 06 Dec 2024 02:28:32 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175b4e14a9f9a677d48ef9ccb75d32572136c9cda82ee355680d65434fabc6b5`  
		Last Modified: Fri, 06 Dec 2024 02:28:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949a38d4de953a89f91eb21107babbe1c01f609ae4bbba1d2584726effc0e618`  
		Last Modified: Fri, 06 Dec 2024 02:28:33 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:03a186d2aa6c1bb0a5803c1e488439046f46fdd229a2dd662bb0b39e6af7ae43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6240319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937afc0e544939b04e0bdfb0824a005c28f37c6bda6ddfe943f6317ec020f2d3`

```dockerfile
```

-	Layers:
	-	`sha256:f0ee6e8d13b597ef43ec4ad585291f61b3b7a04fd3aefbcce6f84bd9e87d3046`  
		Last Modified: Fri, 06 Dec 2024 02:28:32 GMT  
		Size: 648.9 KB (648931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e9d283ff19e82bf3c32773227ed5206251dae81101aeba04f72a8f33b0b8e3`  
		Last Modified: Fri, 06 Dec 2024 02:28:32 GMT  
		Size: 2.8 MB (2842815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27649a41ca1700af12d25f975e6606fee1b58b2a4702b0ae6a8dc40d15d9c135`  
		Last Modified: Fri, 06 Dec 2024 02:28:32 GMT  
		Size: 2.7 MB (2688523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c5cc36d626a30f15f10ee2f418755f0473d93aa1433445e9b1c6f36648e403`  
		Last Modified: Fri, 06 Dec 2024 02:28:31 GMT  
		Size: 60.0 KB (60050 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:1657b65db9e1411f5a42c9bf44a1d59f787e0d205a2bab1a712582907c30dbc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1db455500c7ef5d692501d21107f92af4b58c4e50407dd710fa3b9f69c5c58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43f73a5049c200e88650aa274889ffa80c207abde28bd208a3fad8a20e8a35f`  
		Last Modified: Fri, 06 Dec 2024 02:28:56 GMT  
		Size: 42.7 MB (42723851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7314235fa2f7112e60b274242e1c22adf5f92c6c69f14a98b610e30d88d50369`  
		Last Modified: Fri, 06 Dec 2024 02:28:54 GMT  
		Size: 9.0 MB (8995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f3277025a5e5986632f58c4b3505e3d9237fb25486cdc8b6657e5279357706`  
		Last Modified: Fri, 06 Dec 2024 02:28:54 GMT  
		Size: 2.3 MB (2321293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3edbdce706cf6bb2904d27eecd43b5af8e8cac192267dd65db1bd417406aa40`  
		Last Modified: Fri, 06 Dec 2024 02:37:06 GMT  
		Size: 18.3 MB (18335742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c41a707b46357c0897cb291e51c81a5884593bd840efbc6d6c378e7adad8c4`  
		Last Modified: Fri, 06 Dec 2024 02:37:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0d7ff6a1355ec2fe3e1e2e531e8ccddba8b60bd0eebe6b65746781cc06c6df`  
		Last Modified: Fri, 06 Dec 2024 02:37:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a49262cab50536ca4cf58a078c64aaf5c21e1123770f75034a847f13f6517db`  
		Last Modified: Fri, 06 Dec 2024 02:37:06 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac2eecf7dcd49d05b2d2d2a90338607460b51b81f8735b51da8c6b42cc7f35e`  
		Last Modified: Fri, 06 Dec 2024 02:37:06 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:58b3a142f503c091decc77c4a20d3fd3bf675a78f152ca3462bb46c9d48b3937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6480949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe11a45d6be4e669a26c6d99facce2a1a8908a51c91a6429bbc8a4e7563662ae`

```dockerfile
```

-	Layers:
	-	`sha256:75ac0d843edeb21860ad1c7144860550fd7dfb721dfbd13df8356dad386dc0c0`  
		Last Modified: Fri, 06 Dec 2024 02:37:05 GMT  
		Size: 653.7 KB (653654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15b8ad1e7134d41691cb638160f5b0473382068d358629eee7d34f9802eb886`  
		Last Modified: Fri, 06 Dec 2024 02:37:05 GMT  
		Size: 3.0 MB (2960742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3023925c9b4702598218c10b5d4eee8aaa4343b8aa7eff12589f9766aec0e41b`  
		Last Modified: Fri, 06 Dec 2024 02:37:05 GMT  
		Size: 2.8 MB (2806456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:516303ea452c0e4b5d4465afc41903952c15cd182c84fc71433058428120262d`  
		Last Modified: Fri, 06 Dec 2024 02:37:05 GMT  
		Size: 60.1 KB (60097 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:617ac4a98aa3bf1d9ae4ccd0837323a958b7b906c6d3facaf60747ab81ccb256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67035645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c245a6347f39369fc3ad0179b7fb7a04c46a973ef31cf64ccb70917f83c23d53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7501b2f8e0c231a0e4a459ccfcbe0f2789ca11fd08ee49627a77c7baa1fd75`  
		Last Modified: Fri, 06 Dec 2024 01:34:51 GMT  
		Size: 35.7 MB (35672269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9872cf53cd4deae4f917eeabb15904a26a640249b57ae37a5dfdeab779ed7e09`  
		Last Modified: Fri, 06 Dec 2024 01:34:50 GMT  
		Size: 8.3 MB (8324928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ab324b838165f0536e59c22f213083d22fddf01ac21e4918d7f060f2bc1ef7`  
		Last Modified: Fri, 06 Dec 2024 01:34:50 GMT  
		Size: 1.2 MB (1231511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4304b7544b34a1c54c3b2795922e2d9ff14de936c195a91e882c2595d3e9b32f`  
		Last Modified: Fri, 06 Dec 2024 01:34:51 GMT  
		Size: 18.3 MB (18335970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f8743a9e35b47ee7b3402fd66f19e79c0a77ca3c12f2404335e07326c23116`  
		Last Modified: Fri, 06 Dec 2024 01:34:51 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb46cc14f62451725a4ade68e415b874ee35b267a2e8cb971fb18c9ef4c76dd`  
		Last Modified: Fri, 06 Dec 2024 01:34:52 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d583a0d59fc3adbad462347c7cad911f391314eec0f4645880dcb2d3b51f36a`  
		Last Modified: Fri, 06 Dec 2024 01:34:52 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b993963b3334108c56072d697f9c9308f229b6d6527abff41cdef6bd60e55c`  
		Last Modified: Fri, 06 Dec 2024 01:34:52 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f37b164e1cda6094557f4dcf7fadf3e3a40adc779be57e97a7120f2bc086f683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6421975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31e76f52fa80a63c23bbe2a0f90db2b0d83d86c64102d4503494aaa35bdef91`

```dockerfile
```

-	Layers:
	-	`sha256:9f30e17eb0d20abb1b76d36c1629e03bb81d8e9b3169889db540695e82272bae`  
		Last Modified: Fri, 06 Dec 2024 01:34:50 GMT  
		Size: 648.1 KB (648134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca51ebc9eacedbb222f30bbde8f1d0923b467290fb28d2e871199bb62e2f947`  
		Last Modified: Fri, 06 Dec 2024 01:34:50 GMT  
		Size: 2.9 MB (2933497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:548085561e0fdb8c62096ce9e2cae5cd9df9fbe708a8363807c5407c8e585199`  
		Last Modified: Fri, 06 Dec 2024 01:34:50 GMT  
		Size: 2.8 MB (2780536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32140d324e684502988bbbf6996e7d7aab2be33899070958fce402a8c417df78`  
		Last Modified: Fri, 06 Dec 2024 01:34:50 GMT  
		Size: 59.8 KB (59808 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:02c1b2c29e1f3c5adcc329e7c44b7fdb3ec6015df1fa7a10b0885d51272aeb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68048658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f301c5745f7fe940f5cca26b368923c988bbbe5623ccd77a6d29281c1aae68f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc4a421b70e9e390fecc425f4c52f849565f19e6beffe180af2a21ffd0f4621`  
		Last Modified: Fri, 06 Dec 2024 02:33:31 GMT  
		Size: 36.0 MB (35958228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3432bcc3d5211b22253a953950d85d51b55b7f916ae7ca086028069cb7451bc0`  
		Last Modified: Fri, 06 Dec 2024 02:33:30 GMT  
		Size: 8.8 MB (8834116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1577b40c1ded00a2a6cdf36b8eebb7a9c969c333e5894dc7d5bf30b05ac3089`  
		Last Modified: Fri, 06 Dec 2024 02:33:30 GMT  
		Size: 1.3 MB (1346112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977ab5bff01b8d7ccad6b4c7f2321235e78809a417dc7c700a6cb6783aea810b`  
		Last Modified: Fri, 06 Dec 2024 02:42:56 GMT  
		Size: 18.3 MB (18335989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4932cde176ded68fa0606461a79c95cbe5b57b82adfdd2d3f1d20cf05af212b1`  
		Last Modified: Fri, 06 Dec 2024 02:42:55 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0579838856d625f0ff07edae3c01f4c7fef669bfb8b584e8438240aebe75687f`  
		Last Modified: Fri, 06 Dec 2024 02:42:55 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ddae774e88986e5b18a9dccc45cf8930bc3b91edaae30fec3936f5f5e6706f`  
		Last Modified: Fri, 06 Dec 2024 02:42:55 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba05744fd2ad18e63cf5050d29a8aab6751b67f5f42f0f0bbbc76d40293ec54`  
		Last Modified: Fri, 06 Dec 2024 02:42:56 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b39cf18aee7d34dde0f5878ba0319a24437695b46fd37aa4ee8194bfd0046073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def37c8398e672cca66b5760df1851910a27c869ad47946cdc1ce28dbf4a5b1f`

```dockerfile
```

-	Layers:
	-	`sha256:9284df48b83e2b0566cc66de6f90800c75674e9a7f17ffae17cbd1fc31635bdc`  
		Last Modified: Fri, 06 Dec 2024 02:42:55 GMT  
		Size: 647.0 KB (646975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88ce46b93796ae41febd81e01c9fe27fcce611620bd3623bb2b96f76f385177`  
		Last Modified: Fri, 06 Dec 2024 02:42:55 GMT  
		Size: 2.9 MB (2933220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f427656bc9e2f756dbbf0d87d90722e762ba513123acda97c5ee302f05c922`  
		Last Modified: Fri, 06 Dec 2024 02:42:55 GMT  
		Size: 2.8 MB (2778922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d343aede1015a5afa08a9610cd198a3a82de6dced03bcfb8a1b6c7a5a0477e`  
		Last Modified: Fri, 06 Dec 2024 02:42:55 GMT  
		Size: 59.9 KB (59919 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:fc4006eda55281827096063b45bf59e06b40bc7190b4a1f9831915174dc8b90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69713375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec30d38380e4012bcfe2d980e800e7e946923dbe4e022e50d1c70ec164520ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 22 Nov 2024 21:01:04 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Nov 2024 21:01:04 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Nov 2024 21:01:04 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 21:01:04 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Nov 2024 21:01:04 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
ENV RABBITMQ_VERSION=4.0.4
# Fri, 22 Nov 2024 21:01:04 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Nov 2024 21:01:04 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Nov 2024 21:01:04 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 21:01:04 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Nov 2024 21:01:04 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Nov 2024 21:01:04 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Nov 2024 21:01:04 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 21:01:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Nov 2024 21:01:04 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Nov 2024 21:01:04 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7e287f09d6c914fb18f344d2605d174765bad222603808a8cf70fa340266f5`  
		Last Modified: Sat, 16 Nov 2024 03:27:04 GMT  
		Size: 36.9 MB (36866962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612f8628ef34bcf66b3b2dd82b2bf7c775d334574273308aec9a2409f06a9b1d`  
		Last Modified: Sat, 16 Nov 2024 03:26:59 GMT  
		Size: 9.9 MB (9866549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b8118b806f7abcfa3dba4e254b2c2c2bf92f4da271d8e2bca0330715a189cb`  
		Last Modified: Sat, 16 Nov 2024 03:26:59 GMT  
		Size: 1.3 MB (1270919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159125f9829d753e4730d577e60f067ac7988002f523fec37e71b176b9d762c9`  
		Last Modified: Sat, 23 Nov 2024 04:06:50 GMT  
		Size: 18.3 MB (18335720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365705bbabbd21b732b11a68d39a3e7752378728bc901e5587bd6aedae602a3a`  
		Last Modified: Sat, 23 Nov 2024 04:06:48 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11964b34fd91a98ce8b726a1557e696606dbfdee6a3cbc59d5a78f809d922de9`  
		Last Modified: Sat, 23 Nov 2024 04:06:48 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b78fc1773b242ef76f63c9be9e8528a6fd3d30927a5e045eb9e8a33ad98f019`  
		Last Modified: Sat, 23 Nov 2024 04:06:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa027774b9e2c2a73ecac524d09fe199ec9ab54314faf757ee0c52a0e72a6ab`  
		Last Modified: Sat, 23 Nov 2024 04:06:49 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5ff6d4b3e2827144722259cdf4784ba3c1c164b79a66428af03e541066d0d530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee8e9d20e80195bf16198288d3a56842b71ca8e3d42e0ce9b760499e8728fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0704828b3f85fb1a333600fc01107afa000ec2703f56d39192387221298aff70`  
		Last Modified: Sat, 23 Nov 2024 04:06:48 GMT  
		Size: 649.8 KB (649818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1712537b97762484e20b139b385203b81fb979aef8f93539c4eec15c2718a80`  
		Last Modified: Sat, 23 Nov 2024 04:06:48 GMT  
		Size: 2.9 MB (2949343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da2a911f0387fe501265058f5d08489d0d5e1451ad11d669f5d53f59f890a4b`  
		Last Modified: Sat, 23 Nov 2024 04:06:48 GMT  
		Size: 2.8 MB (2795057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e82812cf610cff97e438c15cdafd2e9640f239da6ebb983d0acc841e75eb7f`  
		Last Modified: Sat, 23 Nov 2024 04:06:47 GMT  
		Size: 59.9 KB (59920 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:5708362822dea0b5832bddd97caa08b2c0994b9b84a9f249735eaf8da2dba2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66615918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7d9467b05e6ff79065fe0a6d151a8ed4719ab65fba527e1a61b020a3dfbc87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Dec 2024 18:32:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_VERSION=4.0.4
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Dec 2024 18:32:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 18:32:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Dec 2024 18:32:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Dec 2024 18:32:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Dec 2024 18:32:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 18:32:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 18:32:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Dec 2024 18:32:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff66e1f1de64a33fc7cfd252eb6e9b83237a63fbc613f269e3cb830264837ab1`  
		Last Modified: Fri, 06 Dec 2024 02:26:53 GMT  
		Size: 36.0 MB (36009577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a11ec00b8f0415fbe7c81222c7cfded7ab6fdc35147fcefc625e331adf3550`  
		Last Modified: Fri, 06 Dec 2024 02:26:52 GMT  
		Size: 7.5 MB (7481783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7707e4350ea044bb6b65e87349a7c2bab89a21005fc8a0ac10c3415dc8a73fd3`  
		Last Modified: Fri, 06 Dec 2024 02:26:52 GMT  
		Size: 1.3 MB (1325194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a349be80cd692499a71bed4133a7f19f93efd7c11a4e7263cd272d1c5052a1a2`  
		Last Modified: Fri, 06 Dec 2024 02:37:43 GMT  
		Size: 18.3 MB (18336012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104e8defd1185dc6474b3889cb58981c9279e580f7f4bd1d17b4369e2cccabe8`  
		Last Modified: Fri, 06 Dec 2024 02:37:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23ccf2a4afa8c728a69fd2e881ed6e5d2a3abbef1232f147fd762545e2639bc`  
		Last Modified: Fri, 06 Dec 2024 02:37:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993e4ec2ef49ee0675c68eb507b99007c3030b336ac9d65c5cfab7520bf7468c`  
		Last Modified: Fri, 06 Dec 2024 02:37:43 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dcf7327ed33b363e92eea9936a9c61d78a5500487f98f42fc7afc650087dab`  
		Last Modified: Fri, 06 Dec 2024 02:37:44 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:732e59523223fcef65f1d323e49b653425d4f9e31f78d33d60e3ca31ba2e694b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6253076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0ffdbf36acefc7358f59f24603d12efc9622634e3fa4894164f22d1095de14`

```dockerfile
```

-	Layers:
	-	`sha256:592c4d0594920056cd588a40e990647eee47f172d792b8de2c03f7bb55f93b8a`  
		Last Modified: Fri, 06 Dec 2024 02:37:43 GMT  
		Size: 646.9 KB (646941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1da9643a209850e9fef2fdd2139f736a4bed4328a33b869b20543aaee61ba8b`  
		Last Modified: Fri, 06 Dec 2024 02:37:43 GMT  
		Size: 2.9 MB (2850273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32c0d05fdef51a91de8142ceb30a6d51fba0784ec91ef9fe833f27eabfd805c9`  
		Last Modified: Fri, 06 Dec 2024 02:37:43 GMT  
		Size: 2.7 MB (2696005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ec1a0544d9e20c954091ca840ac8a25d7a79b6b9e14166955b2e3ebf5459dc`  
		Last Modified: Fri, 06 Dec 2024 02:37:43 GMT  
		Size: 59.9 KB (59857 bytes)  
		MIME: application/vnd.in-toto+json
