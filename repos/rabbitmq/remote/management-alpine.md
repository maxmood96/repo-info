## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:8519cbbc11989f2c3f7b8526cda718ecdffe0917774e7ed3599c040b34ac8b2c
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
$ docker pull rabbitmq@sha256:b120f75c3ee3e80b987a9c25fc2adc8abc71784e0a755da19b20de9d69d5e17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99567472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bd94fecc624f666a5009587195e7cc6038e1cf942e45a27bd337d408f5394c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Apr 2025 17:26:54 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
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
ENV RABBITMQ_VERSION=4.1.1
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
	-	`sha256:cb2c3b975dd5a90e504cfb1d90d60e038a06f482428a0d75f28412a9a8074ac5`  
		Last Modified: Thu, 05 Jun 2025 03:53:54 GMT  
		Size: 13.7 MB (13705896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fb044ca6374aa13b931b8c5f208249bd1c269af9866ac612f5dd64a20c2285a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1657243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ec72abfb0c1fc86d9a8bbfb19da07f90332f00e610a2326baefe05eb9b1055`

```dockerfile
```

-	Layers:
	-	`sha256:cfb8ff8a39acd416b7bce3298555433a74f9ae38496a6fe0f4ef4a912b4817d2`  
		Last Modified: Thu, 05 Jun 2025 03:53:27 GMT  
		Size: 1.6 MB (1646020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b60d43662dc0cd07c5c93889250c2328c763905322b08fec90de9de1e279d8a`  
		Last Modified: Thu, 05 Jun 2025 03:53:27 GMT  
		Size: 11.2 KB (11223 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:3d4e259bff67f4d5c3805cc8fa724c7c1efeee429fa61f79516faf4403c37970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88289369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639fdb10ef1896f5f96fe8ac9f5625eab7fd1be7f49dd71f00305ba33efe6924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Apr 2025 17:26:54 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
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
ENV RABBITMQ_VERSION=4.1.1
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
	-	`sha256:d4719ca4d7aab01573da114c34d503a40f5cf870d884b402f8a360da24b76edd`  
		Last Modified: Thu, 05 Jun 2025 03:54:14 GMT  
		Size: 14.4 MB (14384321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fb8c183e5f7117f6fbcb73ec4474af7d4ff750badfeb7a2e4f737033f71729c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 KB (11084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e9e3f1a18ecd52bd407dd90761b7a7dd259e378474258fe168f203dbfc0aea`

```dockerfile
```

-	Layers:
	-	`sha256:cab394e12c92e7ba4694bc2ba217f87053d0c53b7cf22cd72dba7b75fd2c963c`  
		Last Modified: Thu, 05 Jun 2025 03:53:32 GMT  
		Size: 11.1 KB (11084 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:b6d58c7126408a943c77476846b4af6f361df3567874f3eb49603b957be500b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87155512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35e544ef432af7920ed3309d0a54ed2aae935b4f40a1b7b34d9b80fc477a04f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Apr 2025 17:26:54 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
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
ENV RABBITMQ_VERSION=4.1.1
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
	-	`sha256:3bcc751c23d7a2d1bb3d2df36a07571c0cd68c2b9dc9e660872f5d981c571bc0`  
		Last Modified: Thu, 05 Jun 2025 00:08:48 GMT  
		Size: 14.1 MB (14051831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7bf7d5810584e70840c747575960ae6b2b581aca05cf088f2c21b3eace0b4257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1658348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f5eeda352d679881fd86086d07d2c6623f11623c0a76be5ac237db1843abdd`

```dockerfile
```

-	Layers:
	-	`sha256:af38f791a222f7b1bbd45a996fa183b585a14d47f15e9ffa561ffd06aa972b12`  
		Last Modified: Thu, 05 Jun 2025 03:53:35 GMT  
		Size: 1.6 MB (1647049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b528db08d9de8d44ad325360988828ce1f3d60066768835e3ecc6277f0f177b`  
		Last Modified: Thu, 05 Jun 2025 03:53:36 GMT  
		Size: 11.3 KB (11299 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:afc7455f3567640ee7f7f30e86be5bab92df40957f263702dcbd64477e8383d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98721621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f121e03aa4927bcb484a517cbd313b4803b04f60674796060ae962c92227e720`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Apr 2025 17:26:54 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
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
ENV RABBITMQ_VERSION=4.1.1
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
	-	`sha256:52eb03d12e8549bcd7f2e6c6cd7802a0d4e635a8eeb76951dcfe5304017475ae`  
		Last Modified: Thu, 05 Jun 2025 04:00:57 GMT  
		Size: 13.7 MB (13743079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:835fe3979203d624ffb97db6d035ef127e16e9bce13b3fbea4416f402d2ea108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1658224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a42d061e92597f2f32b2ca2606fb8e62ca06b3ce971e7351031cd678328a32a`

```dockerfile
```

-	Layers:
	-	`sha256:9fae27000ba2f5c47e75522c0f92faa370f892b65f62e0f25c0a3649db37f205`  
		Last Modified: Thu, 05 Jun 2025 03:53:40 GMT  
		Size: 1.6 MB (1646897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f64405e0875f3e9df1f565333fa61f42e29d9592be4897d2862b4d5c3e1b5b9`  
		Last Modified: Thu, 05 Jun 2025 03:53:41 GMT  
		Size: 11.3 KB (11327 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:fadd27331b7ac064055cbb71fc4482ec65d47ccada309c4c14504b2254bf25df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90561052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb7f31c913b10b8275e6dc88dc7fdf490b09ac90299697df1b81d6e4d523dc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Apr 2025 17:26:54 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
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
ENV RABBITMQ_VERSION=4.1.1
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
	-	`sha256:c773d8f9099caf559a6769ef1f482c34489596b50aa88934de655fca72efcb9c`  
		Last Modified: Thu, 05 Jun 2025 00:08:21 GMT  
		Size: 15.2 MB (15226452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:28663aa97b2789cb9dd90a39f84213d38b977e2e8e679f26b44eb2b01f00ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1657014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542ac45268bc0558434df2c5af1f2320602c33364712b78689ca2af488de84c6`

```dockerfile
```

-	Layers:
	-	`sha256:68425db24decfb2c5b4703528dbdc02b313a238520f2f7143a70d81d0d2af298`  
		Last Modified: Thu, 05 Jun 2025 03:53:45 GMT  
		Size: 1.6 MB (1645823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27527b5b220629c29736a84c93e089d6fd7555beeb5d074db3f2b9f2084f10a2`  
		Last Modified: Thu, 05 Jun 2025 03:53:45 GMT  
		Size: 11.2 KB (11191 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:ee3058975f7542a57770d86f7084412cfff014e3fb7f2e081cbf68e2ae00f95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91861439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc524ea2a67edc4d54861b7879ecf8706d49dbd7f18a3cfd298631292cfd6071`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Apr 2025 17:26:54 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
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
ENV RABBITMQ_VERSION=4.1.1
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
	-	`sha256:806ff637f5b8ac642c3903591dcee3472c22da1b418750feab063b78a4619d00`  
		Last Modified: Thu, 05 Jun 2025 01:07:37 GMT  
		Size: 15.4 MB (15381350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ad74222075a52ead283f318d8ae542fc3ce74277b7dbbcd1c4339f0e7da7cf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1656535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faeac962c2c976e988c9961e9b560fa8f21911886d53c86c31464ec93a7e824`

```dockerfile
```

-	Layers:
	-	`sha256:07fcb220b693106e795653fe1fca276a6d476cb2e2d9f3361947d3187077a322`  
		Last Modified: Thu, 05 Jun 2025 03:53:50 GMT  
		Size: 1.6 MB (1645268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fbde5ffb70abd82ccee072a24cba911d78c79991dc0e8826cca34b77829d3`  
		Last Modified: Thu, 05 Jun 2025 03:53:50 GMT  
		Size: 11.3 KB (11267 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:18137eda8add2a33abea63e564d35fdcf9177726f96525bda01b113f52f21212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92926504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb0a4ba06252afd662b4c3cb8f9301c20334edc1e90e5f13985d08a743c7f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Apr 2025 17:26:54 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
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
	-	`sha256:1944535f0656f00c35f894420ecf9883f1f47bac731f1201e8e1aa6afd8e2fe4`  
		Last Modified: Tue, 03 Jun 2025 23:17:06 GMT  
		Size: 14.9 MB (14856055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5d150edcb2431511d66d797e084fa98f045a886872490ff98286e343a66f397d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1656788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5bdca22b498c8a3051662eb05674afc234bb396835d13d69047f8e306be3f7`

```dockerfile
```

-	Layers:
	-	`sha256:90d74030c66f74ddc8523cd0dda303b8a8cb4c85feb806e660b5e57f9cc61636`  
		Last Modified: Tue, 03 Jun 2025 23:17:06 GMT  
		Size: 1.6 MB (1645522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3582b580ddc17e55a9abd105d2fc054ac4ee4598d2e1da5e80ece81b27b5faee`  
		Last Modified: Tue, 03 Jun 2025 23:17:07 GMT  
		Size: 11.3 KB (11266 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:0cdf46306197b3797ed820948c5f4ff210ed8ebc4ed7f2491369e84ec0890680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90472140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3270246ae739cfadc821c8d4820e4c25773443eb24f1439240e6bf2a3122ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Apr 2025 17:26:54 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
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
ENV RABBITMQ_VERSION=4.1.1
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
	-	`sha256:ac5316e2fbaad9aaa8432ebfe6f590a32468b8e00273652fa7ba0a0c094348c3`  
		Last Modified: Thu, 05 Jun 2025 04:02:37 GMT  
		Size: 15.4 MB (15392990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5203803e726c5a219ee1a268c039b554a6efc3d8b5009e6d1d6a9111253cb2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1655941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da6cb45c6b9f8513d2c23e55949224026aaed205d0e039cdb6e01838cbbf0db`

```dockerfile
```

-	Layers:
	-	`sha256:8f4258e94e6e4393c667504ddb03479e8548a5c23ae4dfc447b8ff6691cf1a34`  
		Last Modified: Thu, 05 Jun 2025 03:53:58 GMT  
		Size: 1.6 MB (1644718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446da70b827867fdafa52ebdf1720560a7d27b8fe9b7ffc2bfe8979158ff3afb`  
		Last Modified: Thu, 05 Jun 2025 03:53:59 GMT  
		Size: 11.2 KB (11223 bytes)  
		MIME: application/vnd.in-toto+json
