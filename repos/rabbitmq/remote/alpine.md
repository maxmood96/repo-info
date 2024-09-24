## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:2b01eefe80f95eb4e1e2552fe46431de19b67950f530f1b44ac3df506fd52f9b
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
$ docker pull rabbitmq@sha256:438a20a260cefe3cc9ddbe48d9b16d561c5a863e8eb73fef6c2705a494804482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74024860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b485c6e2194aa478b98c69f3f291daaa26d6860d0e23a6767f88287f3ca1951`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a09dd5992a6f2882df5c05e22a78becbd9a1ce5bfc243689ad76622dd05eda7`  
		Last Modified: Tue, 24 Sep 2024 01:07:02 GMT  
		Size: 41.6 MB (41571048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32b392fd8a72a3ae0e2b38cf8b57a3d57899f89b8b47c9ffa1e71b37e11044`  
		Last Modified: Tue, 24 Sep 2024 01:07:02 GMT  
		Size: 8.3 MB (8284887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05a17184ae24c8e1f5a0cd67bd3a30e9f6f47cf1848462fa46b967e39328f4`  
		Last Modified: Tue, 24 Sep 2024 01:07:02 GMT  
		Size: 2.2 MB (2234372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dafd1e64ad7ccc55c07ae790035f8032faebabbbf3c6f113fe0bd10157e6c`  
		Last Modified: Tue, 24 Sep 2024 01:07:02 GMT  
		Size: 18.3 MB (18309000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdeb8f117be6892a4ec243d4976771e6c996b6d4d0645fd12e6285005cdd55`  
		Last Modified: Tue, 24 Sep 2024 01:07:03 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf375c7e8f455718df51e3efa5a9c4c4db55f03e5ba5755280d6231d63d537e6`  
		Last Modified: Tue, 24 Sep 2024 01:07:03 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b19c2ef9343d4c5381ab99f1ae41d57cdcca4e73fa56e6a98157aff0a4b9b2`  
		Last Modified: Tue, 24 Sep 2024 01:07:03 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb932313f0f136e32e69352600a1f096632b921960e1eaa8d69e2a0ca389e8ab`  
		Last Modified: Tue, 24 Sep 2024 01:07:03 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3814357a2c91189cf5d80c9126402255cbe3c9596270ea42a5040899b1019c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 KB (59446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998991d19f2fd320f6548c835e700fbbc44fbd21919e2b2991d180eaf591203e`

```dockerfile
```

-	Layers:
	-	`sha256:f67c280c069f90c3f8ea3e9d66f54d99c592f7492850ab00c3ee5c7c0a0d0d0a`  
		Last Modified: Tue, 24 Sep 2024 01:07:02 GMT  
		Size: 59.4 KB (59446 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:7e7591fa8bd15b6960f960fc46392c161e209a6fb1dc1e615e7b6cc1ef01670f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63173095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577ffcff4d6b5f6a0e197f103daeed48bbae315917659707cc1bda196e159df4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc86c03e9da6b54d1acf7c43dbee9686494771dbd572357ebf468acd00875d`  
		Last Modified: Sat, 07 Sep 2024 12:04:52 GMT  
		Size: 33.2 MB (33185875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd269fb16bdae3e476ff0d39c0432228b661eb9e4202284f15ed23681039615`  
		Last Modified: Sat, 07 Sep 2024 12:04:52 GMT  
		Size: 7.1 MB (7079945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbb0559a74c8d168c21891fc520f8c60ea643b12725bbbbe46ca4ca1c5d68d5`  
		Last Modified: Sat, 07 Sep 2024 12:04:51 GMT  
		Size: 1.2 MB (1230004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3510102e8caf62ae2f25fcc5b2446452ec1ca9594b2b9890508a08a4a77fff27`  
		Last Modified: Tue, 24 Sep 2024 01:01:25 GMT  
		Size: 18.3 MB (18309021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724b524b2be6c882faf4e591a9b2322d000c87da91a7b39865d59824ad7dd5eb`  
		Last Modified: Tue, 24 Sep 2024 01:01:24 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3f7c1ae08318d043697e39f4ba2c4487c2110c7205c1a2178a5bc64e89763f`  
		Last Modified: Tue, 24 Sep 2024 01:01:24 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a86eab17190cee564bc3dee1c56f313ddbde0f709beb684b9c7914e00698a28`  
		Last Modified: Tue, 24 Sep 2024 01:01:24 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ae4de1ca62ad447ab31a2ee321f646d931a93fb3dcb180550970409be7bd35`  
		Last Modified: Tue, 24 Sep 2024 01:01:25 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0d05aed8cca84edef7310ddff9b463402cebf3ba4c783d8f3222eedbbfa7af6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f17eb0b0c8bcb7a8a837ef709ab777d2532d866bb120911f6402961cb2fcb2`

```dockerfile
```

-	Layers:
	-	`sha256:afc918ad8773de4ed6aa9aeb42ed2f52aa63f38203158d707fb5041e8ec293c0`  
		Last Modified: Tue, 24 Sep 2024 01:01:24 GMT  
		Size: 59.6 KB (59633 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:7a9304a3acd7e62828d729379ef8982078b01f4dd06ccabe444750592146b5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62343061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7566caa3a10b636897598b5172aaa2da66af8134f6cc425b4dd8fc973aca7da7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd9d453be4c080b9b86f2acb6b9dbd0ec34c17a1163757b6966259831cce69f`  
		Last Modified: Sat, 07 Sep 2024 12:26:04 GMT  
		Size: 33.1 MB (33087585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd729021b6dae860ba7a13249de85f7343adb05da25af22277cea034f3d84ba`  
		Last Modified: Sat, 07 Sep 2024 12:26:01 GMT  
		Size: 6.7 MB (6716593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b4185c167bc7761ccec13a8003dedb2855a78327479ef4585745da32adee48`  
		Last Modified: Sat, 07 Sep 2024 12:26:01 GMT  
		Size: 1.1 MB (1132942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb2019fae8d5fc83deed2589b603aed8ddca9c5b53ca04e4a57f680722c1740`  
		Last Modified: Tue, 24 Sep 2024 01:03:27 GMT  
		Size: 18.3 MB (18308700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df909a5734b5d6291048ac459b7c2667ccedf32c9b816f02bcfc7d5763116033`  
		Last Modified: Tue, 24 Sep 2024 01:03:27 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f7890917d1d9a3e5b1ef9213cf137493a12e106dccced569efc5f2f79e8f12`  
		Last Modified: Tue, 24 Sep 2024 01:03:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e1731333dcda2d683c114655d59733290e1101105e8c64c41f11dacd8a81e8`  
		Last Modified: Tue, 24 Sep 2024 01:03:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3fb10a53364a7d8bf72c5e276a6d7cf7a10acc20a1458ce00fd37735dcf6f6`  
		Last Modified: Tue, 24 Sep 2024 01:03:27 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c1cade6b0a8d2bed3be5fcf78d02d97af5bf4bb30e3d13a1735946e2aea53957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6221434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0705dd407891c230308a15f99bda74c604d0b46cd58021d32492858073a3a2c3`

```dockerfile
```

-	Layers:
	-	`sha256:a9854a333144a02c6ac750f0a2ab70b253006966020db3226fe0eaa091845e72`  
		Last Modified: Tue, 24 Sep 2024 01:03:27 GMT  
		Size: 638.4 KB (638386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ff9f690a6d166f639d360dc0d8386ef901a79ab9cbf0422defafabd01f27215`  
		Last Modified: Tue, 24 Sep 2024 01:03:27 GMT  
		Size: 2.8 MB (2830899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2065fa3f5c06de8ff2183589bc5611259daee3217e585b94f484a94c49620ad6`  
		Last Modified: Tue, 24 Sep 2024 01:03:27 GMT  
		Size: 2.7 MB (2692297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f083c52267b1a4d729024e158552792f7293feb6522e0e3466f9a9004095e0`  
		Last Modified: Tue, 24 Sep 2024 01:03:27 GMT  
		Size: 59.9 KB (59852 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:796b13e8e3c15258c8c73e136d1b3068d97498fcdd9a8fe235f134aadd2dca69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73405779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3a1d85032942f14b46934542e754c4ad7a7cb8d573b9d9a739af7f96015ca5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3c99bf71fb3b6f073fc14ae9527292614744ea736f6351d9de7b1c6e787049`  
		Last Modified: Sat, 07 Sep 2024 11:21:55 GMT  
		Size: 39.7 MB (39690107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f601b017a968c1401d45c5107f6d079226f3a855bd3defe75fe86a114b6fc0`  
		Last Modified: Sat, 07 Sep 2024 11:21:54 GMT  
		Size: 9.0 MB (8995974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbba0bc4bfef30f4f115198675779fca456958eb4635fc517d242dc50ef70c3`  
		Last Modified: Sat, 07 Sep 2024 11:21:54 GMT  
		Size: 2.3 MB (2321274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cd162e6da27672483eb2ee0cbb62d01e9abde42955ba352852d86c94e61fa8`  
		Last Modified: Tue, 24 Sep 2024 01:23:08 GMT  
		Size: 18.3 MB (18309034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82722a57f6b9be057185b8e14dd9920d1d14527fdf5a86cca3b223ca3829322`  
		Last Modified: Tue, 24 Sep 2024 01:23:07 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a6501b0bb3a1dc8dc9d2ce18bb484a4946e96b85169b41617a0b36d8f81625`  
		Last Modified: Tue, 24 Sep 2024 01:23:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b3f8325edaec209d9f93c3f7873a3acd6eba1fd984f2258f9f59047ac8bc71`  
		Last Modified: Tue, 24 Sep 2024 01:23:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f967f6a09700f9acb666345f9125f9049c14c8f8333926cf002ba590c8ca37c`  
		Last Modified: Tue, 24 Sep 2024 01:23:08 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:61374f39cf8f13a9c6c203164825181cf3d403472db6e168070bc23948a5870b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6462130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e363452de26087291e64227abf3eaa0643b95f04e59114fe3b1ef20bdbb3d9df`

```dockerfile
```

-	Layers:
	-	`sha256:0cd0acf3232eec8011d27b0a3725b6b2d499717d09aef6daf6bec1d9953a3958`  
		Last Modified: Tue, 24 Sep 2024 01:23:07 GMT  
		Size: 643.1 KB (643109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3505da8a31286daa155a7032caed711e165c49b485f0555ea6f4fd0b8c3f616`  
		Last Modified: Tue, 24 Sep 2024 01:23:07 GMT  
		Size: 2.9 MB (2948826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27b0866e7a68946c1389dbafec99995e05d3deb3e3133c8bc4c21a4d59e84392`  
		Last Modified: Tue, 24 Sep 2024 01:23:07 GMT  
		Size: 2.8 MB (2810230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1174eee5a169bfc87d637af983340999aa531d538a9c31934463c32a73f81a68`  
		Last Modified: Tue, 24 Sep 2024 01:23:07 GMT  
		Size: 60.0 KB (59965 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:b2707333f2646fe4f60b117ed77b8b2ce255c3eebfd713b0caad6de2435a508d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64693523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a6ad43f218198b4f4186421a0da606386dc13221b6681d8e088f2eb548e616`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c056ee028d65190c5985b38a481f5cd6aba47180296b599f0610bbeddfd2052`  
		Last Modified: Tue, 24 Sep 2024 01:07:15 GMT  
		Size: 33.4 MB (33357541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38aef5459b3909461694dfd7e14b458cddbb73ab565b4cbe470ea6edcd9b9cc2`  
		Last Modified: Tue, 24 Sep 2024 01:07:15 GMT  
		Size: 8.3 MB (8324829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c343533bca2bd74e2c3b52f590f242b580e97e50a533b0625d727cb5de7475`  
		Last Modified: Tue, 24 Sep 2024 01:07:14 GMT  
		Size: 1.2 MB (1231508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4887f8d7e76b782261c1c1749c10d22898c782b56df7dc9064ddf148df2d39bb`  
		Last Modified: Tue, 24 Sep 2024 01:07:15 GMT  
		Size: 18.3 MB (18308728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d41a18ee2a697a488bf50ea854085fe51533f4e00089765a77c32e7f119080`  
		Last Modified: Tue, 24 Sep 2024 01:07:15 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4700c18e0dcfe3691b6d4dbe15282008c2ca2648deda61d6475d0d2e9934d2`  
		Last Modified: Tue, 24 Sep 2024 01:07:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061dd8ad69d979e5904f79a5d230bf66e35362ec88684a6ac9d958fc64c8a522`  
		Last Modified: Tue, 24 Sep 2024 01:07:16 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55c90491a74fafe513852010e2399a779afd01d19a10373a0fe174dbe9dc66f`  
		Last Modified: Tue, 24 Sep 2024 01:07:16 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:eb2d50f610d57b0530a9e08b7a1bd287952c16c53b40827eec01f89f6b065f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 KB (59399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d46542efcc383022d0beb18c5139882d273eab36ac03c7cb487c3b126fc46f`

```dockerfile
```

-	Layers:
	-	`sha256:34471535a1780f954eae991fdb8733a658cefef07cbc2041df9e801495650fa4`  
		Last Modified: Tue, 24 Sep 2024 01:07:14 GMT  
		Size: 59.4 KB (59399 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:5e989f3d8a540815ab9a407dded2d2d2bd09c0f4e4cd575f331329073fdfe128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65677754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e025f0e76c9054eb6cab303514ec1a5712eae9810b1b5c2ea9ff6c1bce73837`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcb199bc4be6814c9d55db2fca0bb542fc5a767492af5adb4442ebffc5b31a9`  
		Last Modified: Sat, 07 Sep 2024 11:14:56 GMT  
		Size: 33.6 MB (33614675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cb8bdef0126f8e62c83419b737c1ee93fd719e3d6903e080179b8421f163fb`  
		Last Modified: Sat, 07 Sep 2024 11:14:55 GMT  
		Size: 8.8 MB (8834094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e71b4c9ed62eb3a7d96bff484d4203eae06a5c748a111ab80a1ffff3cd7d97`  
		Last Modified: Sat, 07 Sep 2024 11:14:55 GMT  
		Size: 1.3 MB (1346081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18551c523137f2e456a04582d6c0b116c63485189a23d77a13428e8de9d875d3`  
		Last Modified: Tue, 24 Sep 2024 01:35:51 GMT  
		Size: 18.3 MB (18308733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ba145d00a401a4059e068470f52efb16c364bd0c391ef185ec55d8a7d0acbd`  
		Last Modified: Tue, 24 Sep 2024 01:35:50 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee2ecd6a0bd8c910a48aff833d61d24aac785bd6b71c0c342c926dff96385f4`  
		Last Modified: Tue, 24 Sep 2024 01:35:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838358c61833472eaf360d20ab91d1e19245d640527841d173dfdfac06a8c4fe`  
		Last Modified: Tue, 24 Sep 2024 01:35:50 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833fc53bdff56db4a187c2ff82b404dc8b8e969a4697cf650f665d68bcb81259`  
		Last Modified: Tue, 24 Sep 2024 01:35:51 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0075575060ee7804cf0a140c4e4c0c1f28f361887d13426317225cc57672a979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579fdd1620c02d8e023469807e035932890d43568801ea19836633e8da75dc60`

```dockerfile
```

-	Layers:
	-	`sha256:ecba93881ec0c7764ad371d8387e9fb22973116586272da070206a52ce6e9a1f`  
		Last Modified: Tue, 24 Sep 2024 01:35:50 GMT  
		Size: 636.4 KB (636430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c78f3265cfc044f79ec14f8ad6c46febbe88349956a4aa46d07f78c95a380134`  
		Last Modified: Tue, 24 Sep 2024 01:35:50 GMT  
		Size: 2.9 MB (2921304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6186ce4cf7386f8ad69f643a2f150b1a689edbd50fdc9c53cae45bf3fb71ba`  
		Last Modified: Tue, 24 Sep 2024 01:35:50 GMT  
		Size: 2.8 MB (2782696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e3ded515e5445bc950331873ad3f65c5ab7c7f067fb810701ee5cde17e71d3`  
		Last Modified: Tue, 24 Sep 2024 01:35:50 GMT  
		Size: 59.7 KB (59719 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:2def296efe13c346fcaa887933bac8e29f7f0f52ba82834d5f13f38602427b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67381899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2ef37a0ac5f9e58dc6f6e6b9a9a5081ad1764c5f874c64b818e8162b65f8d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d541526334938416ce86387328ea1389282f9c31e5f50b4a1f50b184b762df9c`  
		Last Modified: Sun, 08 Sep 2024 07:39:54 GMT  
		Size: 34.6 MB (34562240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f20314d91607af74d9b0bfea7a13585bccf5925d9297c73963560cee8f2c00`  
		Last Modified: Sun, 08 Sep 2024 07:39:51 GMT  
		Size: 9.9 MB (9866547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac183215d5cf0095068fdd0fedf851340a7c89f1a424b6a1c44cc48ba69fa61e`  
		Last Modified: Sun, 08 Sep 2024 07:39:49 GMT  
		Size: 1.3 MB (1270891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af473c2aeff01cdb38ef4e2e3fa0b7758122dbe6aca350cdfb5cc72955a0ad`  
		Last Modified: Tue, 24 Sep 2024 01:33:31 GMT  
		Size: 18.3 MB (18309015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be67e2d3992e31645c129f3f1a095b081e0c3d7077476b34b266571c623361f9`  
		Last Modified: Tue, 24 Sep 2024 01:33:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b70d3b4d9691bc5ff2ab5c14436c79b1760023f42191b7cc0a0a45ffb1c8afa`  
		Last Modified: Tue, 24 Sep 2024 01:33:28 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2e5011def5688d8a99ed3502bf30723586d9a321a2fd4eca9f39239e50e83c`  
		Last Modified: Tue, 24 Sep 2024 01:33:28 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b145125094287efa34cc88dc4519a58faca5cc22e8e5119870ab087a13a20a`  
		Last Modified: Tue, 24 Sep 2024 01:33:29 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:69a53fef7ad5beca7552c38497c7028edd426a1d45ce017efac3283eefa74350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6435251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed178a4fc71a58e0822601c0489275bba7c6c3945cdbb620e9952ddb67742783`

```dockerfile
```

-	Layers:
	-	`sha256:f02f8f17ca5e299c214c76d6e21dfd89444f74643d935f0ac6ecf1a62d84a834`  
		Last Modified: Tue, 24 Sep 2024 01:33:28 GMT  
		Size: 639.3 KB (639273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dbcd1a0723b25877d972c585e3eeb78030e861ec97129edb99011c12822b1af`  
		Last Modified: Tue, 24 Sep 2024 01:33:28 GMT  
		Size: 2.9 MB (2937427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46a604c01dc4300f574a9a00855632a38fb007e3bd316a99cd34641041bd6ce7`  
		Last Modified: Tue, 24 Sep 2024 01:33:28 GMT  
		Size: 2.8 MB (2798831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389bf381bbbe2c11cead881dafe3dbaf6974751ee98ec836bfe3f6140672b384`  
		Last Modified: Tue, 24 Sep 2024 01:33:28 GMT  
		Size: 59.7 KB (59720 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:3b24a3d2a5ef8a621bbc9c1a476c27a9e68e0a94f75ec747bbb81fd0eaa97630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64268743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164fd31e65db0d1419d0ca755303934aec40445aab706d174c4ca7a2dac430fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b817b10a0c9729e45812971a59a7c7610314759cf9920828f966b2ccdb6831`  
		Last Modified: Sat, 07 Sep 2024 10:17:23 GMT  
		Size: 33.7 MB (33689699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8569e07ef45dc8559fda5855d29b0a8e020c14ec39d9dbe44037f4f005302c`  
		Last Modified: Sat, 07 Sep 2024 10:17:22 GMT  
		Size: 7.5 MB (7481813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86fd01dd71699fad1a630d604ea6bb31cd3a64ac5c268ce8ef06697cc87473b`  
		Last Modified: Sat, 07 Sep 2024 10:17:22 GMT  
		Size: 1.3 MB (1325141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d739ac8cf6c420c6a20f14a3e5e65734933d9068642e933cdb4be6f8894fc5`  
		Last Modified: Tue, 24 Sep 2024 01:35:21 GMT  
		Size: 18.3 MB (18308746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19d60c35e3ebea86befc4a743c5688d15b8b489952240a85a9bee8df1480bd4`  
		Last Modified: Tue, 24 Sep 2024 01:35:20 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8635d047986ba0ffe2171fe4b8464b55a6d64f38d01bf711af3a7f6cb3fb5c`  
		Last Modified: Tue, 24 Sep 2024 01:35:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18896e92c5c40950ac36af34b488af12cb2d96a97565148c59e9376d0f16786`  
		Last Modified: Tue, 24 Sep 2024 01:35:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3103dcdcdd50f01d153e85fe4680dcac122e6f6e5302daca5261c6f2c75b1658`  
		Last Modified: Tue, 24 Sep 2024 01:35:21 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7ac53d04f46eec4f3a58dde9c85911eae2c835b1587bc3353d445d40c5c33605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6234197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310b739791e7932329cd3789fdb885be3a2365071921e6232af7b16184e15ff8`

```dockerfile
```

-	Layers:
	-	`sha256:3c09139071bddcc63d901520d66b8ae08d0e43640b81ac946cfd193df49c083c`  
		Last Modified: Tue, 24 Sep 2024 01:35:20 GMT  
		Size: 636.4 KB (636396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6da76154caba411ff62301e10bd403e9045d13baee531f0b8f48539a968030`  
		Last Modified: Tue, 24 Sep 2024 01:35:20 GMT  
		Size: 2.8 MB (2838357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0814572cae464002f66405d2a35b4769ea5d5363a8135d9eff3a96fc355086c`  
		Last Modified: Tue, 24 Sep 2024 01:35:20 GMT  
		Size: 2.7 MB (2699779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7641f65cc38bf2bd8813a355c2faf4826d7c2b4d548e35caac623aa94d716147`  
		Last Modified: Tue, 24 Sep 2024 01:35:20 GMT  
		Size: 59.7 KB (59665 bytes)  
		MIME: application/vnd.in-toto+json
