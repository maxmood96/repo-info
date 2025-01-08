## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:53c8614344f6bd5ec2afb664bb0b27d746797c21b98465c3f700709188aec908
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
$ docker pull rabbitmq@sha256:db61e3dc9d69f2b8c9afc2d7f1ecda6106f1e233bf3541273e8d3922d22fcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77573491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384aa9b09e1dbfe7066da6883bef3050d7456a90fc79abdc02e97c4c57551ba7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 06 Jan 2025 19:11:15 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Mon, 06 Jan 2025 19:11:15 GMT
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c84ccc703dbfd81d42b1968e0fd98ea3d96662a3a6a106721ae5181102d0fc`  
		Last Modified: Wed, 08 Jan 2025 00:38:50 GMT  
		Size: 45.0 MB (44989513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb63fd913d48f815f301a962b654372c9cba6fa7b5e820593c18dbe2bff18445`  
		Last Modified: Wed, 08 Jan 2025 00:38:49 GMT  
		Size: 8.3 MB (8309076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a518ff37989673c3f49730620e26e2b221e4e0c68ffde3a0de58d0e7f009a62`  
		Last Modified: Wed, 08 Jan 2025 00:38:49 GMT  
		Size: 2.3 MB (2277953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1253e9ac029d946f32e2d36e44a0700688510569dbfed7cce29716d31180e69e`  
		Last Modified: Wed, 08 Jan 2025 00:38:50 GMT  
		Size: 18.4 MB (18358978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce02fd884fe0ce9f79d7f0ceb1b8dbb20434781a3febbe0ac887a30237745411`  
		Last Modified: Wed, 08 Jan 2025 00:38:50 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29a5b26565f00f229b6a9e90a921924c0b1efa1d59700c208c7dc0ddd9a781`  
		Last Modified: Wed, 08 Jan 2025 00:38:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e48149add6a9da2d8df286666f1823d9ea37beb10a38fefb1af5e3190355a2`  
		Last Modified: Wed, 08 Jan 2025 00:38:50 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f469955504c68ebc52d68ea769af162815fbacf1e8d0ad5773af9413520fa518`  
		Last Modified: Wed, 08 Jan 2025 00:38:55 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:589c8b15a1aee727675085701b41e0f4ede27ae3316f4aa83e2eda10151c3283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6728289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58420e48b71ef13f14d9dbef1611439172cd06d24fc6283be6dd1fb15970641`

```dockerfile
```

-	Layers:
	-	`sha256:d7240d30de78a5a29725f16183a718d536b32ab592add6a5caf23b8583cabe5e`  
		Last Modified: Wed, 08 Jan 2025 00:38:49 GMT  
		Size: 657.8 KB (657762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cafadda15db8536e968dba2b2e2afab9de841e5fd3b2d6beb4eb38d6e486e775`  
		Last Modified: Wed, 08 Jan 2025 00:38:49 GMT  
		Size: 3.1 MB (3081579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea416361ede0c9bcaeeb14c400d242cd4e401ae85f94a49f587f69b07b50062`  
		Size: 2.9 MB (2928075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a677300c21a107b8540460109e20e51dd3195865be73eb4e6a7323d4afcb8a`  
		Last Modified: Wed, 08 Jan 2025 00:38:49 GMT  
		Size: 60.9 KB (60873 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:c3be7d3f8dec3c350c6dc7c5fb9af345ca6b6d1afa1ce4e9372dda37f5fb8de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65633455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95862af887e0b498989c180865035cc73d892333b0016a7ec8790d4f2411be0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 06 Jan 2025 19:11:15 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Mon, 06 Jan 2025 19:11:15 GMT
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
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e70201d061568774a35b1c2bde4b19ef7af5ddb7279e02c576d0af06b29e771`  
		Last Modified: Wed, 08 Jan 2025 00:34:47 GMT  
		Size: 35.6 MB (35594358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2811be3c8778ac922fca47c1ee1dddd4ccabd8883b907529a7e52726ffa564`  
		Last Modified: Wed, 08 Jan 2025 00:34:46 GMT  
		Size: 7.1 MB (7092022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692145b1035ca2aea0cbdac43122227396fab33cfa7cbb6f4b2e1ce215bda64e`  
		Size: 1.2 MB (1225403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab180d7f1a750d703b21e7a1f807e79c12659fe100ae3452fbf97071d56e1d70`  
		Last Modified: Wed, 08 Jan 2025 00:35:13 GMT  
		Size: 18.4 MB (18358896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b3b44ce42f0c267236dd87e5ca8ecfe4c1a17bd0f976669cbb3dbe65a0628b`  
		Last Modified: Wed, 08 Jan 2025 00:35:12 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e2d2506205ab641b7dcec24b279c823de255dec592e77afafa83d6e22b6e1a`  
		Last Modified: Wed, 08 Jan 2025 00:35:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f2adb0ac0c1304c46ca90cc5b1489d4fbe50d658eb177520944e2d3bbd772f`  
		Last Modified: Wed, 08 Jan 2025 00:35:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80313e8069e2a146508e07cf39d270338abdede8b414e17d4431fd90bb51765a`  
		Last Modified: Wed, 08 Jan 2025 00:35:13 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d543f73251d4b115792131d36b22702e6c2261e2b65e013956d3c64c17522756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 KB (60849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54af890a85f6f0dc772b01ea3c7e576d0c43fd1c3314beddcc2aa77898c7d12`

```dockerfile
```

-	Layers:
	-	`sha256:e215fb78825f2faddbdce74fa8a894f202e890f80f80a0a41356217e66d7916f`  
		Last Modified: Wed, 08 Jan 2025 00:35:12 GMT  
		Size: 60.8 KB (60849 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:c664a79e12721442ec9d3ab06e8f256da8f2db3b954a808356b620591a2bffc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64844528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e24ecc3b3954765af8a35f60b1a85ae589b59fda2c1e6f99ae589d0db126836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 16 Dec 2024 06:05:26 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b37d8f898d79e706e0b2ea8c101eed4ac9185e05625ec683a9fd8b9e8f720`  
		Last Modified: Tue, 07 Jan 2025 17:27:22 GMT  
		Size: 35.5 MB (35525581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fac8f7ac1cae799829826e080117b5650eef75987260b61b81ff4a9da25a9c`  
		Last Modified: Tue, 07 Jan 2025 17:27:21 GMT  
		Size: 6.7 MB (6731748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f90e20125cd8ff0a7f597f40214704e4956955cefbb8adcb8e6f6a59bcb7adf`  
		Last Modified: Tue, 07 Jan 2025 17:27:21 GMT  
		Size: 1.1 MB (1133191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b45101db6c60677d35cebab9444300c2ed7e26abf1fd7273c9c9cacd4e3bb77`  
		Last Modified: Tue, 07 Jan 2025 17:32:33 GMT  
		Size: 18.4 MB (18359018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f262bdde731828c65c0716fbb42e905f0596000a7fe3d9c42bafaa12d4097a7d`  
		Last Modified: Tue, 07 Jan 2025 17:32:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59256ecb3a40bc192000098547514c048a9f0e7bb0f135ff58e39eca927a943`  
		Last Modified: Tue, 07 Jan 2025 17:32:32 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f0b9940ecf6b4a946f11f7a8b9b0c7827e32adcaa1fe9f33c7f1c427b3654`  
		Last Modified: Tue, 07 Jan 2025 17:32:32 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8614b3866dab11b9bcb482acf0aa28a07a729e2db97b35817aae62a78af606`  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b48053b499d46b1f5fbfb9fd67e1128a04c14161f6cbd87f145a2f8450b18f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6493975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b810d1d06bd17c4a9afc662b032d9136ea298b8ce0ebeaf793aeb2bd1517de`

```dockerfile
```

-	Layers:
	-	`sha256:fa6c861115ccf9a966f3c71d44505c84a7bd7bd84a5c76ec575860663d04f1af`  
		Last Modified: Tue, 07 Jan 2025 17:32:32 GMT  
		Size: 653.9 KB (653905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbffd311702dd8193ec80576bf23ba3ebe653fbf9a2014f3547ba5b7fb2fa034`  
		Last Modified: Tue, 07 Jan 2025 17:32:32 GMT  
		Size: 3.0 MB (2967429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c08284162aa88f1f7630bc870a93ce14e33472df70721835a169eb8e56e4c12`  
		Last Modified: Tue, 07 Jan 2025 17:32:32 GMT  
		Size: 2.8 MB (2812604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ec4d52b569b4470962c8283bf757c3e8450e56a2dda334c105bffba23d9f05`  
		Size: 60.0 KB (60037 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:4522a98300e08f0e6d5bd53726cf7d83d08e11cfc8de01d63309fae7529d3e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76692226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba54630983efe4000d986d9503a906c6d7ef442d55e73288e8a048f1a413324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 06 Jan 2025 19:11:15 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 06 Jan 2025 19:11:15 GMT
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a09c7b2d23b1e7a37bc7a1d633f6e3d4f9f6404de8d2d4d9dc236537318b389`  
		Last Modified: Wed, 08 Jan 2025 00:50:23 GMT  
		Size: 43.0 MB (42993979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931e2a184d034c19e6429399700a6e8aa7194b2d4bb75be3ab626095e441d824`  
		Last Modified: Wed, 08 Jan 2025 00:50:21 GMT  
		Size: 9.0 MB (9031973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a8e2fa734a291aebde7349a5f05c907b54bfa6d6d744c485fdca0c11bd7b9b`  
		Last Modified: Wed, 08 Jan 2025 00:50:21 GMT  
		Size: 2.3 MB (2322577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12754928b77cea95cebc14914f0ee7bf4c01de73b015124e6b7c2013b362cd51`  
		Last Modified: Wed, 08 Jan 2025 00:54:28 GMT  
		Size: 18.4 MB (18358944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a062ba7ca8461c525ad0ea4f244b5d0fcdadaf7879f1336e1cda0ad7e875131`  
		Last Modified: Wed, 08 Jan 2025 00:54:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8633f789fd41b7ba8dce0d60dace1143f457c6c7c43f85d98e29787bf0c439b5`  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b13e3710ef2f92f48580d4811bdd690fe1016de99342dd63dc5b63d0905c4c9`  
		Last Modified: Wed, 08 Jan 2025 00:54:28 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8703c88596e6b0ee4adad0989ee528e3a82e7b1d28c77ff4c6ab5c6bbc5532b5`  
		Last Modified: Wed, 08 Jan 2025 00:54:29 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bcdce7d15c23ba602b76f1ed70e7def5875cb8ee4ceb2ac3be44922a6b119d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6837612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4d5bf5a3acbe85f584654e7b09a5edea8a2316a2fa05c03687dda620dd411d`

```dockerfile
```

-	Layers:
	-	`sha256:0b962d65ce5bc2b8f5ab57866dec72d5dabb3fae2e7dac12d20cd9f9129d9032`  
		Last Modified: Wed, 08 Jan 2025 00:54:28 GMT  
		Size: 658.6 KB (658551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25cd76f6d64e89671d8cf00ae0504bc5179872b0562c34ebb80f8518ab78ee90`  
		Last Modified: Wed, 08 Jan 2025 00:54:28 GMT  
		Size: 3.1 MB (3136384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4dafdf4179824b3583d60feee7a510a2f8063fc02d24a8ef52e46fe166bde4`  
		Last Modified: Wed, 08 Jan 2025 00:54:28 GMT  
		Size: 3.0 MB (2981565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0186d019e50da1134c9ba59e7ed9d6e5831f69942f12f8397d0a6d99e54a3827`  
		Last Modified: Wed, 08 Jan 2025 00:54:28 GMT  
		Size: 61.1 KB (61112 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:055b6c77f2420251cc26de45bf32ed65a4f1759b57876e77bb0638dba2a75bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67050302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ee9f9ed82d1cb94e9fea22fb7fae0539f5b092e0f08b083edef13210d4bbd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 06 Jan 2025 19:11:15 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Mon, 06 Jan 2025 19:11:15 GMT
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
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eefd925ca9e50518091f82094be6d517fba9928a3d18b67bc950452e2bebbc5`  
		Last Modified: Wed, 08 Jan 2025 00:37:31 GMT  
		Size: 35.7 MB (35681013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71104950e3d6acff519d88bb04eb6e1a87d7be64004d340a79a316950315c81`  
		Last Modified: Wed, 08 Jan 2025 00:37:30 GMT  
		Size: 8.3 MB (8320839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68176b3fc387bdfd6e7bc7c97bd75994a8df2abbb79180cce3e8a3307c3c6666`  
		Last Modified: Wed, 08 Jan 2025 00:37:30 GMT  
		Size: 1.2 MB (1229373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6482286c1995c204e68e24bd2335933075f0760a4ad71841f1203947fd0fd36f`  
		Last Modified: Wed, 08 Jan 2025 00:37:30 GMT  
		Size: 18.4 MB (18359056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64ab3eba290b51519eef5ba51ed2afd712dae653eb6302583f0fd6991a8f48`  
		Last Modified: Wed, 08 Jan 2025 00:37:30 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c0d8bf4b61635b20b8b311cf3ed7708b80a4e68932eb92fc5f86f0b1525d32`  
		Last Modified: Wed, 08 Jan 2025 00:37:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6858af81392ccd247b8d07fb5eb92f9f68983e8f36d111955b92f9f2c30e16d5`  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e427eb6582f12c801d7c208d3af57edf8690609cf7a72a6650112f2d23744464`  
		Last Modified: Wed, 08 Jan 2025 00:37:31 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:84fe0e5d7f86147202d119c52c111bd41e2504ee9c671f9f30479f49341a5c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6701482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b152348d57ea37a743954835f57f5b3b901edb471d3fce198ffb42031da7878d`

```dockerfile
```

-	Layers:
	-	`sha256:31a2228012e6c87a9dc37d0b53390518e2e08e8305869ee222972fe5cfcfaad9`  
		Last Modified: Wed, 08 Jan 2025 00:37:30 GMT  
		Size: 653.1 KB (653111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a62cfa4c7118d8c1442969c1ca9313f371f93e33a4ec290c3d5df620ea0fa58`  
		Last Modified: Wed, 08 Jan 2025 00:37:30 GMT  
		Size: 3.1 MB (3070525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5428d6ca445e129b700a211fec86b3595c9bd39ad1db3eb84272d19e9a38da27`  
		Last Modified: Wed, 08 Jan 2025 00:37:30 GMT  
		Size: 2.9 MB (2917025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2189a7af5456bb20af03318df30472ffb16eb188b0464f54393a8aee8098862d`  
		Last Modified: Wed, 08 Jan 2025 00:37:30 GMT  
		Size: 60.8 KB (60821 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:bfc0db73ba32784b15dbef07b99fcd3feb6f1adc40dd635709934a792d22e5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68203948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6fbf2be67d589d854bc6a4a936b240b2bd5bc65f4b6a36dad3690094e336a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 06 Jan 2025 19:11:15 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 06 Jan 2025 19:11:15 GMT
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7480f807f039edf3b444f8aa8dc1e21ad6d1eae14557aaab53659e8f172dbbb4`  
		Last Modified: Wed, 08 Jan 2025 00:54:25 GMT  
		Size: 36.1 MB (36085854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b5fe3e072aa6e24c760867515fac668ccae6044920a64e35c3352e2e811ef0`  
		Last Modified: Wed, 08 Jan 2025 00:54:24 GMT  
		Size: 8.8 MB (8844407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61e79cfb37ccc254d0a5e9948d2519984587352b1ffc48e3dff54244c1566eb`  
		Last Modified: Wed, 08 Jan 2025 00:54:24 GMT  
		Size: 1.3 MB (1345109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2748f35348c8d233143f8c739255cdeda037649c3aa7c2817d27e5f9696431c`  
		Last Modified: Wed, 08 Jan 2025 00:58:35 GMT  
		Size: 18.4 MB (18359082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3051889e36da0316b8a4386b267a33cd7f1144dce04c767039720979ab22ea`  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7cade3bbb3a0b1ed35c224c18f217409b49ea1befb78e5a37ea75d619dfbcc`  
		Last Modified: Wed, 08 Jan 2025 00:58:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a053c8e9923a5d27e8c2825d52faacb3a0919fe876a501e51941958af8afbe10`  
		Last Modified: Wed, 08 Jan 2025 04:53:47 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54992090ac91be46115de3f584f37a65320289634280466e8f8f9b2674e7cdae`  
		Last Modified: Wed, 08 Jan 2025 00:58:36 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4472382ce31ddba6764697e1f31c584a824f3682a0dfab648528a6e55def321c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6733280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb73746d21467c02ba67c6b78a219b5eaa862d42b105501dd45910d3715ea22f`

```dockerfile
```

-	Layers:
	-	`sha256:7e026919b2f7df3aac641979833147f574d52ce7d6b2da4f962ad773c912abc9`  
		Last Modified: Wed, 08 Jan 2025 00:58:35 GMT  
		Size: 652.0 KB (651952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e34d2c3a68d7e43028b0e12b252d80fdc6dd139e140cdf660760daae63f1ff5`  
		Last Modified: Wed, 08 Jan 2025 00:58:35 GMT  
		Size: 3.1 MB (3087613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07856f58e6faf8f217fbd6eadf6c7caa8bd2ec0eec9065592b834b35e6042ae4`  
		Last Modified: Wed, 08 Jan 2025 00:58:35 GMT  
		Size: 2.9 MB (2932782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354335635ea7beca1fac1a07efbdbdb0a910ce2cebc7e27e7edcec6db41db9bd`  
		Last Modified: Wed, 08 Jan 2025 00:58:34 GMT  
		Size: 60.9 KB (60933 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:893d3ad6b9696092c1addee1ed3beab1c4183da00ba1a14f140ff5995050afde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69862279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007f74ab4fece4bfde638807fe9bbab7b40a034cd2aecdf870af607665bf188f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f359027c27b19d95fc947dcd7e167020faf9ba96fa247b2f309772108cf5c0`  
		Last Modified: Sat, 14 Dec 2024 03:43:41 GMT  
		Size: 37.0 MB (37028323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2c797e41b0fb5384ce013ea72f66a5625585169049f297885e7c2061072ca0`  
		Last Modified: Sat, 14 Dec 2024 03:43:37 GMT  
		Size: 9.9 MB (9854310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48c2e72bba74432ea92c840dc923373673e2146e559cb70493f77492e6f6c41`  
		Last Modified: Sat, 14 Dec 2024 03:43:35 GMT  
		Size: 1.3 MB (1265041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f43ac3104e3c0b35911a978dab456856e20e3efb4b0373957cf0c3ee51d1f54`  
		Last Modified: Fri, 20 Dec 2024 00:19:55 GMT  
		Size: 18.4 MB (18358836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb17ab1e423e7a0e66fd9d9c5058cb7debe65ac636049590413b80e4f9430a8a`  
		Last Modified: Fri, 20 Dec 2024 00:19:52 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9316d5c73b3073322d90c5118045f53b352833ab23e4a2935f92e9aba8300fc9`  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f615432c00c0bc33c10ef0d45da09ec9abc6ac6d888285dba276340b599d8`  
		Last Modified: Fri, 20 Dec 2024 00:19:53 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3185baf7f69d1eceefb37f84b921fb25f00fbcd2a85981ad3ec43bb92b0fa6`  
		Last Modified: Fri, 20 Dec 2024 00:19:53 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:06cb80319c09cac68ce0482c7b0e7306837b5fd54629f749f3ce46b768dbf22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6810323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58dbc38c39f44b0b1c18e447d7e6b090827dd8e48d2153a6ecec7225027f5beb`

```dockerfile
```

-	Layers:
	-	`sha256:5ed80b3e8cb1cd2054c92cdbddc7cb94435e7cd09c482629e6ce96db466d265b`  
		Size: 654.7 KB (654744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b29095b8b693f8759a81a95e0da251e810046c6e9558183f66aa10b6b0040b`  
		Last Modified: Fri, 20 Dec 2024 00:19:53 GMT  
		Size: 3.1 MB (3125246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a089e01847cf56f38c3757c7783a706916dfd0e52d186fedcdf719ed3f13207`  
		Last Modified: Fri, 20 Dec 2024 00:19:53 GMT  
		Size: 3.0 MB (2970427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e9fc7fc89ee246cd7656ec36768b8f803a3aedc61e5707ae39bbffd8ad54f72`  
		Last Modified: Fri, 20 Dec 2024 00:19:52 GMT  
		Size: 59.9 KB (59906 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:f6980ebd86411df2ae70477ede8cebb983434c82bbb00fbb466c61281f98cb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66749786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ccaa2638b083555f4c4f87f54807adc48bec82e1368f71e337da09fa3a215b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 06 Jan 2025 19:11:15 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 06 Jan 2025 19:11:15 GMT
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f956a71ad1e860f7c9e2d44c04a4969443eeb1ecf7feac2ca19d3f21eeee3e`  
		Last Modified: Wed, 08 Jan 2025 00:50:52 GMT  
		Size: 36.1 MB (36097696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1289ebcd4b5d515fbbddd7a6c3f8e84f2bf2bcd1544a211bfbc4d1d5f7c2168a`  
		Last Modified: Wed, 08 Jan 2025 00:50:51 GMT  
		Size: 7.5 MB (7508449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8189aa60a086a1eaad2ec92198db32950c7b283c52e9373d0e40ebe0280cb453`  
		Last Modified: Wed, 08 Jan 2025 00:50:51 GMT  
		Size: 1.3 MB (1323337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba109b15d8b88b83adc74228b81f667cd21860892586f5ec729a38236a7bed92`  
		Last Modified: Wed, 08 Jan 2025 00:51:48 GMT  
		Size: 18.4 MB (18359115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39be5426fd7619aa817fe38a04fd740516d150119ec0bd49e97674660b3a0a61`  
		Last Modified: Wed, 08 Jan 2025 00:51:47 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656bd03ced857a8af9883b5de11dce2acf5e2ed876242d1a4e6b041df27731f6`  
		Last Modified: Wed, 08 Jan 2025 00:51:47 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b9922b3ac26777bdf1edb44bae537960f696cdd970ac80ec0f1883390ea53f`  
		Last Modified: Wed, 08 Jan 2025 00:51:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073b47ff18a1d928f60a784ddaca797c27f6d355a76760b286e75e79a5eaac41`  
		Last Modified: Wed, 08 Jan 2025 00:51:48 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bced330b11dd1b9dc72c0bae711c5c870b89e86e0725241c792ab6ad9870c94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6513150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae628b3d18e23348e43df3b529a46196eb673b0d4657e72c1ce4b6d795b0a07`

```dockerfile
```

-	Layers:
	-	`sha256:860433c1d62ad2360c359eceab784f39b9cdb284c9b5b59ad0880d9198674e71`  
		Size: 651.9 KB (651918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3c82520e86f17f78632ca4052ff6dd5c4ce9c660cdd536b6af59281207b7092`  
		Last Modified: Wed, 08 Jan 2025 00:51:47 GMT  
		Size: 3.0 MB (2977580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207fa0b683d659c735b5f40e9b2bfca958f9d3fdd6b18d01fa6d49446e355a84`  
		Last Modified: Wed, 08 Jan 2025 00:51:47 GMT  
		Size: 2.8 MB (2822779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:540b2def85714dae1f8ee31538f663179410c9721e763692f000c959e43512a9`  
		Size: 60.9 KB (60873 bytes)  
		MIME: application/vnd.in-toto+json
