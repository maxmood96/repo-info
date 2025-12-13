## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:96bac8ae5f1d734aee33b45624dae44be7414a5bfc2318c2e33b10580e8df786
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
$ docker pull rabbitmq@sha256:71b06effd4bfcd2e0b58f4c47384a37d88f023ddf74fb6956b2bf97f0792f250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83418653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45639148959b292328a4563b828a48d3c187eecfcad31d03fb8cec975fc85ae4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Sat, 13 Dec 2025 00:25:31 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:25:31 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:25:31 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:25:31 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:25:31 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:31 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 13 Dec 2025 00:25:34 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:25:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:25:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:25:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:39 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:25:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:25:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:25:40 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:40 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:25:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:25:40 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:25:40 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:25:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:25:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:25:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f080173b4211ee27145632ee2de1abf9a7a2b8b507bb6b6f4fb7555c345c2e63`  
		Last Modified: Sat, 13 Dec 2025 00:26:15 GMT  
		Size: 42.6 MB (42598933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67f17961c01122f2eb59f5c24c1e6756dd2da8cd4aa6e915871b25c6e75965`  
		Last Modified: Sat, 13 Dec 2025 00:26:07 GMT  
		Size: 9.2 MB (9206824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad04e9d3f46125199c073c448d0cbcba76b8443087da80ac5ab4551690fe7944`  
		Last Modified: Sat, 13 Dec 2025 00:26:06 GMT  
		Size: 2.5 MB (2465540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab3e3d9ac34049b7486f29779291731bb50d407f5a720362ca9bb4362d0f441`  
		Last Modified: Sat, 13 Dec 2025 00:26:10 GMT  
		Size: 25.3 MB (25286295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e139fd37ec010047c4a4a6e1392fa3a7a43ec5c55e4a7b2de96e45ffa94cef`  
		Last Modified: Sat, 13 Dec 2025 00:26:07 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2643146a2a95ee0258ab761119dc8fa4b2c00e4e04a0a0cb6ef231a4e129182a`  
		Last Modified: Sat, 13 Dec 2025 00:26:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c98189ac5bf428dc2d7750155c29e5445fca032b55a41be91d3b6982949209`  
		Last Modified: Sat, 13 Dec 2025 00:26:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53df893c997474879a429393d072e1e600a867b0b7bf87fc2bfcb61143777ea`  
		Last Modified: Sat, 13 Dec 2025 00:26:08 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b0f0c8f4d8d8bacf6cefc07e7af6cbe391cf63bc9428c1f8db2c4ff708976d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3599cbf46e2cbd43407476f7394ad066d0facfe3d8f2e601d9a5839b60e8af1e`

```dockerfile
```

-	Layers:
	-	`sha256:e1da5086555b0687e2ba8e54f0c072499b0ad353682cc550b9099412bc532cbd`  
		Last Modified: Sat, 13 Dec 2025 01:53:06 GMT  
		Size: 677.0 KB (676964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f614e05d96e677f944ec1b51a66142c00d487a37b05af00db492b4b3ebac15dc`  
		Last Modified: Sat, 13 Dec 2025 01:53:08 GMT  
		Size: 3.2 MB (3190316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc349ae499b0a6f3b2b30187f3e0de9a9f714a3192df84af89ed6c02a513cb1`  
		Last Modified: Sat, 13 Dec 2025 01:53:08 GMT  
		Size: 3.0 MB (3036751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928009ebacb78ef1c2b9a471d4c25f3a8c20f0839119d0cf8f4d1f07a1b87b89`  
		Last Modified: Sat, 13 Dec 2025 01:53:09 GMT  
		Size: 60.3 KB (60308 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:ee245eb3f2ef7e1a218fb1c910e25173cbca336d3751b048ec6767051d52a889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71621772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8353981425bac028178748bad0e48e1163c4770db0635dd3c1d0a3fbde5b73b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Sat, 13 Dec 2025 00:24:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:24:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:24:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:24:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:24:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:24:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:24:57 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 13 Dec 2025 00:24:57 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:24:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:24:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:24:57 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:05 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:25:07 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:25:07 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:25:07 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:07 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:25:07 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:25:07 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:25:07 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:25:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:25:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:25:07 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:25:07 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6708ab37d9dae87885aaa7a8327ab95b047b329b2bee3a853bd9dba27d781c8`  
		Last Modified: Sat, 13 Dec 2025 00:25:28 GMT  
		Size: 33.5 MB (33504380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6f99e5d43a1bb5ecaa85aaf2cd62f51a6ee07a513e1618afb0171e4bc123bf`  
		Last Modified: Sat, 13 Dec 2025 00:25:31 GMT  
		Size: 7.9 MB (7857233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cdafb549d333de23337eb7cde3bd897e2d514a28743118a8612fce34d28f58`  
		Last Modified: Sat, 13 Dec 2025 00:25:25 GMT  
		Size: 1.4 MB (1404611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dd25104c64be3ddb4a6f3017b9979240bea58b137c8616a077ac696c3fd640`  
		Last Modified: Sat, 13 Dec 2025 00:25:27 GMT  
		Size: 25.3 MB (25285905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d4f959ee36583d0b8f967d2a69d53b2bc541998ca214858cc2d9d72fd489ce`  
		Last Modified: Sat, 13 Dec 2025 00:25:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ba478caac5461c66f255c521402cb37c7f2b477817d93082d008fbcf508bb5`  
		Last Modified: Sat, 13 Dec 2025 00:25:26 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f7777dbaff3ab1db0cb415571355fb8fd3ecfa7db16397e0a8a2be6cbeb925`  
		Last Modified: Sat, 13 Dec 2025 00:25:26 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096bd2814d7bac45c0f3fe77682f1844e2e55599748cddd099445e57d2b89692`  
		Last Modified: Sat, 13 Dec 2025 00:25:26 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:26254509ac1cd15bfe7432724d6d3061d777917781052244bf42b097e041a205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 KB (60289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af74a0075c4bb25413ed7f2f16c0a1a33c1b1787a472f5e376392f2f9be068ad`

```dockerfile
```

-	Layers:
	-	`sha256:c9dc6168e3c0f82e7f71e7637c4dbef534608d12c8c0f3222625f982e166b397`  
		Last Modified: Sat, 13 Dec 2025 01:53:13 GMT  
		Size: 60.3 KB (60289 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:300ccd24f9d92fdb2fa8ffc4855fcac946f235b1c91cfc2063f117237a2016b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70718946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92d2ad947ffa2adf83b7062e1b5b766c1cbee943a961802efeec8cd413f02bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Sat, 13 Dec 2025 00:26:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:26:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:26:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:26:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:26:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:26:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:26:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 13 Dec 2025 00:26:16 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:26:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:26:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:26:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:26:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:26:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:26:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:26:22 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:26:22 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:26:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:26:22 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:26:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:26:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:26:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:26:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:26:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02e844aeb7d651bd7f9f83bdd8dccae0aad4b075feb023a936ef7372d293362`  
		Last Modified: Sat, 13 Dec 2025 00:26:51 GMT  
		Size: 33.4 MB (33410116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22898aa1b92fda9f9b11aff670e02a833e10f37585482301968220042ddaa101`  
		Last Modified: Sat, 13 Dec 2025 00:26:47 GMT  
		Size: 7.4 MB (7447251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964a9f4daed62082bb13d4eef4b5703bfa38ba6c5908c48b6d764efb5caa310a`  
		Last Modified: Sat, 13 Dec 2025 00:26:46 GMT  
		Size: 1.3 MB (1295850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a363ee4b46f43c0c6d014a4333ac2db7d0358a7b6531f23838637004fa799c0`  
		Last Modified: Sat, 13 Dec 2025 00:26:47 GMT  
		Size: 25.3 MB (25285518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e0cc447e6776c5f32791177127ca8fe6621f80fe55bbb4693d0bac755c0b3a`  
		Last Modified: Sat, 13 Dec 2025 00:26:46 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3008b8aa7062527dab4172b54cc931a493114b1e968f7a697478eec6be41289d`  
		Last Modified: Sat, 13 Dec 2025 00:26:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f2781d75b7147ce86dae71c346b4bcf69cce81335a2f8160bfeb75e468dac`  
		Last Modified: Sat, 13 Dec 2025 00:26:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613ab7d894079660c7a68441624081326beb14d948eb91da9fddc04577aadef3`  
		Last Modified: Sat, 13 Dec 2025 00:26:46 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:40c7c127793a4f0e1824d4f2a54b27909e9f584bbeb11b7fb03f5a4de294e53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6691331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116a385d2af9d7f3061d6478c95beb213be199848c2d1d51ffce133ed9913ee0`

```dockerfile
```

-	Layers:
	-	`sha256:df1029e9e573734fce5db74af3a93ca537af680144bd150aa839ff2bf54093ca`  
		Last Modified: Sat, 13 Dec 2025 01:53:42 GMT  
		Size: 672.1 KB (672107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a54e0ee69affbdcd7f705fd753924dcced7217c24003b33fbe51a46f2cbe6b0`  
		Last Modified: Sat, 13 Dec 2025 01:53:42 GMT  
		Size: 3.1 MB (3056807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e91deaea63053cc580d976579a9709eecb921bfb05f90ccff45689ba7fd6cde`  
		Last Modified: Sat, 13 Dec 2025 01:53:45 GMT  
		Size: 2.9 MB (2901913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54fcb8f38b5c85969b752a55aa2c86f6daa10900b1714c1effd005cdc50de42c`  
		Last Modified: Sat, 13 Dec 2025 01:53:46 GMT  
		Size: 60.5 KB (60504 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:749adf2b61a783194d1b87a6de51caf4ec08d5076ecb302add3a625af4f8cb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82440526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48992555b14a527e02d306cca92d6f1846b0530cf3489c0ab16190dfe38b07d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Sat, 13 Dec 2025 00:25:17 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:25:17 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:25:17 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:25:17 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:25:17 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:17 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 13 Dec 2025 00:25:19 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:25:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:25:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:25:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:25:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:25:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:25:26 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:26 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:25:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:25:26 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:25:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:25:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:25:27 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:25:27 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fa1251c34dfd415fc5474d390dc844529f24f56be2c3b5a1dc4580776aa371`  
		Last Modified: Sat, 13 Dec 2025 00:26:07 GMT  
		Size: 40.5 MB (40454863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120534dd5703d981d9fd073751d8beb375e21aaac8f059f9c5c9db0558202286`  
		Last Modified: Sat, 13 Dec 2025 00:26:03 GMT  
		Size: 10.0 MB (9987903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15d76445f37c277b4522d48c158ebaa21a41b55ab1df066940ee764d05258f6`  
		Last Modified: Sat, 13 Dec 2025 00:26:03 GMT  
		Size: 2.5 MB (2514368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4885c4f8b7b5f5ca0518ddf7010b6ee5975d774d10c4dd0be61ce5524a4824`  
		Last Modified: Sat, 13 Dec 2025 00:26:05 GMT  
		Size: 25.3 MB (25286444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bfa333c3e84c9620bb8cf3a0696c8209e93309ede16b7463bf466a2f89428b`  
		Last Modified: Sat, 13 Dec 2025 00:26:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404ea0dd3a1c7862dc70a61fd04966fe40ecfccc9bf57f26bc59a754cd51365a`  
		Last Modified: Sat, 13 Dec 2025 00:26:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a5afa8306a728062144c17de9984430c76ead65d02d1a29a041acd5dc5389`  
		Last Modified: Sat, 13 Dec 2025 00:26:02 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e408e210712404116cc1b6dad24cf2ccce28ed9e6a4ae5e54a85e6f52897553`  
		Last Modified: Sat, 13 Dec 2025 00:26:02 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:76eadb3264588b413bf71b44d6abdcf70839d58e3f17827531b204bd8cee3011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7037315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846d88e81dfbe4894f8ab926f5e3fedca3b8ef9e1212163fe73f209368092aa1`

```dockerfile
```

-	Layers:
	-	`sha256:a6ca0fbc5e2cc4440be62ad5027fe03174eaafcdc4547ace013c4817de2a45c2`  
		Last Modified: Sat, 13 Dec 2025 01:53:50 GMT  
		Size: 677.1 KB (677107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d2078e7e4f50529b940da2bba85ed4b8a9bb02554de512cccff99bedad9bb3`  
		Last Modified: Sat, 13 Dec 2025 01:53:51 GMT  
		Size: 3.2 MB (3227275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f4224af709f759a8e27f1d13ed2981d750f787596dbb82210b10f38154114`  
		Last Modified: Sat, 13 Dec 2025 01:53:52 GMT  
		Size: 3.1 MB (3072387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afd6d26a2887f51f79b9dd1c5222805edcfb33d22070ffd93ab04198ac56054`  
		Last Modified: Sat, 13 Dec 2025 01:53:52 GMT  
		Size: 60.5 KB (60546 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:85d4ae0ae383aa9068ae4e8c5702b401e314e5673ff6e97faa55efcbbbd8587d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73039086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7f63a1837f0497119adcb77fd4fe95e056182b85844c462d9b95127fdf7d1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Sat, 13 Dec 2025 00:25:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:25:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:25:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:25:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:25:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:35 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 13 Dec 2025 00:25:35 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:25:35 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:25:35 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:25:35 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:41 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:25:42 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:25:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:25:42 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:42 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:25:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:25:42 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:25:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:25:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:25:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:25:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:25:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2110201f8f3f714e3f27b141c007a7ba6f8053e869078d2ca56f32082a4449`  
		Last Modified: Sat, 13 Dec 2025 00:26:18 GMT  
		Size: 33.5 MB (33459178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09da029dc037432a15804cda8a453ef83acc2f66235a528e8a2ee10c4b8b0719`  
		Last Modified: Sat, 13 Dec 2025 00:26:15 GMT  
		Size: 9.2 MB (9197843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7762b8e6b5b72745e71ee9b35379da377da4124219739e7aff9b1b2598237985`  
		Last Modified: Sat, 13 Dec 2025 00:26:13 GMT  
		Size: 1.4 MB (1408961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b40cf4e75d380f11dda305d9c32f3977f21d1ecbae9d7698da3ddecbb698da`  
		Last Modified: Sat, 13 Dec 2025 00:26:16 GMT  
		Size: 25.3 MB (25285498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759fffa986d8a46329c91af106bf5f6213f2e6ae532e4459921b3c2aeb4aaa03`  
		Last Modified: Sat, 13 Dec 2025 00:26:13 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1760c26468a7557be212ae856c4df11deedaec924d645b7f0034f810dd1ba1d`  
		Last Modified: Sat, 13 Dec 2025 00:26:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc69b3978fe117ab19096484b9e080efcb003bdeafb9d2336dbae6cf5b97438`  
		Last Modified: Sat, 13 Dec 2025 00:26:13 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118d983483ec44e9b6ca9aefd62975123137b94afdeab2cbd58074305fb8d6d`  
		Last Modified: Sat, 13 Dec 2025 00:26:14 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3cdbcb17832e4bbaef137429aa548d64da2b08c4668321547a66841e6e86fb95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6915794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511ddfa9909cc05ff61edadf5fa449eea982680e79186d81587ed26c78a28066`

```dockerfile
```

-	Layers:
	-	`sha256:1a6787551c14f791fd9ce07d71999da0a2f4d64d280e60ce44b70447e1923b88`  
		Last Modified: Sat, 13 Dec 2025 01:53:57 GMT  
		Size: 672.0 KB (671959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7fd0792770230f166cf04676f07fdd0245266ca995628ed28803a1282b49d58`  
		Last Modified: Sat, 13 Dec 2025 01:53:58 GMT  
		Size: 3.2 MB (3168569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af695403ff2070aba819077bf47ed3a6520311b6844504a26986f519735e20e`  
		Last Modified: Sat, 13 Dec 2025 01:53:59 GMT  
		Size: 3.0 MB (3015008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d3c3d45c38373ca918e0fc7e04b006407bb635698b07caaa4110e742207266`  
		Last Modified: Sat, 13 Dec 2025 01:54:00 GMT  
		Size: 60.3 KB (60258 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:4477c98ea3f2e204d7d022098ca811390750d1544c4fab09ca14d3336248cbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74680732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e704da83a7146a8c29600621217465db893969614a80a58962ac68d4898f0c81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Sat, 13 Dec 2025 00:25:18 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:25:18 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:25:18 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:25:18 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:25:18 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:18 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 13 Dec 2025 00:25:22 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:25:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:25:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:25:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:33 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:25:35 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:25:36 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:25:36 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:36 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:25:36 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:25:36 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:25:36 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:25:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:25:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:25:37 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:25:37 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af8902fd1c6b13b1867e0689acf6ef02b225deeeb4cd9dd7c3ba54264046d0b`  
		Last Modified: Sat, 13 Dec 2025 00:26:36 GMT  
		Size: 34.1 MB (34067420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5c79338ef7d51c9f2996d5437fd6d89952bd0e231802dce36bd67fb7388841`  
		Last Modified: Sat, 13 Dec 2025 00:26:35 GMT  
		Size: 10.0 MB (9956668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c487ce5b4000841d669a5eae972980b9b7b78a00fe6b7b20f9c49da721ed99`  
		Last Modified: Sat, 13 Dec 2025 00:26:34 GMT  
		Size: 1.5 MB (1542624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d50ecde10f67ec95bc1d959db10e84f72f46107c0d2c1ac490b0a18ce807e09`  
		Last Modified: Sat, 13 Dec 2025 00:26:38 GMT  
		Size: 25.3 MB (25285254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ac5d7ac22bec463e0810c66e9badf6622366f876591ca4e0944b5e9dfa7c57`  
		Last Modified: Sat, 13 Dec 2025 00:26:38 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f5555b944b91007be5866a8eaf3820d7a5f9c932211c1141f41352ecf085a6`  
		Last Modified: Sat, 13 Dec 2025 00:26:34 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34631afd5141a1aac4360770af8815db7f7e516854556fdc1c18b5734e1afa3b`  
		Last Modified: Sat, 13 Dec 2025 00:26:34 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bdc0c3271481da1285a572fe3224ea6cbffdfcf181838ad10740527817e1bb`  
		Last Modified: Sat, 13 Dec 2025 00:26:34 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:964974c4296282cbb9625c3c42e10169ece87c1a1eaecd8f427d3b6e8d069a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6938994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d1f808103edd31105c9cac97223495a2d12608436e0fef80832e1b5f4bb224`

```dockerfile
```

-	Layers:
	-	`sha256:0bb44fc3a439af071d2657b68efe78e0a511b8fe3552084cfcaec10b86737853`  
		Last Modified: Sat, 13 Dec 2025 01:54:05 GMT  
		Size: 672.1 KB (672104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dfd807b205c23cd41ebdbd09d5bb1704a7ba24fa1e7abecc29d0a4e6927cb91`  
		Last Modified: Sat, 13 Dec 2025 01:54:06 GMT  
		Size: 3.2 MB (3180710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e5601f27efe20c730aa631dc7d33b8e55db3f9546cc81b519c9210beabcaf4`  
		Last Modified: Sat, 13 Dec 2025 01:54:07 GMT  
		Size: 3.0 MB (3025810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b37f462208a2c7abf074990c2bb81c181ab74ba041e45b8bad1825a04040fb7`  
		Last Modified: Sat, 13 Dec 2025 01:54:07 GMT  
		Size: 60.4 KB (60370 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:5cade653123f5313dee5ee7099bff93ed318d042e0b2f2d4e9a6b18c67e599fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75965721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c416393a96e635de7e47b36cb0f2285d87a44c42ed8eb0554499df1ac175bd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 15 Nov 2025 12:40:37 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 15 Nov 2025 12:40:37 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 15 Nov 2025 12:40:37 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 15 Nov 2025 12:40:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 15 Nov 2025 12:40:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 12:40:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 15 Nov 2025 12:40:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 15 Nov 2025 12:40:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:20:39 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 03:20:48 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 03:20:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 03:20:48 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 18 Nov 2025 03:20:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:20:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 03:20:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e59a1c1b9f6e68d2e81dfe93f128277d090e8d42bb80d9fdce1bd0812253e90`  
		Last Modified: Sat, 15 Nov 2025 12:47:29 GMT  
		Size: 34.9 MB (34892992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b82b64d03f44428bb7c7c84bc38b196743066f1c2cd8073fa6e2958a1f2364`  
		Last Modified: Sat, 15 Nov 2025 12:47:25 GMT  
		Size: 10.9 MB (10906598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445ba2528747173700141a982a31baa29e2bb537c0faf37187397c5cef3d8ac0`  
		Last Modified: Sat, 15 Nov 2025 12:47:24 GMT  
		Size: 1.4 MB (1366487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ab85becded663592a6bc65df027d3b64784a81fde022e9ef0f2d593a067f8f`  
		Last Modified: Tue, 18 Nov 2025 04:39:50 GMT  
		Size: 25.3 MB (25282651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c6b0a6f4b731df4b2017078d1d133e2cbed722a0bca6e74485cc38e59b447f`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e1906d3f3c215386290a7ef260fba1c1a172ded9261e1333dfc67ea58d0473`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f065a8e08b979e6b746f95b8f4fc2e86e14d9b444bf9212b642e4e55b9c3833`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb79fb793b07ee339d044a1fe1e5e3f5dd9213f52951f7d84366dd805ae73a`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:53a741c41f73a58327d751bafcf55a28b79b7408e602d9b826fd9f6f51ee1896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6871306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d32d52fba2d8ab99a17f61818c0008cbbcbcdafc90b8bbf3ac6e77e9d741a28`

```dockerfile
```

-	Layers:
	-	`sha256:fb7d5bb6f27fb41df548cf4d7ef09809923c6f515cabc4e3e567caa3fece52a3`  
		Last Modified: Tue, 02 Dec 2025 13:53:12 GMT  
		Size: 672.1 KB (672069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75168eb38c6a68f809fa633e77bcb41800e6a43dea1d6ee64f55d172c5e13668`  
		Last Modified: Tue, 02 Dec 2025 13:53:13 GMT  
		Size: 3.1 MB (3146927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2027b801be77776683a9b2852cad0ef9eca1c10eb6c3ca44144143131ece7422`  
		Last Modified: Tue, 02 Dec 2025 13:53:15 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7daa45a745fec68dea6a2453843d531f45b9a9ae14a8cbfd65fb34d6d296349c`  
		Last Modified: Tue, 02 Dec 2025 13:53:16 GMT  
		Size: 60.3 KB (60271 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:380ace6bdd315123144f7390e353db4b8e14e3a8b45efb4ccd9468f1d7d38992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72793122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bac8dd75ba97a158edab634ec02d26730383a4005648caa6df83dab868ede87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Sat, 13 Dec 2025 00:26:10 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:26:10 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:26:10 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:26:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:26:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:26:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:26:12 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 13 Dec 2025 00:26:12 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:26:12 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:26:12 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:26:12 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:26:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:26:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:26:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:26:20 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:26:20 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:26:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:26:20 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:26:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:26:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:26:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2ebf37b8890dae37bf00c1a6380c714d7406e5f79a53a2e7036f42a95d607a`  
		Last Modified: Sat, 13 Dec 2025 00:26:59 GMT  
		Size: 33.9 MB (33919394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc9d9a216187bf506674a933774637a733643f442cbe2bd0c64eeb899d13283`  
		Last Modified: Sat, 13 Dec 2025 00:26:54 GMT  
		Size: 8.3 MB (8346905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0d036244e84d5bee9465e8babf6117ab4b2e1614dafaa0d3645f198182b981`  
		Last Modified: Sat, 13 Dec 2025 00:26:53 GMT  
		Size: 1.5 MB (1515835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f0e5701925016bcab49257fad16c31867cfa0c4eb4dcd50e9de0419ff5f92d`  
		Last Modified: Sat, 13 Dec 2025 00:26:56 GMT  
		Size: 25.3 MB (25285435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f28d714a1b43f28dff2dafe6e2e091bfd74ed70bd71c366833a51263d4a2e00`  
		Last Modified: Sat, 13 Dec 2025 00:26:53 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcc43777d88e04960e2e2ab07810d475fe3ac9c124e689f33b263c2c7281733`  
		Last Modified: Sat, 13 Dec 2025 00:26:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc258e2bf1789e1242b3f807dc20f0aa7cd0f8e4b4969c39d5e67e8b7358278`  
		Last Modified: Sat, 13 Dec 2025 00:26:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5501099178df14d4322b8225977f501418acc0192a20382485c062b6cf68e1ee`  
		Last Modified: Sat, 13 Dec 2025 00:26:53 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:862182e442a43cb01ac33a2cc557a98c94fdab0042d9ae6d58f3e7cb829ddb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6715376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1171e552e026e3ee8b6c9843a6b3b74d6cc7f333cc7a543d2396a79f386ef4c5`

```dockerfile
```

-	Layers:
	-	`sha256:751d61a64d0dd796d0f5eed612a82f86145e7b28d84af583ced0515f32eb92de`  
		Last Modified: Sat, 13 Dec 2025 01:54:16 GMT  
		Size: 672.1 KB (672070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c50e1645f90e0962bc8f14001a501c6978d117d63e2ad31541e08ecb252a6fb`  
		Last Modified: Sat, 13 Dec 2025 01:54:17 GMT  
		Size: 3.1 MB (3068934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5d1b278b3867dec7d1527467ad1d466cec1039ecaa11a1656136795b706566`  
		Last Modified: Sat, 13 Dec 2025 01:54:18 GMT  
		Size: 2.9 MB (2914064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0243063633a4a1df2bcb7c71ae502e690327cce20247ad87d857c9f3887f2a55`  
		Last Modified: Sat, 13 Dec 2025 01:54:18 GMT  
		Size: 60.3 KB (60308 bytes)  
		MIME: application/vnd.in-toto+json
