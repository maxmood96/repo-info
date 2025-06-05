## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:f34d3d1679a2a2d4e96774ccf778bfc4ca50dd3b83b552842297d2537ffbb7a4
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
$ docker pull rabbitmq@sha256:251ac3e2be5ae792ff35cf39bdc9e6dc55c53d3dde4db45f0f15b2a32e61b4c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85861576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0857aeefab09970996bcfe8e79715b7dbdf4ffb53e68d2f89b6ab986e589a778`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a8225a3113a9c8ae9acb4428c5749728cc96c540e367e6080c4ec90feff503`  
		Last Modified: Wed, 04 Jun 2025 23:53:36 GMT  
		Size: 42.8 MB (42834655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2d75197e85412756888ebeecb2be3b76426fdb8fa7a32831c780e357ae4519`  
		Last Modified: Wed, 04 Jun 2025 23:53:35 GMT  
		Size: 8.3 MB (8310296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714ab35dff1b376bb713e50213fec2b128494b6b94d0c4ebf10383cc0de5834`  
		Last Modified: Wed, 04 Jun 2025 23:53:35 GMT  
		Size: 2.4 MB (2374051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302d2ef3fb8e88e6a53f17423aae8e3eb43b44ac2d683ea3e2d8cc3a6abe8db8`  
		Last Modified: Wed, 04 Jun 2025 23:53:37 GMT  
		Size: 28.5 MB (28543981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef749ef0178f7aafe84f0e347d55fae57bce7a9792020ea8efc90fe4754f7d4d`  
		Last Modified: Wed, 04 Jun 2025 23:53:35 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bbe3eab0554802f8584c7eb5eff007e2caf0797a978741e90041b4c706d35c`  
		Last Modified: Wed, 04 Jun 2025 23:53:37 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629164f52e839597d566db2c9187bac6d53b04808437e731b16d2b46065a9dda`  
		Last Modified: Wed, 04 Jun 2025 23:53:37 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a63655904888f9d73978e8327b36be4f8fa5efadecf60800cf3f8baf25660d1`  
		Last Modified: Wed, 04 Jun 2025 23:53:37 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9ea810219f03bb202a18760770ec5f3f095d4d779612a729435dcbc325d35f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6782695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892744dddcbfc8571323652d28b1d2cb26f2a095ca7ea2cd989125fb92f68a96`

```dockerfile
```

-	Layers:
	-	`sha256:069a2789e0b676874ef69593b7cb6e2b58e70719ef70fd0b4bf1f021e2672574`  
		Last Modified: Thu, 05 Jun 2025 00:53:21 GMT  
		Size: 671.3 KB (671273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a041ffba5842c6c5f53dab9918eac338559ae98a833610529ec8b5c02005f44b`  
		Last Modified: Thu, 05 Jun 2025 00:53:22 GMT  
		Size: 3.1 MB (3102342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:322ccb63767aec65f31ef6300bec4bc2a76dd6567a5e1a93548f453cda0a8bb0`  
		Last Modified: Thu, 05 Jun 2025 00:53:23 GMT  
		Size: 2.9 MB (2949137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd879023c63021b27be38de73d059cd870f7421a3124aba4efd4c97ed81ec50`  
		Last Modified: Thu, 05 Jun 2025 00:53:24 GMT  
		Size: 59.9 KB (59943 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:c090632f2dc5d285c2b5dde75fc9ff7c579c84e6e433e0df03a105a911cbad82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73905048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1365179acd242b0cd1b462d1bd3b44ebd0346388ba6a98f1fc2e232fe63be555`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebcfac75050602e92454001fbf145470545c5722b9fae517a25ed47bb209f34`  
		Last Modified: Wed, 04 Jun 2025 04:29:28 GMT  
		Size: 33.4 MB (33430937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbc66eb96de3604ff839ed1b78334188e21afd480379a8b8acbd74251da8d23`  
		Last Modified: Wed, 04 Jun 2025 04:52:05 GMT  
		Size: 7.1 MB (7097607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1889d643e0de7cae489ff404c87694e660ce7e764250f3abf9f51917890a31`  
		Last Modified: Wed, 04 Jun 2025 04:52:07 GMT  
		Size: 1.3 MB (1329813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46165d33f77a1f148e2156ecdd223429c41a333915ce1e718514057ff9d471a9`  
		Last Modified: Wed, 04 Jun 2025 23:45:28 GMT  
		Size: 28.5 MB (28544018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eced545f8378235cd47c1e1224cd8b7b8e4d08cd7d8dd023224c5cc40011bb8`  
		Last Modified: Wed, 04 Jun 2025 23:45:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3e014b244bb51fb042549dbc4f54ef9ec2dd90cb957885682dd3bc8e064e3`  
		Last Modified: Wed, 04 Jun 2025 23:45:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57daca55658fb6a856eb89c55f8824a44dda5c481e1ab1fe0d534a19e1141d8b`  
		Last Modified: Wed, 04 Jun 2025 23:45:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfb3ed3238066b68922e354797972bdb1f6fcad713453a9434b8c9137c67c15`  
		Last Modified: Wed, 04 Jun 2025 23:45:27 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d54c768075b152017497fcdc1998569925b1f5bcac9ae0b3999f9d726a3944af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3c3089bdb880f25b7dc4409014d193752f3ac49ed692c8a5f8d13d9e912b88`

```dockerfile
```

-	Layers:
	-	`sha256:06576fe1a5527d071d7c3df1ed60766df7fbb66155416321f7dbd0e7ea694eff`  
		Last Modified: Thu, 05 Jun 2025 00:53:28 GMT  
		Size: 59.9 KB (59921 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

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

### `rabbitmq:4-alpine` - unknown; unknown

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

### `rabbitmq:4-alpine` - linux; arm64 variant v8

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

### `rabbitmq:4-alpine` - unknown; unknown

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

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:77baabede728ab8736538c5f5a6bf5d8a942d6fc4499149f75f8c413e8c61444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75334600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88efbb609a98cce04c0c8f639c7900235dc0dc87dc948bbb16aee3a865cc4dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54ac3aae85b2c1708f3b516ded327a5d48825ac8196bcd429372f4890ea83a3`  
		Last Modified: Wed, 04 Jun 2025 23:53:26 GMT  
		Size: 33.5 MB (33517671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d0550a72c280dceefbc78b37ac96a95315a5e8ec5174895ac460554e16686e`  
		Last Modified: Wed, 04 Jun 2025 23:53:26 GMT  
		Size: 8.3 MB (8323716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77185cf3f0f3a704b435e2591dcf2334f4eab5a8d4b956aefdae05c059c79d6c`  
		Last Modified: Wed, 04 Jun 2025 23:53:25 GMT  
		Size: 1.3 MB (1332261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec221a4e8aac361f0d917d3dbff85fc30193910186ddedc6befae7a5594e2e`  
		Last Modified: Wed, 04 Jun 2025 23:53:26 GMT  
		Size: 28.5 MB (28543176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec93fdd5e183740266b380b46b13e3c537b74b7c4aaa72e411a891684ef6583b`  
		Last Modified: Thu, 05 Jun 2025 00:03:08 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1dcfa359ece58673c113c0892de2be8df285bdda4992df266e3462a54c3f1b`  
		Last Modified: Thu, 05 Jun 2025 00:03:10 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca135b8760ceb47b233f5b829bff84d0ffb28893e6d62e9a0c7dac6f7f6a03c`  
		Last Modified: Thu, 05 Jun 2025 00:03:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac9fdf519dafd7fb65acf33eac1280a96ff411344e204cf3531c3883b08e3d`  
		Last Modified: Thu, 05 Jun 2025 00:03:24 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e4b853331cd77250a85f98172ac03c93e180ad3af5ff776fecfa2a3671cbd744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6755536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5f51059637d882f8152af6dba3f82633a164f89a7e1fd2c1edfabf6d6f684b`

```dockerfile
```

-	Layers:
	-	`sha256:eaa9473e4f49431fd72f702432463f7f289364b4156c1b2f016125a8fbad71d9`  
		Last Modified: Thu, 05 Jun 2025 00:53:47 GMT  
		Size: 666.3 KB (666268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:774a94069cfdbdc7daa3c078b1d3ef79cc9f0e19c81ef4191b7f902f61036946`  
		Last Modified: Thu, 05 Jun 2025 00:53:49 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd4bbb9a8a29cc4747bc7dacc698ffda68fa937c0f4003f8adb969e49e21d93d`  
		Last Modified: Thu, 05 Jun 2025 00:53:49 GMT  
		Size: 2.9 MB (2938087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb538180ec96273c4607177c61bf2d1f7ca6cf54cb8090f75cc2b68542933a70`  
		Last Modified: Thu, 05 Jun 2025 00:53:50 GMT  
		Size: 59.9 KB (59893 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

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

### `rabbitmq:4-alpine` - unknown; unknown

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

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:aa0ac212fbcec68f2ef658a218aeeca96b5ed30f8e8f0fca75f183210748abf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78070449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a63058802a004410e68a6399d1b37f2c3d6eeabaeee0673bf2cadd3b7cc01c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 30 May 2025 21:14:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 30 May 2025 21:14:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 30 May 2025 21:14:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 30 May 2025 21:14:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:14:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 30 May 2025 21:14:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 30 May 2025 21:14:13 GMT
ENV RABBITMQ_VERSION=4.1.0
# Fri, 30 May 2025 21:14:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 30 May 2025 21:14:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 30 May 2025 21:14:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:14:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 30 May 2025 21:14:13 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 30 May 2025 21:14:13 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 30 May 2025 21:14:13 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 30 May 2025 21:14:13 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 30 May 2025 21:14:13 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 30 May 2025 21:14:13 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 30 May 2025 21:14:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:14:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:14:13 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 30 May 2025 21:14:13 GMT
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
	-	`sha256:83c7bd077aef103fb01bce051ab38aa989642def1563dcd3d3ad854c8f9751cd`  
		Last Modified: Wed, 04 Jun 2025 04:54:23 GMT  
		Size: 28.5 MB (28451473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ea5427d90f54247047b4bd3b0f8bd9c687bce9ef64200cd10089e689d7ceef`  
		Last Modified: Wed, 04 Jun 2025 04:54:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48651eb5be9355e246d0ebf83773834f271f9c4488bed1c8ee5eb7064567df4`  
		Last Modified: Wed, 04 Jun 2025 04:54:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd3d371140e190a7d8263ed13ba28d0f7e093d401dab8330129d0bad79db00`  
		Last Modified: Wed, 04 Jun 2025 04:54:28 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde4585d6b429d452bc963b0fcc4ef11dcd89136cec68234e1ca722e28ae91aa`  
		Last Modified: Wed, 04 Jun 2025 04:54:30 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e68d09e4e4d084887b678f461bc92676881e8302d83d8e8ad7fd1350556053b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6865332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba40b5a007fd6b9a67f191a597634a0d18454da2c35a459517f8287b79183dd7`

```dockerfile
```

-	Layers:
	-	`sha256:f2e08d61a9b0b6945dc4427493c7a803c0122879251bef6966f868c550a7e73c`  
		Last Modified: Wed, 04 Jun 2025 01:39:34 GMT  
		Size: 666.7 KB (666725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8357b2b6c22fe1ffe5d4d8de22c4c7a227dca4c968755034557cb6b6def34653`  
		Last Modified: Wed, 04 Jun 2025 01:39:35 GMT  
		Size: 3.1 MB (3146563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae92c5efea0a001cd44f17c69f7da0ebc9341b73a07b0aed4266e710f455c2ea`  
		Last Modified: Wed, 04 Jun 2025 01:39:37 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:786781eda83cb6b911837e13b12f7675503ced9ff0eb55393104734d100a708d`  
		Last Modified: Wed, 04 Jun 2025 01:39:37 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

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

### `rabbitmq:4-alpine` - unknown; unknown

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
