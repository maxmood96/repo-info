## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:fc69c2116e0b9098c43d7a12815aaa5e52b18de705d0d62d6b9a6e460ae4128f
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
$ docker pull rabbitmq@sha256:774d0ce64df1e00bf5de6636a4004c6dacdce2f0077b0e0ca0b468b25ccade9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85518292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d134640459acb804fbd7b7e18aeabfb38040c25e06ac1172571b3149e1e4164`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe41a4aae24f82f6cdf52642e269fa8068b441163ecd186354d18d8284f82f98`  
		Last Modified: Tue, 15 Apr 2025 22:08:27 GMT  
		Size: 42.8 MB (42831880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebc1de04519194f0489274b74b8a2645ecfb51d537fd7ca732da5d9d19608f4`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 8.3 MB (8311606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e9d8829c8807db6890c4055a48d84aa92f1f172e659e168a1f5e35f8c03a8f`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 2.3 MB (2279362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9793a9d323db581a4fb815ca7273560b568605940e856ce04dcf76cbbc6e1188`  
		Last Modified: Tue, 15 Apr 2025 22:08:27 GMT  
		Size: 28.5 MB (28451448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27276ceda95e01921cc21c86e607a624d123d42b79102ba979395183ff066aa7`  
		Last Modified: Tue, 15 Apr 2025 22:08:27 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8bc264db43db3bc7a63e4783f5935b72316a3031d54e8978925358586a7c4b`  
		Last Modified: Tue, 15 Apr 2025 22:08:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7fb1fb95559a6f62a70b72f308687d50069350b8a1d2b0dbd9d737c14c99fc`  
		Last Modified: Tue, 15 Apr 2025 22:08:28 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70d0c675c935822ad91598d4a978df9c6c0241cc93c5854c1ef7ccc7b7ad11`  
		Last Modified: Tue, 15 Apr 2025 22:08:28 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9f22b8bacc8ac80a3ccf3514ca2ae6260749bd0e00915b29d077787d0f4534f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6728950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d885865d00cfadd685801cbc1effcaad68cc463865473b20d56f4ac3639c55`

```dockerfile
```

-	Layers:
	-	`sha256:4ea4ec3b0f66c245e182d009f992ca23758dfc24440255e097aacdc59809dfe7`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 659.6 KB (659640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2e2d9e1336af29a05d02f866fcdd36d89af381d2c24f42317c2af9b7578c7b`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 3.1 MB (3081286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f8393cd873547e60533b8384f30c86e87a54453012ece9ea552a672746cdb1`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 2.9 MB (2928081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5d9728cd150f8d35bef157f22b938cba7918be59b8a8bb228e3be82cf35bef`  
		Last Modified: Tue, 15 Apr 2025 22:08:26 GMT  
		Size: 59.9 KB (59943 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:9f2cf2d02a2ed363819310f426c2ac1cde953090732f57d16c928a8953d66bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73570121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca91c6caf59ea1554c513490f02988ea389b5cfe5c10dc07cd6a64dbf1ea278c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fc7de5297f460eb8edbb34d2fa88470349312b717c45c18d4cccc10ef15f94`  
		Last Modified: Fri, 04 Apr 2025 17:30:56 GMT  
		Size: 33.4 MB (33427362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41b00ee5464b93d67fdf77837de86033b382261212c42a17526a10a5bbf3f0e`  
		Last Modified: Fri, 04 Apr 2025 17:30:56 GMT  
		Size: 7.1 MB (7097958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6196f0e9a4a2e32bae325452b9da3e6ef9f612848be7ccf84ab3446472ba0a8`  
		Last Modified: Fri, 04 Apr 2025 17:30:55 GMT  
		Size: 1.2 MB (1226979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18428ec9145ecd7b3eb943992500077e1eda91fe12b8be9e244f769295630d30`  
		Last Modified: Tue, 15 Apr 2025 22:02:35 GMT  
		Size: 28.5 MB (28451351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6c5c1249610c6aee634bcc37450fb7da0a1e5e4723f34bb96017833ef93a31`  
		Last Modified: Tue, 15 Apr 2025 22:02:34 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfc311ebee11219dd4b1b28548fe137a1a049c0f4d15dfbfccb054837195bdc`  
		Last Modified: Tue, 15 Apr 2025 22:02:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f28f152ae6af725b1ea76cde0968f32dc38d3871a112f1efb13e06f390cb4`  
		Last Modified: Tue, 15 Apr 2025 22:02:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd5c4f38e6af5fc255e5aebe6da2d1dd956be6d5c8c46adf9ed5afa5f7d1dd5`  
		Last Modified: Tue, 15 Apr 2025 22:02:35 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9f1617af1f4b2f4238218520dba7216a0e510e3e204a1444caa1e68d02569161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97754b474f821b73244d6b5912d55be59fdf9a8a143d5d7c35b3a610d663998`

```dockerfile
```

-	Layers:
	-	`sha256:23dfb9db143dc35bcba293d664e7e3bc62a2d4b3a91d3ef4a07aacaa3cb8e2d4`  
		Last Modified: Tue, 15 Apr 2025 22:02:34 GMT  
		Size: 59.9 KB (59920 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:4e3163a42305e46edefc9681c50d0404d687d5b0ffc685895a23c40b1f97ed75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72798058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b99a0b6e837c404824cdc2ec72cb06c5353bb36e4fe994e63a012cdfb27e39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180687ec158ecb9d2287088070115c5d94d14aea357ed2cb35ec5a1fd15a1a84`  
		Last Modified: Fri, 04 Apr 2025 17:35:53 GMT  
		Size: 33.4 MB (33370046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8497ebbbc56f64557a9607867ff3739a5e4a1df46ed0cf9df1c0f271463ad5ae`  
		Last Modified: Fri, 04 Apr 2025 17:35:52 GMT  
		Size: 6.7 MB (6742225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91faa9fbaa189690893c27b0422c385dd52ef1dfd84283d57cd33790ff76a365`  
		Last Modified: Fri, 04 Apr 2025 17:35:52 GMT  
		Size: 1.1 MB (1134773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18584e395cc91c03fd8014635110d4826dd46887a185834dbb01755864b99ae`  
		Last Modified: Tue, 15 Apr 2025 22:16:59 GMT  
		Size: 28.5 MB (28451148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69655e2a69bb2b1f4b64791e0c7ad8e25ea600076dd1d43aa4a52dbefa29b417`  
		Last Modified: Tue, 15 Apr 2025 22:16:58 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857b839416c4f2ad722f871f585abb42e47b8df127e7a009811328bf2964fc81`  
		Last Modified: Tue, 15 Apr 2025 22:16:58 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30e13223c62194b7a70b23d8068b6178fdec4e2105329af70f5e7add986ddce`  
		Last Modified: Tue, 15 Apr 2025 22:16:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85aacc9f6ab1a0ad847ebe49060a73bebb5e6e0c9616ad681a4efbb771c66ad`  
		Last Modified: Tue, 15 Apr 2025 22:16:59 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3f9193b6b5e2f65981a14db7a7a21a74d2a0a7099b5be6ae6fcf7a748bf08e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d56676d85e2ea45614ee88c0600d4b94f1ceec4896aae262d355ef3a870735`

```dockerfile
```

-	Layers:
	-	`sha256:20a004e77fd3722a7899752ed5c184ad13ed51e4148559b3dea55f1bf4d1c493`  
		Last Modified: Tue, 15 Apr 2025 22:16:58 GMT  
		Size: 655.8 KB (655785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3e42dffa526338e35be6f2ebcc3aba48995a4f76eab2dc7ce8831619f1c18d`  
		Last Modified: Tue, 15 Apr 2025 22:16:58 GMT  
		Size: 3.0 MB (2967140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13fbce94c3ac32e7c512e7d9a58c68c775476c9c4673ee050713700cad520a7a`  
		Last Modified: Tue, 15 Apr 2025 22:16:58 GMT  
		Size: 2.8 MB (2812610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939cd73aa6d076a85f5d168ffc295b5a9d6e1601122563755aa20e911eda0ec2`  
		Last Modified: Tue, 15 Apr 2025 22:16:58 GMT  
		Size: 60.1 KB (60136 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:350dbdb13f0cc82f449224e67c7ae20bdc0917e5499600dcf2c269276b77a3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84633373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abec99c0ec18834105980e6471155f1e88032a066f5286db9d71df2d0420dfb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c537f47f7bcc53c0caeabd81742dd023240f01e2016c548caf8f514027a3f9b`  
		Last Modified: Fri, 11 Apr 2025 23:44:24 GMT  
		Size: 40.8 MB (40828401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8d1d435fcd2d2c8403e1bf93b37f09e04a064bd1112b689c67ca308056ca74`  
		Last Modified: Fri, 11 Apr 2025 23:44:23 GMT  
		Size: 9.0 MB (9034861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f84000cc2bf3c11d836c512660669140dfb20cea51299a83861de750611e5`  
		Last Modified: Fri, 11 Apr 2025 23:44:23 GMT  
		Size: 2.3 MB (2323914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9dbdf85a6f6e7815770e33ebab03e50d81eade7cd788d396234277b421d459`  
		Last Modified: Tue, 15 Apr 2025 22:23:16 GMT  
		Size: 28.5 MB (28451420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3334fa401e27d67d96c572a99c6ea17133fe5f10ad9f0c7f911436031249163`  
		Last Modified: Tue, 15 Apr 2025 22:23:15 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691803cdae689f02128ec9695e9bdfd753e7087f3b68cfd1fd54f40c23ade687`  
		Last Modified: Tue, 15 Apr 2025 22:23:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e620bf38ecbda16a12f27a19484fb645f268b3fa83aa06704b299889f3cf4bf6`  
		Last Modified: Tue, 15 Apr 2025 22:23:15 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776bd577abcb9a90c2d286ecd6e67651296a356068949a3b8d3e40a3ba529c34`  
		Last Modified: Tue, 15 Apr 2025 22:23:16 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:60ca2e25abbd33ea706aef9121906be001ab15c8c536ae6499a2c643f2a0259d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78efdda600f96b1cd4625f3c3aa775eb9a4cc8daa448f7e5fd9208d9813ed517`

```dockerfile
```

-	Layers:
	-	`sha256:4467c6929132449437de9892f7497dc36f40404a3a31a634b06faa766a27866b`  
		Last Modified: Tue, 15 Apr 2025 22:23:15 GMT  
		Size: 660.4 KB (660431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c4264015c638787e925b47d16a7a8196c950acdb09fa8005ebb6795e14a1fd`  
		Last Modified: Tue, 15 Apr 2025 22:23:15 GMT  
		Size: 3.1 MB (3136095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27b28ef6fd9a170549eebdaea4a35b98b04bd61c580949d5794b28f0d17ecf6d`  
		Last Modified: Tue, 15 Apr 2025 22:23:15 GMT  
		Size: 3.0 MB (2981571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d09d2b257736d11dffc722b6d87e92684bfffe1eea9d0c032feedf51eb2f8ab`  
		Last Modified: Tue, 15 Apr 2025 22:23:15 GMT  
		Size: 60.2 KB (60182 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:86b7cbbc4da917de4b971084a969498d02f4676dc7fb0ebf9fa8cda91e9bc7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74987557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95702868912991ae7146a01f2ce9dbeaf98c9ff8022742bc2d5736698688390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9fbed4a5436da1d78bcd416ac65c9f57f9e2cf9c2a4f570db8ba040a6407e5`  
		Last Modified: Tue, 15 Apr 2025 22:07:30 GMT  
		Size: 33.5 MB (33515600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362820bbd81d51a1d6bbf79c33f53c17f46dad10ea6dba3380cdd0eb1b4703ba`  
		Last Modified: Tue, 15 Apr 2025 22:07:29 GMT  
		Size: 8.3 MB (8324841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917742fc4d94ed784245556e90a2ea3ee3a8afa79de07bbf2120468ab766c99a`  
		Last Modified: Tue, 15 Apr 2025 22:07:29 GMT  
		Size: 1.2 MB (1230630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601e732eb75dbcbd5406067638e9d9af29e6c5b69e29370a013da6dc329827ae`  
		Last Modified: Tue, 15 Apr 2025 22:07:30 GMT  
		Size: 28.5 MB (28451115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdc4b4d9768803b41872bb078fefa77ef9d82c6e0934f16f9bff0fbd6126480`  
		Last Modified: Tue, 15 Apr 2025 22:07:29 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e11143c046ea3a1902151ea7d76501cbf4f4e465baa3b2a3807671d81373d7`  
		Last Modified: Tue, 15 Apr 2025 22:07:30 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72686c079762d5496cc6ff9a30043bfffec4da532a396c8275f8c3496995c35`  
		Last Modified: Tue, 15 Apr 2025 22:07:30 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcef9aab61382afdac52de0e45feed67d45c421ff8054971f70a4b409fc1225`  
		Last Modified: Tue, 15 Apr 2025 22:07:31 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4f71d280cd5120554401863a1e5a5a0df5dd0bd198dbf571b98be41ba8c84304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786ddc26b8a29db9087b00b6daeb81acf58a99a856c156a1a3f5e70d27e2c6b3`

```dockerfile
```

-	Layers:
	-	`sha256:0876cb79119af6e2b5589913ab32294090b517e0015a23aeb5dcbc36e25da9e3`  
		Last Modified: Tue, 15 Apr 2025 22:07:29 GMT  
		Size: 655.0 KB (654989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c42aa1f6da90ffb2657779cee339504575309a010cabceaabbd002607d8bae`  
		Last Modified: Tue, 15 Apr 2025 22:07:29 GMT  
		Size: 3.1 MB (3070232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974e5743dfe4b5e13a16e582e699a158bfb49e85477901ebab3881638154770d`  
		Last Modified: Tue, 15 Apr 2025 22:07:29 GMT  
		Size: 2.9 MB (2917031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d4437c97e03b8db21ee5241cb2b5efd5ac365cb53f477d2ee35cae1c20d874`  
		Last Modified: Tue, 15 Apr 2025 22:07:29 GMT  
		Size: 59.9 KB (59893 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:9d114c7926e6e1e88f30392e242cd2d95ea6624747a6502084bb5f4baff9de1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76121805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeef8bb15dbd016d4ad3408ccdf9e62924fc95d5e1f06e1a6af52af3d18436c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba56643b135045f7aee8b7a22b6cd6fb39a4c8acd1ae6f4406c25f70c5f1e37b`  
		Last Modified: Fri, 11 Apr 2025 23:45:24 GMT  
		Size: 33.9 MB (33899840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b74af34c0b18b147f270503c139ea0dd5f8acacfdfafa57c8920e756e9311`  
		Last Modified: Fri, 11 Apr 2025 23:45:23 GMT  
		Size: 8.8 MB (8848295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4077528002c281b6c0be1f39ee7c02d85fd31a5d2bcb1a11b1546b895e007237`  
		Last Modified: Fri, 11 Apr 2025 23:45:23 GMT  
		Size: 1.3 MB (1346534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f1c60eae7f5675bccbeff493bf29e4f4ab2320ca32f080439507dd75dc8682`  
		Last Modified: Tue, 15 Apr 2025 22:16:06 GMT  
		Size: 28.5 MB (28451038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca465a727ecf0db63691c02d323e4858f84bc593f166aef9f844f960a4d725c0`  
		Last Modified: Tue, 15 Apr 2025 22:16:04 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46fc5aea7d5683b676acc8947ff922eb8ca21f00b307cf621addd730db2bcec`  
		Last Modified: Tue, 15 Apr 2025 22:16:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fceddb060ca0f27d3df487bcb107ad42a5488d1950d0d776b5bd30609a82a5`  
		Last Modified: Tue, 15 Apr 2025 22:16:04 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5021f56ee273cdea5c5e2cd7ea90fb9a43abe243d1fd46e40e8e3fd410a5f161`  
		Last Modified: Tue, 15 Apr 2025 22:16:05 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:db5368f29f5077ba7a21a5200a0631f809145075007eeab6e4ac15eb99b249d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6733949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec7c9debb8674c112f157b09e079a7549397d4c308a4a37ec2d6023bbda165c`

```dockerfile
```

-	Layers:
	-	`sha256:29c53a5a5cebd93d575315d18d802b4b4db592f2d00a90f8d20dc74c73138bf1`  
		Last Modified: Tue, 15 Apr 2025 22:16:04 GMT  
		Size: 653.8 KB (653832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38ef82d70495af4a77dd34c5bf4295ef75923e57f40f477c449fe79823476348`  
		Last Modified: Tue, 15 Apr 2025 22:16:05 GMT  
		Size: 3.1 MB (3087324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ca8bff0b46c0f1f407ef6a6bbc0ee07a319152fc083751e1c494be69c40aa6`  
		Last Modified: Tue, 15 Apr 2025 22:16:05 GMT  
		Size: 2.9 MB (2932788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0633ede931a42ed241434255fea382fddc5c42ece174f23931d5675e704ea2fe`  
		Last Modified: Tue, 15 Apr 2025 22:16:04 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:169736257059b7e591678b0d5dd442ce1920681988272cc487f688d12ebc34ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77805674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b165ff0725622ef2b8a93bb31a14025f169de217550e382600cae4a2e3d785b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8886d26542841afc2fd7344a23ab629abee86f99bf07c7ee3f47d014de361885`  
		Last Modified: Fri, 04 Apr 2025 20:00:13 GMT  
		Size: 34.9 MB (34875773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df45b7bcc69afd85ac4e88ea60a44663dce9bbfbf75ec31959b089c20e93cda1`  
		Last Modified: Fri, 04 Apr 2025 20:00:10 GMT  
		Size: 9.9 MB (9858933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3097f20b70883b87845ed897d900aec16949918e53ec654caaf91b8be2df99f1`  
		Last Modified: Fri, 04 Apr 2025 20:00:08 GMT  
		Size: 1.3 MB (1266419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fefab1a7f510356f20f80dd96fe704f5c499955fdf9421410f694e38c39f401`  
		Last Modified: Tue, 15 Apr 2025 22:15:45 GMT  
		Size: 28.5 MB (28451362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2226b47c2cae576e52345c7304a798e5704fbb17a4de01966f18570e11070635`  
		Last Modified: Tue, 15 Apr 2025 22:15:41 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647e807cce08418de21067d307a109855e0e910fa276bb67495c7e5170575587`  
		Last Modified: Tue, 15 Apr 2025 22:15:41 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4cc8f946cd028184b6ccbcf958120672ae8900c576250bb7c642c579514d10`  
		Last Modified: Tue, 15 Apr 2025 22:15:41 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25047ed621fa2562af26340809c2dd10d4f4ceb0dd59d99df13dc6c5748e713a`  
		Last Modified: Tue, 15 Apr 2025 22:15:42 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1a459414cd99e5c53bf7f38f8dd382daf6b874c00f5109b4c4cc2934df29c6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6812063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5be45d22b412c93f965d3571295e740800d5a1f33097264cc76b92e0116351`

```dockerfile
```

-	Layers:
	-	`sha256:3ef9fc1766ced4d87b69227f3e1ced61fe5aa0e5c9ca05500c2b534f956b81d5`  
		Last Modified: Tue, 15 Apr 2025 22:15:41 GMT  
		Size: 656.6 KB (656624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:084219182e40acdd4c580caaabd9f6ff4d6716022997bd4af7d4dc75b5383f01`  
		Last Modified: Tue, 15 Apr 2025 22:15:41 GMT  
		Size: 3.1 MB (3124979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1830b189bf9460436faef78d74d4b8947b354bd3351d3c48fe833807f8bb828`  
		Last Modified: Tue, 15 Apr 2025 22:15:41 GMT  
		Size: 3.0 MB (2970455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed89249bc398ffbd8db660a6412a473fa980a4e5bd1b6c580213d0875c9bc37`  
		Last Modified: Tue, 15 Apr 2025 22:15:41 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:27befd42c0dd7d86dfb223b0663827a0e71c984787426ccdf88e0519b351f2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74699993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e318a3fe1c99359819358e1a68b0ea6de8a84d2871eb5333fdfab148850caf4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3e7f6067fc1a3d3d2bda8f4122c972e45c09b2e028e96a56d5ddbb715b848d`  
		Last Modified: Fri, 11 Apr 2025 23:46:19 GMT  
		Size: 33.9 MB (33943904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeff32fa4eaf3d0d5fcaad2d7f19d69e3e91be5bbf478a3eef2da0065b505ac4`  
		Last Modified: Fri, 11 Apr 2025 23:46:18 GMT  
		Size: 7.5 MB (7510932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c1829a44d8e1bc5107a40881692f85084556cdd949623fed76314f050f543a`  
		Last Modified: Fri, 11 Apr 2025 23:46:18 GMT  
		Size: 1.3 MB (1324690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465d28b771afee683bb35a3e3f8e3c865584bb3cdc850a72129655d3d537c00`  
		Last Modified: Tue, 15 Apr 2025 22:16:13 GMT  
		Size: 28.5 MB (28451149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1222ec28f3e385df048ce18c5ec0eec07de019a6573a8d6c748f1d77d6ec7ff`  
		Last Modified: Tue, 15 Apr 2025 22:16:11 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01788975e224e1fbdd0da5405d98e7f32b46ac2a6ca29619ac8d5bf4f94c8aa8`  
		Last Modified: Tue, 15 Apr 2025 22:16:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d788a6e9824e4f0384a230261a5becc1b94f85cd247caaf72715df41fa386e`  
		Last Modified: Tue, 15 Apr 2025 22:16:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9abb6a6e5b5cc9b69f5ce4e74dd8f7842cf29648194bddb3e3a3fbe013240e`  
		Last Modified: Tue, 15 Apr 2025 22:16:12 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:48233c6f22bf42ae741a70b1af3d24d31945a0df3ab0fafbf28b166cc240be9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6513817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb7b77d1b19c9598399199912438efd77927d81a1c1982ea36dd52b06a75ee0`

```dockerfile
```

-	Layers:
	-	`sha256:8db4ca061b03674801a714b7cf94e7eeb4b9d778e3866f67bfb2bc57c23c8713`  
		Last Modified: Tue, 15 Apr 2025 22:16:11 GMT  
		Size: 653.8 KB (653798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4f64c49ef161170aaf07e7d6d9f956cae9337593cdb62a33120d8e0d0638a9`  
		Last Modified: Tue, 15 Apr 2025 22:16:11 GMT  
		Size: 3.0 MB (2977291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce37f04cad220525e06b3ea68ad3ec4ef2181f293b8fee0cea2ecba46d91203d`  
		Last Modified: Tue, 15 Apr 2025 22:16:11 GMT  
		Size: 2.8 MB (2822785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192baca818a9974e93cde533b4ff6e2cb554cc6bc3da7892748317e83db55815`  
		Last Modified: Tue, 15 Apr 2025 22:16:11 GMT  
		Size: 59.9 KB (59943 bytes)  
		MIME: application/vnd.in-toto+json
