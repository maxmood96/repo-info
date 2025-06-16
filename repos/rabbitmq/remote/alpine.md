## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:a6e65ed678b305fee8b6ee5db44752eb9d4bf530ad90d58a96e03199704f31e4
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
$ docker pull rabbitmq@sha256:586d64f82cccbfa60a484f17deff464a689cf052c2a9c2611b53479b9d39261e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85856782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ea9528b3371603733053f71067c725718ebcf7b4bdefa42eb963c38ab99711`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 11:56:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Jun 2025 11:56:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Jun 2025 11:56:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Jun 2025 11:56:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_VERSION=4.1.1
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Jun 2025 11:56:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 11:56:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Jun 2025 11:56:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Jun 2025 11:56:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Jun 2025 11:56:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Jun 2025 11:56:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Jun 2025 11:56:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7e829f213211a7b1884ca548a840fc5ff749fe2fcc90f05b69da5a8f10d0e6`  
		Last Modified: Mon, 16 Jun 2025 18:00:23 GMT  
		Size: 42.8 MB (42829525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab067ad82f7d1f8dc8635281e6c9bd91ed7c56d4df4749de5cc370c1e752a525`  
		Last Modified: Mon, 16 Jun 2025 18:00:21 GMT  
		Size: 8.3 MB (8310279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26015b150af005260c22337612935ad77e4effde74feaa652957e035e0e75e77`  
		Last Modified: Mon, 16 Jun 2025 18:00:20 GMT  
		Size: 2.4 MB (2374084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df64c834147b34e94a65c1e9f8e764d9ef41934d13c65b503fd7b7f7ff7f4686`  
		Last Modified: Mon, 16 Jun 2025 18:00:24 GMT  
		Size: 28.5 MB (28544297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3382e7fc181d1d97ec379e77e993d93004c8b1a90790a0b6d0974691da9fd37c`  
		Last Modified: Mon, 16 Jun 2025 18:00:19 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15031369a412c5304fb96c046df369c6d3ac05fd140567b726d4a06860f23a5c`  
		Last Modified: Mon, 16 Jun 2025 18:00:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52d4b3ef29a6878a2098e84deae317b62899e26db632a104560df436b541968`  
		Last Modified: Mon, 16 Jun 2025 18:00:19 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d137a1b19392cb654425972aa7412b2e20393150763fd872ff1e9ad799fd02`  
		Last Modified: Mon, 16 Jun 2025 18:00:20 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:48d8ba41fe17c7a4114ef7567bad4a831c1110f536b4d5b9abbde0664ce27e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6783063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e13cc4fc69ce80f3104a28ecfa55504c10c10f2e59fbda4c14945f9f48c6f53`

```dockerfile
```

-	Layers:
	-	`sha256:13220c65878f5ca1fe10d36d8931f350d7552fb0a32b5eed462111a4baad3847`  
		Last Modified: Mon, 16 Jun 2025 18:53:08 GMT  
		Size: 671.3 KB (671313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f020a7946858971c3a39cd8cbe98f9b5fc9abece9558216da56c70d54d96a214`  
		Last Modified: Mon, 16 Jun 2025 18:53:09 GMT  
		Size: 3.1 MB (3102656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b44cb886604efe178e250fac32b1e77f3ad06f6e0227ca8b961687c0979e2d0b`  
		Last Modified: Mon, 16 Jun 2025 18:53:10 GMT  
		Size: 2.9 MB (2949137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d648b7a9a30843c261313a8a2ef042602cbc7edc7654c430c81443ca08c13880`  
		Last Modified: Mon, 16 Jun 2025 18:53:11 GMT  
		Size: 60.0 KB (59957 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:88cb16f7f940fd97a90e7baf80e726f083b098e27b2191787dfac2bf1f8c962d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73918587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befb97d7542082d8aa783da0a4b0d9d42b54d2af7d85b3d83168a1992be62ed5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 11:56:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Jun 2025 11:56:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Jun 2025 11:56:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Jun 2025 11:56:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_VERSION=4.1.1
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Jun 2025 11:56:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 11:56:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Jun 2025 11:56:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Jun 2025 11:56:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Jun 2025 11:56:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Jun 2025 11:56:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Jun 2025 11:56:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876af733809b4b7ede8aa9c7e716044c26019d91d0c4036f437b07fea7cf5de5`  
		Last Modified: Mon, 16 Jun 2025 18:03:33 GMT  
		Size: 33.4 MB (33444174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ae9e78e128405d186d5fbc7d7c3655e53c03d83299657efce6a8444f39aa9`  
		Last Modified: Mon, 16 Jun 2025 18:03:30 GMT  
		Size: 7.1 MB (7097647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3534ef3279bf0175340b6b7f57adfff23491eedac8a285cd63427a8937a0ad`  
		Last Modified: Mon, 16 Jun 2025 18:03:29 GMT  
		Size: 1.3 MB (1329816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425fd0812912b95126cdf8614a63713407f7463cdb3ee9cec63f736af1669bb6`  
		Last Modified: Mon, 16 Jun 2025 18:03:32 GMT  
		Size: 28.5 MB (28544270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b1853ad70f0fed8fdfd18a744c03b6400fe009cb77cde9fb8bb567db9429fc`  
		Last Modified: Mon, 16 Jun 2025 18:03:28 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0104b0dc979190c3c60a1e7451c471a5c57fbd203ad332c7c8be14f5275ce6e7`  
		Last Modified: Mon, 16 Jun 2025 18:03:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72756d391dd25ffd29fc840e0e317ee7c0dca56734176be81c3038eb52be5758`  
		Last Modified: Mon, 16 Jun 2025 18:03:28 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5735aa142fede2aaa5ea5ca9ca50dfc97cec6ee2a9fa4ccd48082233f4a92fb4`  
		Last Modified: Mon, 16 Jun 2025 18:03:29 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:842602719cd7e0297315f35e9229bf02853fe02b13b2cf0fa1d4cb24c451de4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83571b5d0bab56776f98222aed0b70413aa984f46a44c48d72c2ee6e0a239e8`

```dockerfile
```

-	Layers:
	-	`sha256:0ebe83f1a6a24993b901330aac14e92ea26557f86d7b11ee4f609f050e6ae195`  
		Last Modified: Mon, 16 Jun 2025 18:53:16 GMT  
		Size: 59.9 KB (59935 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:f8465fddd37d8f9510210e0e9fa3defbe2c3641819e9da76f59287d684ab4e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73103681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701706941594738120e8cc156e84e8201fc9e9a553c184dab56c1588eb51cc9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 22:26:55 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 04 Jun 2025 22:26:55 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 04 Jun 2025 22:26:55 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_VERSION=4.1.1
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 22:26:55 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 04 Jun 2025 22:26:55 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 04 Jun 2025 22:26:55 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Jun 2025 22:26:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 04 Jun 2025 22:26:55 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba27b9b4cd61787cde4d4df02271453cc41363ff22ac920f5de173e0636a3435`  
		Last Modified: Wed, 04 Jun 2025 04:52:32 GMT  
		Size: 33.4 MB (33371081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828eefcd7d47842d3056a471f9e83b0b747aae8a65c1e86b6924a45776bdab9e`  
		Last Modified: Wed, 04 Jun 2025 04:52:34 GMT  
		Size: 6.7 MB (6741803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9970cf767a4f89b0edfeee5692ac5aa9e2afb8204289ca8dc155cfa22e2e4b`  
		Last Modified: Wed, 04 Jun 2025 04:52:36 GMT  
		Size: 1.2 MB (1226721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4e673f2f5c8b2b883f52ce5b55a76e9af871c55a6f119e97083a8e8f837710`  
		Last Modified: Wed, 04 Jun 2025 23:51:12 GMT  
		Size: 28.5 MB (28543152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6249552e672dd39cdda217bddf07c6013687ef1d7b42f24965c7a6c81d6afd5b`  
		Last Modified: Wed, 04 Jun 2025 23:51:11 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf4a77c05b7159c49ee4c86c0c5ae2c436d09be16062d8d85d35e2dfe1cf3fc`  
		Last Modified: Wed, 04 Jun 2025 23:51:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d505a65497196995cd510069fb403e908d84743b72686b119682d1b1f84a619e`  
		Last Modified: Wed, 04 Jun 2025 23:51:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6c08da77338f1a7bc89a3a63ec1c2e755038347eb119138e0f35cf35458414`  
		Last Modified: Wed, 04 Jun 2025 23:51:12 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ccc4cc3cce16b446d46410d22395df4ecd862bcd325037d1779eeb176af253c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6546992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3aadc31ad918e47251bde8764d21a435e81a1242cea3bec1f6e8320e81fba7`

```dockerfile
```

-	Layers:
	-	`sha256:3d53cbdf6ef324e999d778dc7cdd3b9cd10add57d4c48ec3bd5228695f87c028`  
		Last Modified: Thu, 05 Jun 2025 00:53:32 GMT  
		Size: 667.1 KB (667064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d493c9342de2726d76ff2b3e6091febd4d3296fff8139afb544d6a5e29a7a082`  
		Last Modified: Thu, 05 Jun 2025 00:53:33 GMT  
		Size: 3.0 MB (2987161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7f2746edbdeece76bc8b759aeb4acb44603c5e9c04471a533e88ed24ce2cce`  
		Last Modified: Thu, 05 Jun 2025 00:53:34 GMT  
		Size: 2.8 MB (2832631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e9d4a88f6cfe69776d8f0ea89b3470d8f02a39e119ce425f4aaabc46fe1500f`  
		Last Modified: Thu, 05 Jun 2025 00:53:35 GMT  
		Size: 60.1 KB (60136 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:176bb0f7067756dbc5c4e861a5547206e45c6988da3df2a8909956854b1a2529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84978542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e034d250a0f2b381912aabef601f06c7bcb69251c6a2bbb8bcf632c62692e2d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 22:26:55 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 04 Jun 2025 22:26:55 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 04 Jun 2025 22:26:55 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_VERSION=4.1.1
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 22:26:55 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 04 Jun 2025 22:26:55 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 04 Jun 2025 22:26:55 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Jun 2025 22:26:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 04 Jun 2025 22:26:55 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d60a9011688cd068a5fea25b636fbbaa2c310d3d35b1a3183a7532c40947c`  
		Last Modified: Tue, 03 Jun 2025 13:33:21 GMT  
		Size: 40.8 MB (40837400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae47ecbebe83d112b298ecc5a767bb964ceccdd480eaae1d08b685cbbd4e55d`  
		Last Modified: Tue, 03 Jun 2025 13:33:17 GMT  
		Size: 9.0 MB (9034725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a28bd7237c13da1dc2633eea48417351df16198215f935579952d0c62c3d440`  
		Last Modified: Tue, 03 Jun 2025 13:33:17 GMT  
		Size: 2.4 MB (2424772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55b0a8461454e00f1390a141d0b3208625af7b989e89ad7861a8140748a275e`  
		Last Modified: Thu, 05 Jun 2025 01:04:39 GMT  
		Size: 28.5 MB (28543961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0783a7a5b216c11d8be84d2f6b92ae4e71ac60c7930affe41c2f712f930017e4`  
		Last Modified: Wed, 04 Jun 2025 23:56:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fded85d1b00b70984c7a97412b0fb6ebc0432f9a25dbc541d4e01e8ef8333bb`  
		Last Modified: Wed, 04 Jun 2025 23:56:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0527b1bcb9ed936bf0a775c0c4800bfadcbf45fff62f528875db7557110bec`  
		Last Modified: Wed, 04 Jun 2025 23:56:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdba9f2fad9377fdc3332060ede1eed97ea8752c479132b3ffaf1e2007f0251`  
		Last Modified: Wed, 04 Jun 2025 23:56:16 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e05d2a5fc99291c8a419ab92741d0fe60869e986bd9999554933dc2a8bb3664c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6890994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0470ba9ca59a730ea62c27951ea4c0c9812cf68d3083febb3de4c6c4644267`

```dockerfile
```

-	Layers:
	-	`sha256:6eddc3bdeaa369b9d9e1d3a047707d1201e1e2c85c5295e7e6ba5b01ce71aa4d`  
		Last Modified: Thu, 05 Jun 2025 00:53:40 GMT  
		Size: 672.1 KB (672064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f53f30c62638fbaf2a9e1c0e287f897ef76880ac11b86f6f8db6ef2e626af10`  
		Last Modified: Thu, 05 Jun 2025 00:53:41 GMT  
		Size: 3.2 MB (3156636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26003ba368a8c5d9f09a27a75cc528434e4d7159b5cfe87078f7ca6fa66a3de0`  
		Last Modified: Thu, 05 Jun 2025 00:53:42 GMT  
		Size: 3.0 MB (3002112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef5d2fa3413b5e41ceffa665d676929972aaf54418a7b5b76d41e3de16f15d2`  
		Last Modified: Thu, 05 Jun 2025 00:53:43 GMT  
		Size: 60.2 KB (60182 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:864bc37ae61e9cf6eef1c9f44fd9aff5a2c19a531675ec2244d55aa987b23ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75343169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd662be0e72de3e58fed4d73e9b3c9455bb37460f5ce1f4fe70b0250f9fc665`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 11:56:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Jun 2025 11:56:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Jun 2025 11:56:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Jun 2025 11:56:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_VERSION=4.1.1
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Jun 2025 11:56:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Jun 2025 11:56:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 11:56:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Jun 2025 11:56:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Jun 2025 11:56:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Jun 2025 11:56:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 11:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Jun 2025 11:56:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Jun 2025 11:56:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742310320a2a7e9b363e98298d6370b555d90b178ed211aa875e087599610e23`  
		Last Modified: Mon, 16 Jun 2025 17:59:40 GMT  
		Size: 33.5 MB (33526017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158b766114c97f4a24d8616b9f0274d73de641f79eef2e5be04488ea469385e`  
		Last Modified: Mon, 16 Jun 2025 17:59:38 GMT  
		Size: 8.3 MB (8323733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735ae066c255ae4fa3d31aafeb3631a7fedab0bc4107aac947cf5e694cd09b83`  
		Last Modified: Mon, 16 Jun 2025 17:59:37 GMT  
		Size: 1.3 MB (1332257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5577afacf0216fb3b5cc6f14ab382b1bc9730098848ed5ca1a1532b70645e7e5`  
		Last Modified: Mon, 16 Jun 2025 17:59:40 GMT  
		Size: 28.5 MB (28543384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc90018be7939670bc8076d5d582e85684ee98d9287c604d6ee843df83df6b8`  
		Last Modified: Mon, 16 Jun 2025 17:59:38 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e71edbf304f38009aefd152914683ed6ed4eef435126a4467fa6f8516c4f6c`  
		Last Modified: Mon, 16 Jun 2025 17:59:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12743fbea1722bb6e37ba8a8fe1cfcbebf0725a18bf0ef21fafa1570c001c8fd`  
		Last Modified: Mon, 16 Jun 2025 17:59:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf05871a708f90efd828405eb2a0f753fa70618c7204f5d4be58005aff36330c`  
		Last Modified: Mon, 16 Jun 2025 17:59:38 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c5fce8bd6423a37c7fc68f6cb782ce5dc6cc7d385bf35255231b4e7ec9082e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6755904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cce8abdc128981cd72fe3d7930a55ce0514a5838d7a0b827df4b5e5cc4f68cb`

```dockerfile
```

-	Layers:
	-	`sha256:c5f1eb40dca21b81ca9daacce23bacee85508010b4cd71eb820586caae18e54f`  
		Last Modified: Mon, 16 Jun 2025 18:53:28 GMT  
		Size: 666.3 KB (666308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd212baf8c810c25bfb0796b5e8adc313330d869a757454c84a16a5f59cc4bd`  
		Last Modified: Mon, 16 Jun 2025 18:53:29 GMT  
		Size: 3.1 MB (3091602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0459dfecd68ddd337bf2021cee65bb36fc9b04ffee0743205bf0bf2778852ec9`  
		Last Modified: Mon, 16 Jun 2025 18:53:30 GMT  
		Size: 2.9 MB (2938087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5681739ce6c94efa0dc9dea5ccc981cb7de0ecea8c357131050f3efc606dadbe`  
		Last Modified: Mon, 16 Jun 2025 18:53:31 GMT  
		Size: 59.9 KB (59907 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:fde507ac66a1aec3d277d61488526e1fafba6234d2c9741d93406916267c0065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76480089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f510a49f060803bad271ffce8af41e2a8560fa8cb08f2c5274822ae17ad1f18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 22:26:55 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 04 Jun 2025 22:26:55 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 04 Jun 2025 22:26:55 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_VERSION=4.1.1
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 22:26:55 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 04 Jun 2025 22:26:55 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 04 Jun 2025 22:26:55 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Jun 2025 22:26:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 04 Jun 2025 22:26:55 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ce5cd0945ec9bc6d6dcc37316d484ddab8738ae9a491b784641f02e7b88f03`  
		Last Modified: Wed, 04 Jun 2025 04:53:44 GMT  
		Size: 33.9 MB (33904447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f464a31f3707827b3c1ebeb4139bb4efd58161007f0747c6c60ad5b7460522`  
		Last Modified: Wed, 04 Jun 2025 04:53:48 GMT  
		Size: 8.8 MB (8848198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c370cce58c9f10ab3d2a51b4718abaa836754d127b25fc6b0e50cb394158b7`  
		Last Modified: Wed, 04 Jun 2025 04:53:49 GMT  
		Size: 1.5 MB (1452384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7e48e83e222a61a59a0c5a12f29295c4cce1e5f87b5fb4fa42efd29592e866`  
		Last Modified: Thu, 05 Jun 2025 01:05:20 GMT  
		Size: 28.5 MB (28543127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56814dda61d353b0465ac40c76a6789bfe3c42cbe09a9505ba9273286af11309`  
		Last Modified: Thu, 05 Jun 2025 00:15:32 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6b180b486853c63b066f726cf0f3278f9772ec26e4d62eda22561471e8401a`  
		Last Modified: Thu, 05 Jun 2025 00:15:34 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1520d54a1150154b1c65c2147deb359002c60fbca9e62d62125c38dc6b00eb66`  
		Last Modified: Thu, 05 Jun 2025 00:15:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dd1fe9edf7620d62770308d61add8b5a18cb0a5b655bd75f07fe0ac6edbbdb`  
		Last Modified: Thu, 05 Jun 2025 00:15:41 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1dc801eb0931d5f15f87a9036f4e7465ef548f58facf04ac832ca33c9a942996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edca2e91e13908e6889e8d6adb855e5f6fa463d1e86870f66eb7c21363292772`

```dockerfile
```

-	Layers:
	-	`sha256:9b368f38849861bdc8b75e6948333ac659262285330c21fcef17efd47741344e`  
		Last Modified: Thu, 05 Jun 2025 00:53:54 GMT  
		Size: 665.1 KB (665111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c53e7e22380ae8d045a6761fec82f735df2c111ce5ae7cf01329e92e164f0ce3`  
		Last Modified: Thu, 05 Jun 2025 00:53:55 GMT  
		Size: 3.1 MB (3108390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:836c4cff389b225a2aaf26ff7cf3065dda3a0e8ae5bd0a1ba17fd3132ab1697d`  
		Last Modified: Thu, 05 Jun 2025 00:53:56 GMT  
		Size: 3.0 MB (2953854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a05ea6df3f493ee3a283471b605ada525859cc248ae98e00b7a44ae47881b3f5`  
		Last Modified: Thu, 05 Jun 2025 00:53:57 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:5bc3e4add3b31c8689de100836280590fb50f7cdd1d890bf77b1e2549c271e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78162679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173575575d278d314eea004c5538c69d017544e64934a3e227e00144a9e7dd9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 22:26:55 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 04 Jun 2025 22:26:55 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 04 Jun 2025 22:26:55 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_VERSION=4.1.1
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 22:26:55 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 04 Jun 2025 22:26:55 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 04 Jun 2025 22:26:55 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Jun 2025 22:26:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 04 Jun 2025 22:26:55 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e445cab456a357f47bf72921d5853af6edff7331df30d31b03dc47b3a8f155`  
		Last Modified: Wed, 04 Jun 2025 04:54:14 GMT  
		Size: 34.9 MB (34877986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e76ef5f8c1d9d94d546e859e592bb988d9279308e8005505e532993fe5fded`  
		Last Modified: Wed, 04 Jun 2025 04:54:17 GMT  
		Size: 9.9 MB (9859189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c633ad75f192273c24c74487372585add235f96c7ae2d9509210536bb643501`  
		Last Modified: Wed, 04 Jun 2025 04:54:19 GMT  
		Size: 1.4 MB (1366241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2397caf0a907660a72e21ebf62c6c99aa4fd7da813069dc43aa27054a71fb8a`  
		Last Modified: Thu, 05 Jun 2025 02:16:59 GMT  
		Size: 28.5 MB (28543700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25387249545db3de67a7a556506a3b842a6b54188f789ce6565eb74867e477d1`  
		Last Modified: Thu, 05 Jun 2025 02:16:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2bde3574fec0b8752b993231d38698e110537829796fefe833c9e599aae48e`  
		Last Modified: Thu, 05 Jun 2025 02:16:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bede1a1866971bba960f8a4ec135f78506083fb784707e461a4bb0393991a82`  
		Last Modified: Thu, 05 Jun 2025 02:16:59 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c079300d4f2047869b3655ad90ccdfc133d54f1d470ec673e11e20bcbab309`  
		Last Modified: Thu, 05 Jun 2025 02:17:00 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e83b0cc1fb2550c4c551a6f44f77a2e51906eba30e7d4afa93af8d79a2492466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6866687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1adabb0cdc7eca24662cfa9210348523a671a7e331434bb39b6ff91a207eda4b`

```dockerfile
```

-	Layers:
	-	`sha256:ef80cb6cdf1e83203472195bbe9a05426ee47ab0a3b8d998cb945053cf948ee3`  
		Last Modified: Thu, 05 Jun 2025 03:53:04 GMT  
		Size: 668.1 KB (668080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07491413de51fed159518aea2dfcd9c9b90ee24edd77a9ec84b84175ea4aeefc`  
		Last Modified: Thu, 05 Jun 2025 03:53:05 GMT  
		Size: 3.1 MB (3146563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2230f0d9a9dd4f3b3a8309a52d3c9a19395c68a5c66c3aa9f4505d6f5e823e2`  
		Last Modified: Thu, 05 Jun 2025 03:53:06 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6f51a98df860dae0f08025aad446623f38581ce51f8e75c91b86468fd63782`  
		Last Modified: Thu, 05 Jun 2025 03:53:06 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:5abceb176493b2af6f865b339ed570de9f363202ffc9cd1fd18d920e05c760a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34780178e3e3bcd218fb9f607766a7407d18fcad3ef7e604888d86892298c5f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 22:26:55 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 04 Jun 2025 22:26:55 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 04 Jun 2025 22:26:55 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_VERSION=4.1.1
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 04 Jun 2025 22:26:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 22:26:55 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 04 Jun 2025 22:26:55 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 04 Jun 2025 22:26:55 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 04 Jun 2025 22:26:55 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Jun 2025 22:26:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Jun 2025 22:26:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 04 Jun 2025 22:26:55 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dd82321da03835add2b52fca2e4bdbb18d6c494705a3b09f7c8efadacdafdd`  
		Last Modified: Wed, 04 Jun 2025 04:54:45 GMT  
		Size: 33.9 MB (33945280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a600a9f64924e8900d4f8cd75bf16ee7b3c3d84f5ad061190f4362c1cdf648`  
		Last Modified: Wed, 04 Jun 2025 04:54:47 GMT  
		Size: 7.5 MB (7510987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6c2623a2add85ae0c10acd019a3009f8ed74bbfd24cb4fc52d44c11b70b5ba`  
		Last Modified: Wed, 04 Jun 2025 04:54:50 GMT  
		Size: 1.4 MB (1430442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3732b61919cdfacfc310ede1f569e00d3ec5e628bb333d5eec5ac8d2cc1da94a`  
		Last Modified: Thu, 05 Jun 2025 01:05:58 GMT  
		Size: 28.5 MB (28543163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef4506e9b0eae1d8780b2a9da5f077e2748c71132b0c45a46cd32c0f36d9274`  
		Last Modified: Thu, 05 Jun 2025 00:10:34 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fded85d1b00b70984c7a97412b0fb6ebc0432f9a25dbc541d4e01e8ef8333bb`  
		Last Modified: Wed, 04 Jun 2025 23:56:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f48bde20b32b7cc2794d8a8affcc4bd62e69858c502d70324d3aae995d70eb`  
		Last Modified: Thu, 05 Jun 2025 00:10:41 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbd374af1e46229dc369161a262b5dd49d6a65a819b65c774ec53f59b3006b5`  
		Last Modified: Thu, 05 Jun 2025 00:10:43 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f8ff012287947ef00035a4c1581c4f479ea3494525d7c6c40eb71733f839d800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6566168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b11edce66600bb060d4d1c1f6e0fd8e2f6525abf7e59142c3a7843142156cda`

```dockerfile
```

-	Layers:
	-	`sha256:60a84846268bfdd8b6d2a13ff6f731bf350f6d40101e96850dc2b3beb0a1f816`  
		Last Modified: Thu, 05 Jun 2025 00:54:05 GMT  
		Size: 665.1 KB (665077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ede395ffc95d42233250df6b4e8fc4701b6e0a7e97dabc9a83446683f19def`  
		Last Modified: Thu, 05 Jun 2025 00:54:06 GMT  
		Size: 3.0 MB (2997827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf879d98cc0715409749ea59904e1140e9cf8a898112251ddc9dc825527452a`  
		Last Modified: Thu, 05 Jun 2025 00:54:08 GMT  
		Size: 2.8 MB (2843321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b3ff9cad6c68560bb4c26c008afa15517bdd185e1a88544e873c4c96244dd9`  
		Last Modified: Thu, 05 Jun 2025 00:54:08 GMT  
		Size: 59.9 KB (59943 bytes)  
		MIME: application/vnd.in-toto+json
