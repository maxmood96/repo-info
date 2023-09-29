## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:552faa55ba15b761ef7ce2dbd06c5445c35118232c8e369c275e1bfc204c54c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:c3a10cac4a641398dbb9913ab77565b67a031ffda7a913c2cd9224bc28d73956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71039909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb339b019f557de3211871bcbf3dc318b064b310fb2c81cb8b04b85d24245b6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8994e7de72d44eaf8b1cfdc85aec64785d3ef7456f88941530d4979a443c86`  
		Last Modified: Thu, 28 Sep 2023 22:59:34 GMT  
		Size: 40.1 MB (40075621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7955ac2abc3ac30d691ae69706dcdcd6d3bcb29f4b6d7245beb8cae910156ebf`  
		Last Modified: Thu, 28 Sep 2023 22:59:31 GMT  
		Size: 7.5 MB (7545676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb473c2e498d64cec0036aa3fdc209aa1ae4e59cb55828045b299c70af43ed1`  
		Last Modified: Thu, 28 Sep 2023 22:59:31 GMT  
		Size: 2.3 MB (2297448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84907c204826daba7372b953d2b3a0bce55c8ce806ca2aeb6d27da5fba0779e2`  
		Last Modified: Thu, 28 Sep 2023 22:59:32 GMT  
		Size: 17.7 MB (17717453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1958bb5abb125c5c3532481e0349477e994ae58eeba30eaaf04ed93799dc1b91`  
		Last Modified: Thu, 28 Sep 2023 22:59:32 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562740ca2be2d56853b7865a60befc7b7090c3a2d5fe690f436725897ad4a0b4`  
		Last Modified: Thu, 28 Sep 2023 22:59:33 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f004f722719ec2b3a10efe249b6fb4c9c6d30f64941d5f7faad2c2f563dd442a`  
		Last Modified: Thu, 28 Sep 2023 22:59:33 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e7c844aaf956764c54367688fdb74499d52900ce8bc3219faf86338b5913fe`  
		Last Modified: Thu, 28 Sep 2023 22:59:33 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1cbd747a84646707ab1ed87d3f2c78778f55b6a2dc56eb24cd2668c8873bc7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.1 KB (763070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a538a8358c45403b39a5f8bc0f2b3f0635bd51396fd15b7c54446ab6672f094`

```dockerfile
```

-	Layers:
	-	`sha256:bbce1426231965e3fc030356d21a62c4b88eb2c85fbb6c6463748b563f1484e8`  
		Last Modified: Thu, 28 Sep 2023 22:59:31 GMT  
		Size: 701.5 KB (701508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14125a2001c43974f79e71d33d88f0c8a3e65f0a54757b4804692d40d10ce569`  
		Last Modified: Thu, 28 Sep 2023 22:59:31 GMT  
		Size: 61.6 KB (61562 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:e46a7dc9e69e9877e205bf47271d55f00673493d79d6e72923552da8de0f3e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61041683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d6c9519d9cde721edebc0826e3e5ced4e25ab77aa2572026d50d29b34c44a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a3be95759a045709ab38906f7cf6f6e6bf3c68df81e46b393e362cc33ad0db`  
		Last Modified: Fri, 29 Sep 2023 03:17:28 GMT  
		Size: 32.4 MB (32389317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1742b7e570e26dadff608fa018d00f79fb80fc6838ff8d74449f73fa9e2515a`  
		Last Modified: Fri, 29 Sep 2023 03:17:25 GMT  
		Size: 6.4 MB (6375332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1cb5bb11f2dab0cbc588d3ba3b7973975bd87a4e375da85d3ad6cfdb621e6e`  
		Last Modified: Fri, 29 Sep 2023 03:17:24 GMT  
		Size: 1.4 MB (1412501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774ad1926636cfabfd4407e492a3c47dd5750f3d78637e0a38e1f49d420e7dff`  
		Last Modified: Fri, 29 Sep 2023 03:17:23 GMT  
		Size: 17.7 MB (17717491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc78b8207a677abef3f8ce8775e14c031c9b22f615e8f8da24605e18d599669`  
		Last Modified: Fri, 29 Sep 2023 03:17:22 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4987796e1b0bc4fc4194b12a31d597061cb6044ca532888aa142b9390f20df16`  
		Last Modified: Fri, 29 Sep 2023 03:17:21 GMT  
		Size: 108.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b912f2a6ee84e7c13d75b6633d83a099092107ed45936544fd105e5e9ec342d0`  
		Last Modified: Fri, 29 Sep 2023 03:17:22 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c25f9a6f41ca53ecf0bee529609b077ab8619b69b5eba3f848be5e312cb488`  
		Last Modified: Fri, 29 Sep 2023 03:17:21 GMT  
		Size: 833.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:06e644735fbb39fc4378583d1e8aa3eb03fc2a9d2b136c60f749c88b90dff3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60267354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccead02731f56fa8c16f9e528cc183746b56da1ac36527a21fe566d79563a61e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b54b25b49d8347ed6149acb265176b78663285f2d55be185289c2301e98bc3`  
		Last Modified: Fri, 29 Sep 2023 04:53:01 GMT  
		Size: 32.3 MB (32267798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a3ac682cff16f1bfd95c8f6d7287a3522d94626374d85d28316331fa5a1d1f`  
		Last Modified: Fri, 29 Sep 2023 04:52:58 GMT  
		Size: 6.1 MB (6080042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcef1a60595cd13fc0d6833c1d2c2aad363a64b15d1e6e02c8bcd4a2cd18517`  
		Last Modified: Fri, 29 Sep 2023 04:52:58 GMT  
		Size: 1.3 MB (1300453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b603a9dc8913fc0913c55e10266af832bca388bf3ad2f60aa4353d7de16ff2c9`  
		Last Modified: Fri, 29 Sep 2023 04:52:59 GMT  
		Size: 17.7 MB (17717405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239cbf4963cad77fab49fd9c3045880daf1ba67777b1f8737ab4cde54c585824`  
		Last Modified: Fri, 29 Sep 2023 04:52:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822b30415da2ef2bbe91fd4e30ffebf099760a455825e7e04bb935ca2c3590da`  
		Last Modified: Fri, 29 Sep 2023 04:53:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288d1096a46e54c0ba4a0d6b3eeb79ff25746c6d1d4fc7511d533e5539129a9e`  
		Last Modified: Fri, 29 Sep 2023 04:53:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beccad4bd4c0421c3e31a98523af8931c9f7088e4187cc40024a9c694b53c737`  
		Last Modified: Fri, 29 Sep 2023 04:53:01 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3b26d852677416da43dc695e70f4e001cd4cf8ac7261e33a853548b1b372836b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.7 KB (845700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c535e0be1cd6dde9188aab7b1a9ff5b701f77ee72612d6c048364d2ec1d5b7ed`

```dockerfile
```

-	Layers:
	-	`sha256:fe165ce812aa48cf028619c7ceeeb03289a0c520a3f77e778e57f8062c6394d7`  
		Last Modified: Fri, 29 Sep 2023 04:52:58 GMT  
		Size: 784.0 KB (783961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d38751bbe5e43ed98746eaf237414ba5b339de0466ba0bf1084ad081d03fcb`  
		Last Modified: Fri, 29 Sep 2023 04:52:58 GMT  
		Size: 61.7 KB (61739 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:0350149cc499c727e60a1428384c92b0af3ed73b1e876bcd5ffdb704745cfcc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68431539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35a2a591395233cf17bd344f4f6b2f89138d0e19fd1f1d55d49e1460d3556c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc88776f25bc7a218134623254b6c2d572d6f6e753134e433a7a2fe68c9dea7`  
		Last Modified: Fri, 29 Sep 2023 05:02:25 GMT  
		Size: 37.9 MB (37873917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5c9a36641e9e898bd2558e32585cb96b8108afe2f223afb0162e85e06fdcbe`  
		Last Modified: Fri, 29 Sep 2023 05:02:24 GMT  
		Size: 7.1 MB (7137749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16eb7c85d44acece0dde95052bc6c32607bae2356c57b4ed0a55fd362f965459`  
		Last Modified: Fri, 29 Sep 2023 05:02:23 GMT  
		Size: 2.4 MB (2368785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a707216104048d323105e0304dbe10f5a121fb77786fc2722c81fe0affeb97`  
		Last Modified: Fri, 29 Sep 2023 05:02:24 GMT  
		Size: 17.7 MB (17717503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0320049f02ce064961fb6c0e20251c2281e3be81a7d56058268cea7682a778db`  
		Last Modified: Fri, 29 Sep 2023 05:02:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8558da8e8c4e21fdc87662841e006a199dc57d4e0436d6020bdc41854e42642`  
		Last Modified: Fri, 29 Sep 2023 05:02:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8ec1680bc5df46ffba344077689c7a895be34039d379f8d2bb8f421ee3c1cf`  
		Last Modified: Fri, 29 Sep 2023 05:02:26 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3f60ef87c9dca2a664677f1e4257474d543de75546c45c38c59e4c215b53a4`  
		Last Modified: Fri, 29 Sep 2023 05:02:26 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bd49615a91d1011f9c452ffc1092ea4f20876730ea47ab8361dec9fe4b5369e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.5 KB (849516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20da5e2c4bffd82f4c77226133cef1da5f1622947fec1436053e759b4293bfa`

```dockerfile
```

-	Layers:
	-	`sha256:a56899b325aa21d8cb2a29253210ed887c6d5dbf66ffddfe7e6ba49396809c71`  
		Last Modified: Fri, 29 Sep 2023 05:02:23 GMT  
		Size: 788.0 KB (787954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ef714902e01149d00b01065e7483fa614fb0cc25441cc984a21df59fcb2c62`  
		Last Modified: Fri, 29 Sep 2023 05:02:23 GMT  
		Size: 61.6 KB (61562 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:28fac4d6ac7c934d729df8e4b0afe42d51da0b399d58aeec6c219ca194599f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62417204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acaec18980eaa4cbc767963449530d992482d8e7a2b64934a5db840a8a043685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be277914484442ea603c47a6a9660f57e5ed96d9cbdde2bab7ea3067e9669da5`  
		Last Modified: Thu, 28 Sep 2023 23:00:35 GMT  
		Size: 32.6 MB (32623478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a8add6959dcdb8e4d24090e16b040abcc9e3d655098914f7478b6958fe9b23`  
		Last Modified: Thu, 28 Sep 2023 23:00:32 GMT  
		Size: 7.4 MB (7437021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790f294f2b39014c1d3fad99efadec1a0db21d4a8deb7fe2eda2c89d840335a`  
		Last Modified: Thu, 28 Sep 2023 23:00:32 GMT  
		Size: 1.4 MB (1401798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638455244b011df812e9425c88067998bb39be7b23b7025316a721e8c9de4203`  
		Last Modified: Thu, 28 Sep 2023 23:00:33 GMT  
		Size: 17.7 MB (17717403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a2bdcad4cb4d3bfd9cae078540c71369b5b4cb1bb671793a6a589f36b01b1b`  
		Last Modified: Thu, 28 Sep 2023 23:00:33 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c5528f9e55cd3e9b5d8baa7919f0891a05986dfd9db7789bd22d7641f4df8`  
		Last Modified: Thu, 28 Sep 2023 23:00:33 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a03797cfa0139386eeacf4ff953c62afdc9fe02005c78a51ee92ae2f406cce2`  
		Last Modified: Thu, 28 Sep 2023 23:00:35 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a850d086a3dbabfa1a9bab147cce4b84d20e9f6d277f97c58d06525eed404148`  
		Last Modified: Thu, 28 Sep 2023 23:00:34 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:161b664ce35d920006dd9e2153d95ceb3a3391375193010322d7fb40d1f00a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 KB (61288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad43ef5b48609b69091c28221cd800226fe3f02a1a0e2933effe64efa8634f`

```dockerfile
```

-	Layers:
	-	`sha256:f775ad7883132b42a84281c36929d966ef6c8f780704ce58f1e0c3a7f6d8f9e6`  
		Last Modified: Thu, 28 Sep 2023 23:00:32 GMT  
		Size: 61.3 KB (61288 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:8e9f7bec758a43372441dac9a3a6ebb61f08ca2151929aef083f811c48eb942f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63344734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9665d0baec3d2043f9052ad6aacb847c82c7286591264fda0031d0c91294c67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a045c25fd11b9fd90c9e8967e9490e0eb21f7b1e405473eb8c85a73a08769c`  
		Last Modified: Wed, 20 Sep 2023 08:44:31 GMT  
		Size: 32.8 MB (32805164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f9d6257a6f4981201814c155a708f761c5077b00a95895bc7ead8d675dd561`  
		Last Modified: Wed, 20 Sep 2023 08:44:30 GMT  
		Size: 8.0 MB (7951879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7fc7533ba9756c4efc58f88a7a7f79f986adf9c7d39dae5811e8c313aa087`  
		Last Modified: Wed, 20 Sep 2023 08:44:29 GMT  
		Size: 1.5 MB (1522272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71777141a11281a5d3c52bc4e2fe771e7ba16b5f5b12b2f9490299c9f3c353b6`  
		Last Modified: Sat, 23 Sep 2023 00:52:28 GMT  
		Size: 17.7 MB (17717416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf349b134317316b2bcd4f419b32c2463aef5d7d6da45cd9ad6b77d3063a772`  
		Last Modified: Sat, 23 Sep 2023 00:52:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2168f6fd8232ee2f64fa02ab2dd75a13ea056e16697e8e7ea5661d9e2d346`  
		Last Modified: Sat, 23 Sep 2023 00:52:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff46a688316f5061905914fca6baf4066bf49007705b00ad9037d8658bac9de`  
		Last Modified: Sat, 23 Sep 2023 00:52:25 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6183842b83581ca35f8a4ca4de6131031a330d9efd3dea120b0633767e6d35eb`  
		Last Modified: Sat, 23 Sep 2023 00:52:26 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6d873d7d6a4981e3c6c2196ab54c2d757e993207230be04f0209d138a414c474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.4 KB (757429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4952ae9defec8a5baf8277cfe0a4946a0c4b807d980ccdaf0a280aa793699d`

```dockerfile
```

-	Layers:
	-	`sha256:702e10685dec421f28d456bda9bb28fd5b8f8ee6136433a026cf429946753ac0`  
		Last Modified: Sat, 23 Sep 2023 00:52:25 GMT  
		Size: 696.0 KB (695977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b40edf2b27074ea449a9198230e10078b18275bee53d4ecf6045585aa3e870e3`  
		Last Modified: Sat, 23 Sep 2023 00:52:25 GMT  
		Size: 61.5 KB (61452 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:c55f41e595e6d5e9415a185996fd18c6eeb4af9d81fe381de49b66ff266e6004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61334734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c3a01935835fb2b5c03eb92584ab687bdbd7d9eafca874f18d83c3910da7ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b88d919c3d0ab39d1f9e97c5a1fac53063d4389b588dcea8d0863754cdd1965`  
		Last Modified: Wed, 20 Sep 2023 02:50:25 GMT  
		Size: 32.5 MB (32478793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299a5ba791ff5c4429a715201d1eebfcc7f2c60923469bbe55323441f899454`  
		Last Modified: Wed, 20 Sep 2023 02:50:24 GMT  
		Size: 6.4 MB (6427072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400e3bec233c1d961d75a55a6356c6fa1354aadad599a98a845a6dc543a1781f`  
		Last Modified: Wed, 20 Sep 2023 02:50:24 GMT  
		Size: 1.5 MB (1495500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cbaeea7e5843bc1c1b7c0401dc5fcd69ada531070250e8f3d1f929717c33fa`  
		Last Modified: Sat, 23 Sep 2023 00:51:23 GMT  
		Size: 17.7 MB (17717429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d3a513cd459dbfc561132e172da19e099ce685c41e1edf416fbfb69b5723f6`  
		Last Modified: Sat, 23 Sep 2023 00:51:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0b0344087dc10ea3ae01bf873f1b86a8ecec4488c67579888da289510f702`  
		Last Modified: Sat, 23 Sep 2023 00:51:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ea334b264f8f54543004cd64d8bf2c1f4d067df2e8a15a2161e882da858e17`  
		Last Modified: Sat, 23 Sep 2023 00:51:21 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d556be15020fccdf17abb3e25b63bc655fce3ca30ce57f87106bda2cd904f782`  
		Last Modified: Sat, 23 Sep 2023 00:51:22 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:76b04e693b52e41253d67dc9dedf0f74f336934c55241b178658ebf7316fb02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.3 KB (757306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb1b3df9582f939e9248b520ee9fca81a59ac6b5cf0f35863a5a9d01bce82ec`

```dockerfile
```

-	Layers:
	-	`sha256:fe30aff28988b9aad9860395fd58c0abe9a5281e8f567ac3a1e46bb5038a6c41`  
		Last Modified: Sat, 23 Sep 2023 00:51:21 GMT  
		Size: 695.9 KB (695910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d38f91fb4ec6fba5823630490ed71ee70f6a5c8f7575ac9a11eb6eb407fdb52`  
		Last Modified: Sat, 23 Sep 2023 00:51:21 GMT  
		Size: 61.4 KB (61396 bytes)  
		MIME: application/vnd.in-toto+json
