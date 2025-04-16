## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:a42ed932d3252077e83d4f03ac4d37e1b66889d18994210ae3394361fab0d72c
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

### `rabbitmq:management-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:f8029cd7883d7e3f27984f37283dd8b52c4dfb863a1961abfaabf9b3cfff7d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643b703347432ec1c26b87054e3bf19d1f04b186b730c8d55cf070160b1a5d3d`
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
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:62e8924d2374a0b301a9f3cefcc1c20c315ebf7e4499eec27aa2b55d4beb5152`  
		Last Modified: Tue, 15 Apr 2025 22:26:14 GMT  
		Size: 13.8 MB (13767377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e9d52facce26f7fb8c1bffb1773782165c7dc5d895be564d03dbb0ec35edf7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1644193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916bd621b9d8dbac90662ac487b57ec73db6a5b16354982e742eaa80c2dde901`

```dockerfile
```

-	Layers:
	-	`sha256:68a06547860c7b8e9a9837ad7f703c116b668660b3f50093dbc1d8be6aaf2ac3`  
		Last Modified: Tue, 15 Apr 2025 22:26:12 GMT  
		Size: 1.6 MB (1632970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b890cf405d59bff1747e7fe3fe0c02aa7aa5c76474c94e08fafdd285afa2e69d`  
		Last Modified: Tue, 15 Apr 2025 22:26:12 GMT  
		Size: 11.2 KB (11223 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:10e04ea9c516c6bdaf7b83c405d91e2e2973089c93e9b642bd12159c02911d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87974682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca83ee4cc2604c8d4000ece8d8864ae6b83a24751b3d3b443907497a5c01419`
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
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:e11ecbb2ab5a2c3a3c644b67a9da3e8bba5ebe565926f268f74cd0effdb0a314`  
		Last Modified: Tue, 15 Apr 2025 22:31:47 GMT  
		Size: 14.4 MB (14404561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bccfb21068144146a67ef8e208fd1c644e2f6db68da32b8ac5ec78135e159a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 KB (11084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daa7584ce334fa016b7aeae86b72dd27b0d5e0428ddb16325d12d747437e8a8`

```dockerfile
```

-	Layers:
	-	`sha256:09b3025b6b6cc33823476b690887a83080ed7db17b76461df26ad30945c7a80f`  
		Last Modified: Tue, 15 Apr 2025 22:31:46 GMT  
		Size: 11.1 KB (11084 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:9e52c609d907dd98980f5e73772789fe7c9e156ccd94f28311187e64b6205413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86841959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8ba9fa6bca956657d5ccba56d81c4aab87a7c4c572a2c0f614a2585ede9b13`
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
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:9a8a67f737a411885b74d1c4c1a27e61774bdae7e11d34769cfdf0b27b1af94b`  
		Last Modified: Tue, 15 Apr 2025 22:43:25 GMT  
		Size: 14.0 MB (14043901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3734ad05ed72dc94ab9c2e2d8228dc6dadaa6a7565e5faf6df0c217729fb2105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1645298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8552e0ae6242dae3687cc6aae7550bb7513d27e0ee5adff760e37f59abc641f4`

```dockerfile
```

-	Layers:
	-	`sha256:769181cb69a4e732c8891b3cc51733885efaadffb39fbaae229246e9e7d200ba`  
		Last Modified: Tue, 15 Apr 2025 22:43:24 GMT  
		Size: 1.6 MB (1633999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d14f5889ea46cd2f2dbb3c61741080f139851384e163f072e0c05607290bb1f1`  
		Last Modified: Tue, 15 Apr 2025 22:43:23 GMT  
		Size: 11.3 KB (11299 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:226a22bfd3bf7170e3ee13bdd8ec6efc32d47109b8a23f05ea74e661b9b9b171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98359012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a3d07528383d5e2d7d069a929b55e4a4b35cda41ee62265e650bbf3dfdfb10`
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
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:2e522603789059b07ed2b13781824001dfeaea764b1eae7f2a53f4712240f1d1`  
		Last Modified: Tue, 15 Apr 2025 22:32:08 GMT  
		Size: 13.7 MB (13725639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:19481d152ddba63a83e03eed44b6ccbf62d8ff8b65ebadbaedeafdacb423a9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1645174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2f2976d05f69f59b01e8ec712b461579a55dcbd613b3efa091bd571ff3765d`

```dockerfile
```

-	Layers:
	-	`sha256:a81ea6e3018171a9830b20145217d92900888c17958c28d4aab9c8526fb0e266`  
		Last Modified: Tue, 15 Apr 2025 22:32:08 GMT  
		Size: 1.6 MB (1633847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5c9618f81b2ea6f65baf925d15e01e03cbe68c2acde434243fc79e02bcf6b0`  
		Last Modified: Tue, 15 Apr 2025 22:32:08 GMT  
		Size: 11.3 KB (11327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:abbd870ce4d007b7c9ba49f3397f634f82191ceea4a8d39e98897f92402df637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90260015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bcafcc25bedea9a9c2c036266199307a3d374367e8a1588047b251f2803e64`
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
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:f18ddb656f85299e817f0be439944823896288fdc8ec55a3797c53e755099df9`  
		Last Modified: Tue, 15 Apr 2025 22:26:09 GMT  
		Size: 15.3 MB (15272458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4441c52c1c76d6c8c1129cf61e9d83f3b317e76623ac91e99a5c4f2e2c657dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1643964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f628203079bba65b360ea10390c70f55e8a1ac911d25c77511fe3ca0d3373582`

```dockerfile
```

-	Layers:
	-	`sha256:523cb5833136832b23193f496dac30f0f0962320a8f3786289af11f8fe5881c6`  
		Last Modified: Tue, 15 Apr 2025 22:26:09 GMT  
		Size: 1.6 MB (1632773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e36fd8e0c38663c691aaf53623173313bd7211a34133b0c7025796806953d56f`  
		Last Modified: Tue, 15 Apr 2025 22:26:09 GMT  
		Size: 11.2 KB (11191 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:e10d3299d384631b27859728c56517fad11d53a7cc798d8083aebf77f08c26cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91397047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b0c8db37306ee68a624b5f218db7126458c964648a8c6b8a9aa881556552bf`
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
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:d4840517647bba4504da67233656c33b78c3a0f9f0a6fcc43563fcfe009474cc`  
		Last Modified: Tue, 15 Apr 2025 22:39:45 GMT  
		Size: 15.3 MB (15275242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b95ed0afd41b8532aa174af6bdb8215b7f4a898fcc913e05f7f47ad7fc5b54ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1643485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9199b5ff0a5ff55feb8bd55da3ee01080cbb5332696189f432f5e7dd2978b660`

```dockerfile
```

-	Layers:
	-	`sha256:1994c092a6a3be595d64c92e12c4991e6539488c7a1e97f089a72a2341a0ecdf`  
		Last Modified: Tue, 15 Apr 2025 22:39:44 GMT  
		Size: 1.6 MB (1632218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036801ffdc0365c8cfe5895bbc72c34785700c12aad836977b055d631612c691`  
		Last Modified: Tue, 15 Apr 2025 22:39:43 GMT  
		Size: 11.3 KB (11267 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:fa1af069b364b2a204312c94b28209590e009ac4ec9a9ad84a82eb11ec16e6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92622496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836b1a0e6e71d702666b1babc3ef87b48cfaecccea45afe857976adec5e962af`
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
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:b8f8cc40fb00e5e79c9d2f07d0478807a1928e86895541678acf9ef7146255d2`  
		Last Modified: Tue, 15 Apr 2025 22:41:19 GMT  
		Size: 14.8 MB (14816822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bfb02f0463945c4bcc81f614d5c5abeaddac2b0ce3e2553bc23e9ebbc41140a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1644917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ca368fe4e49f86e7dc0def4dd3bdf931098ee2cdc0e7ee4e7b678ebac658e9`

```dockerfile
```

-	Layers:
	-	`sha256:71c10655d1b9919a530f8f9d871b54f308ba383a97cf91f12ca1b459253a03b5`  
		Last Modified: Tue, 15 Apr 2025 22:41:16 GMT  
		Size: 1.6 MB (1633650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e4cd97402a0581a17481cf60259d5a8178ba0c8748438576eaae76d1ce1bb8`  
		Last Modified: Tue, 15 Apr 2025 22:41:16 GMT  
		Size: 11.3 KB (11267 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:b7d3ddd6a9b6bd86d57d2b89dc5ffe75764f0f6fbf97f874e58345e16ffc8432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90002811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfd04d907c222c917637c8e6d4a645c1069199d3854fbd628dcbca7d1857d47`
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
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
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
	-	`sha256:9110c1ab23785ae8ae47008bb3dd2f8dc9f94765764c3d12fac4ff353a1a9114`  
		Last Modified: Tue, 15 Apr 2025 22:39:17 GMT  
		Size: 15.3 MB (15302818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a5a8a945df444b3208df50bc140d8be17cd4c84eb66172a86bc0e4c712eb6b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1642891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb8368b4a2bf483d80284862cb5823446e2fd3d0be214e015d1bff90e78f9dc`

```dockerfile
```

-	Layers:
	-	`sha256:24a72655b2be29c1c524861cee2221fb2de10282c49d8a7e8595a3d65b99407b`  
		Last Modified: Tue, 15 Apr 2025 22:39:17 GMT  
		Size: 1.6 MB (1631668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:126b55cd747cc3dfe02acd975ac9fdd3b51196ea7e871d2aff52d50586afb130`  
		Last Modified: Tue, 15 Apr 2025 22:39:16 GMT  
		Size: 11.2 KB (11223 bytes)  
		MIME: application/vnd.in-toto+json
