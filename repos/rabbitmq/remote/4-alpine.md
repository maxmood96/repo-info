## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:bfe3024e9239980caeb084dc3d691745b802950de925d291dee3477eb617e001
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
$ docker pull rabbitmq@sha256:b69e81eb685cd8830406c83f9c22de6626b707f72c4bba44b91f5c0eb4d54c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77639898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97183b56e8e47b022be980b0a5d69275f809cd555f92508e87887f1c9a2201b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:50:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_VERSION=4.0.7
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:50:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:50:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb135fbad6e539f8e9e5e3906d9267df5be3883ea7d9af0995994258c19a2b1b`  
		Last Modified: Wed, 26 Feb 2025 23:34:30 GMT  
		Size: 45.0 MB (45008614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3e36e9b7d303f401f95aa3ee0bc2891ed01596c10723480c2f020051070cdb`  
		Last Modified: Wed, 26 Feb 2025 23:34:29 GMT  
		Size: 8.3 MB (8311610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cd5c391184eb054a0930520f9a1c4038d620d43fbe5a6d0c98499a29f62395`  
		Last Modified: Wed, 26 Feb 2025 23:34:28 GMT  
		Size: 2.3 MB (2277758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263e7dc5f7cb1db6f40f96d4b3f935ea4ccfd48e37813f4101ec53b952e39e9e`  
		Last Modified: Wed, 26 Feb 2025 23:34:29 GMT  
		Size: 18.4 MB (18397926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d0016e1dd4762b17b6b0e3f4baf2752e7cbd3e8dd8b3c0ac1264e156d2ba7e`  
		Last Modified: Wed, 26 Feb 2025 23:34:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3a585208358ff0ef30724d8efbad1aac8cca1d602cdfccb7ed259de3f76bab`  
		Last Modified: Wed, 26 Feb 2025 23:34:30 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f1d63a233138020ca76a078b1d941120868ef971ce163ab07c83f31d62a3e2`  
		Last Modified: Wed, 26 Feb 2025 23:34:30 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6231f576aeb7f72ed32a09000a23137c89a647942c00e303e1caa1d8025f79a`  
		Last Modified: Wed, 26 Feb 2025 23:34:30 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:12ce671e4f477f4dc7eeef5d834980f903f6dad738213e4c5695481c08ff62da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532d946de8bd4e2afed36f7869788238a0cf736b93cda574be1547cf3cd5ab96`

```dockerfile
```

-	Layers:
	-	`sha256:19258d57ff44236176fa05286b91d3aa02fdd82a5cea8ec0d287b0220c80ebce`  
		Last Modified: Wed, 26 Feb 2025 23:34:28 GMT  
		Size: 538.2 KB (538244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b2a288af3cf3fa866076f85b858f9f6187cc5dc05897dedabc926802fa7ba73`  
		Last Modified: Wed, 26 Feb 2025 23:34:28 GMT  
		Size: 2.9 MB (2932259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41f0a46dbe66b59ccaaec62336464e02524f4d13625f38bc4bd634c7449016c`  
		Last Modified: Wed, 26 Feb 2025 23:34:28 GMT  
		Size: 2.9 MB (2928081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d2963c43facae15909f82500d01cdc5334cdf061cc88139bd40c4b622352c6`  
		Last Modified: Wed, 26 Feb 2025 23:34:28 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:a867d75d0d09bd9dc043c34c71c5238eb05b17c7a9642b1ea1ce18f2bd3db06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65700388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1750d986ebff3ddf2cf3b87a208935cfb42903a95fec5dbd853f74e5dc46b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:50:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_VERSION=4.0.7
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:50:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:50:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2054ccab4ad2b8e18ed7051196f3628814f771c8cb3eed3feba78ad08f6a6d5`  
		Last Modified: Thu, 27 Feb 2025 01:55:27 GMT  
		Size: 35.6 MB (35613015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3feab93f8f673296711cb75b23d68bc57b1b114bbe2e2b36e9c5b630f776b6`  
		Last Modified: Thu, 27 Feb 2025 01:55:26 GMT  
		Size: 7.1 MB (7097948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8f4b20a49162460d8b9dd04936a073c19e5b4a84f24fb89bcf76cdf6a7970`  
		Last Modified: Thu, 27 Feb 2025 01:55:26 GMT  
		Size: 1.2 MB (1225233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5834135d44077d2e5ee4895fa5740a5a1a1e1fa20d88155857957ba598f7d8`  
		Last Modified: Thu, 27 Feb 2025 01:55:53 GMT  
		Size: 18.4 MB (18397718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a636e15bbc53821541b06189f2e84a80c8c074b5a3b210de08d152663aaa88f`  
		Last Modified: Thu, 27 Feb 2025 01:55:52 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50476b7a7babd44299be34188838910e9e5cc1dc8cdd4ffbf6c616391f285020`  
		Last Modified: Thu, 27 Feb 2025 01:55:52 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731b3a5eaf65367a9998b96e3d52d59fa82732395e7461428afbcec73b419a98`  
		Last Modified: Thu, 27 Feb 2025 01:55:52 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dc87133eacdabf6738881c5b369ddb536ec0386dcf398e00840aa5756e7115`  
		Last Modified: Thu, 27 Feb 2025 01:55:53 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:64a8db8b8354c57bee716e81293d7627a14522e0076de45a954fc0f20bdf35b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf48a8e23cdb03dcd4db086ee0eee9ec1010124d6decc97efeb0bd4749fdbc25`

```dockerfile
```

-	Layers:
	-	`sha256:9be1ff4f055ff75fa1ff28139f9aae768840b1d85d80ff1c4a972b6c13250a42`  
		Last Modified: Thu, 27 Feb 2025 01:55:52 GMT  
		Size: 59.8 KB (59836 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:9a4a2cbc93bf9145b5344775abc91c07c31bd032632d4220753c7d808dc96951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64905252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ded5c8be9960c354ab7d5dc30e05f70f61f26bc7151ba862b4381d7f188266c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:50:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_VERSION=4.0.7
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:50:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:50:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59be88dde2ea4a7f6f8742b8b3e5a20e9bb6c2202cdc9335a957849b811d0fb`  
		Last Modified: Thu, 27 Feb 2025 02:09:08 GMT  
		Size: 35.5 MB (35532423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebca2b7423a59eed129e6cfda80f44d0d84486e9e2197e422a2d8cb201a6b5e6`  
		Last Modified: Thu, 27 Feb 2025 02:09:07 GMT  
		Size: 6.7 MB (6742218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3688b328b794162257171d8da5786aa073bade43a0cef30e288f1064455ef5`  
		Last Modified: Thu, 27 Feb 2025 02:09:07 GMT  
		Size: 1.1 MB (1133042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1af5d232f0e5790fe540b8fea41a83eeffc9cab5d12a1814f3a790ade322257`  
		Last Modified: Thu, 27 Feb 2025 02:11:18 GMT  
		Size: 18.4 MB (18397707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb1786ce67672006a4b7a80135f094dfa44e65b4a9e77941df853d9b107ae50`  
		Last Modified: Thu, 27 Feb 2025 02:11:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d99af4347f2104805a5f2ec67d92e7a1328779090f2b1116bfb6d89728431fe`  
		Last Modified: Thu, 27 Feb 2025 02:11:17 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee827cc6b90680f8a84f66cc7832718d6335edcc4c1f854c377293de5764a8e7`  
		Last Modified: Thu, 27 Feb 2025 02:11:17 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0b4aaafb31e82411265b26034217488d1780919afb6508eb2c326f0134d33c`  
		Last Modified: Thu, 27 Feb 2025 02:11:18 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7c1f5a61ed95dd2b672fed9b622c3f74f8d21d65e96dfe947b428a04b3966a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6494355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee44978183306e6d5330c560986b74de88f4ac39ac8046c6dce9e0c2f153361e`

```dockerfile
```

-	Layers:
	-	`sha256:84e786ac85d611daf64cf15a3a9eb8de622f4ec44feab7c3d0abea9387791710`  
		Last Modified: Thu, 27 Feb 2025 02:11:17 GMT  
		Size: 653.9 KB (653945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f276b5e798fa7f8580bffbab312950da28523388e4a9ebe562c94e819cd19e`  
		Last Modified: Thu, 27 Feb 2025 02:11:18 GMT  
		Size: 3.0 MB (2967749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22e919359abedbd769025c599ad331ecbea0328092391eb955beaf48a1369080`  
		Last Modified: Thu, 27 Feb 2025 02:11:17 GMT  
		Size: 2.8 MB (2812610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28d18b1a6ac03e9ae3092b75fab36969e91188c447c7833fefe86be4343f7fc3`  
		Last Modified: Thu, 27 Feb 2025 02:11:17 GMT  
		Size: 60.1 KB (60051 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:40de30b9c27650f858e6448956b1e562413b90a028849cd9158cc42f3302b470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76750702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60303e7313d5b9b731d7533aea3f148b2a4b2bafc87d44048572b621a6f2bff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:50:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_VERSION=4.0.7
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:50:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:50:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477e41e08c5af86bd53b51932f168adb45563eff7145f1a1bdede91b851ce92c`  
		Last Modified: Thu, 27 Feb 2025 00:42:17 GMT  
		Size: 43.0 MB (43000726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3815e8bce911895078e73c723d94f15a7172d7f1e2dbb3708c1f522784e1100f`  
		Last Modified: Thu, 27 Feb 2025 00:42:16 GMT  
		Size: 9.0 MB (9034845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405351bf94813a6a64c3278b1e36f468e5bcf6f93f6bcb183a0ed6b2aa072ca6`  
		Last Modified: Thu, 27 Feb 2025 00:42:16 GMT  
		Size: 2.3 MB (2322469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33914d6e49d176aacebd13cdd42d3c556dc456eed9f25832eda01a1c2aebf8cf`  
		Last Modified: Thu, 27 Feb 2025 00:43:51 GMT  
		Size: 18.4 MB (18397897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9882bf1f76d867d84270b049af3a408906d3578209906abd324c5e963c57afd7`  
		Last Modified: Thu, 27 Feb 2025 00:43:50 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3364196291628e53409745773c5669c05e52eabe3f2901ee2f3ee586af712e65`  
		Last Modified: Thu, 27 Feb 2025 00:43:50 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0c41dabb8ddb90c1845ed6d49d467f6827197f7fe71c53ea4f7533724b4514`  
		Last Modified: Thu, 27 Feb 2025 00:43:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76185439e2e50fc4f8991377bf2cd68f49d44b456b70db488730cb2d955cea84`  
		Last Modified: Thu, 27 Feb 2025 00:43:51 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:414c7a897e4d2d33f1d527bc334d835948aac565fe75f510a90e741a2b96902a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6836963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7503f8b03a6d6e419d948e698149ad8ff5498ca09f0e1d11a915bfde8c873c`

```dockerfile
```

-	Layers:
	-	`sha256:4ab251cf35342ca090904245fd57c92e207b2ed1cef00273ed25ac6914fd36a2`  
		Last Modified: Thu, 27 Feb 2025 00:43:50 GMT  
		Size: 658.6 KB (658591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3532b12284eaec6a6ed23f9bdc70ea304671ef8695abcafe3b66ec3ba740a4`  
		Last Modified: Thu, 27 Feb 2025 00:43:50 GMT  
		Size: 3.1 MB (3136704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9c51d8ca359dc61eccc2ffef5df4497e13bdef929c6c1ed79234d310a41843`  
		Last Modified: Thu, 27 Feb 2025 00:43:50 GMT  
		Size: 3.0 MB (2981571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8d3cafdb12fc5ee70a08e4798c1aade375d83f14d774de74bfe67da8f4c03ac`  
		Last Modified: Thu, 27 Feb 2025 00:43:50 GMT  
		Size: 60.1 KB (60097 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:bf7acb1c420fe77a81b12ff87c72609bd1f63d6d96a31e843d362347078346eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67122989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0ede428e9cb9b685a8115c7514b3f408fc8e1d156dc0caca3fcaee9cb54a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:50:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_VERSION=4.0.7
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:50:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:50:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f4f2fb1a55fbc4ff10b4e0f389172735325e1381b6d3a25c92061c83d92642`  
		Last Modified: Wed, 26 Feb 2025 23:34:14 GMT  
		Size: 35.7 MB (35705857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd532ba74fd39254438c4f36dd83e765116559e843e5d3317e3d3cb6bcead9d8`  
		Last Modified: Wed, 26 Feb 2025 23:34:13 GMT  
		Size: 8.3 MB (8324824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae6da63d07d0d68c8790b3e6e71ba3cfb750b42e173b4fedc2486e5e905e8b0`  
		Last Modified: Wed, 26 Feb 2025 23:34:12 GMT  
		Size: 1.2 MB (1229231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563141cc51de6337c61258c43b18e769cee5f1bdc6cd60bc14f4b5592a40e13`  
		Last Modified: Wed, 26 Feb 2025 23:34:13 GMT  
		Size: 18.4 MB (18397709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac75ecf8ef9baa2a292af4ef2a64891b15a27d4f730e516d3456aa53224e9e63`  
		Last Modified: Wed, 26 Feb 2025 23:34:13 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494f4c8fd794fbf71791a641c79f6569df0d40b43756239c9aa77570f3f8b0e0`  
		Last Modified: Wed, 26 Feb 2025 23:34:14 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5ef4a4a13e4c651bf2388d057f0cefd6e116adad49a133d1b31f4c69950269`  
		Last Modified: Wed, 26 Feb 2025 23:34:14 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f3fee4d182af83f42f6012a831874e7e203de0d4a1c27cfd5d1a616c51aa21`  
		Last Modified: Wed, 26 Feb 2025 23:34:14 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:403faac596cfad999c79e0cd78be1588d1a22b77d999c3628ad913725bbb8239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6431637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dfa902c1e8924f9f24b4f4ae4ebca5228d8c7cc0c38cbb5581a7393aca042a`

```dockerfile
```

-	Layers:
	-	`sha256:fd2782070b178bf98c1b8844cf4ee6841976af698ca5e94f7824ed1dfaa7866d`  
		Last Modified: Wed, 26 Feb 2025 23:34:12 GMT  
		Size: 533.6 KB (533593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76198a389cafee48aaaa299e1cc2da13d94ce81c96cf128d361fefc10b3ad47`  
		Last Modified: Wed, 26 Feb 2025 23:34:12 GMT  
		Size: 2.9 MB (2921205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0301d1bab6b511508183b766bbe03050e932f8b5f6cfd92e27081a93264efc18`  
		Last Modified: Wed, 26 Feb 2025 23:34:12 GMT  
		Size: 2.9 MB (2917031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28434479939b456890a4e12b5f10030ce27268eb2eedd2889a9c4ec0762712cd`  
		Last Modified: Wed, 26 Feb 2025 23:34:12 GMT  
		Size: 59.8 KB (59808 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:52cbea5e9def5c6059604aa8246c6103c4746a3ae52847b8203a987395c57b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68250114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf2d698d7adbe37adcb5a38f1ba49b513a420a01c7cc7a7432a93fbeb504a13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:50:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_VERSION=4.0.7
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:50:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:50:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1511fb8bd3137e2de9dd3fc0445586587535c15cef7d20a048072524c68b2f48`  
		Last Modified: Wed, 26 Feb 2025 23:38:16 GMT  
		Size: 36.1 MB (36083097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ef3626067c050b444c4d3cc4bd96523e149f2df0b794848ddf5f47560e798a`  
		Last Modified: Wed, 26 Feb 2025 23:38:15 GMT  
		Size: 8.8 MB (8848306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ddc1d7bf390c59addf33c15f4e83ed3659a06296aada56fda2525731e075c`  
		Last Modified: Wed, 26 Feb 2025 23:38:14 GMT  
		Size: 1.3 MB (1344997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97420b1ac8367bcc7c303dd8d3fdbcf8abf39337d5e78257f45db495bbe0be`  
		Last Modified: Thu, 27 Feb 2025 02:46:06 GMT  
		Size: 18.4 MB (18397622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19cc21bb345eafdf4bb7d2522e22a15114ced09f54844b17ff78defd5fd7030`  
		Last Modified: Thu, 27 Feb 2025 02:46:05 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74013ab750e13e9469960e272e0411d58ea2e3bb6190903e6e08faea7c2119c1`  
		Last Modified: Thu, 27 Feb 2025 02:46:05 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36cac926b8744ed1a72adecab577763bab14b1db5a8082b92cc5ea78a806cd9`  
		Last Modified: Thu, 27 Feb 2025 02:46:05 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f3e62e30736892e521b236d69d8a4177fbc11bbed2a12202f9dbc6dbecdfe7`  
		Last Modified: Thu, 27 Feb 2025 02:46:06 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e7a65d05aa5f42eda39d765a9e20039ac75b294380648f5a298360a390756fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6732633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f653c59209c992adfe456fde36d5be8ecdb179d062fa692bbdff1084810273`

```dockerfile
```

-	Layers:
	-	`sha256:da1886cc931ca6dc451239f38442c664ea5107552fb2c305c3ecf56d1367aa9f`  
		Last Modified: Thu, 27 Feb 2025 02:46:05 GMT  
		Size: 652.0 KB (651992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0299620ab80c64d58616408de1bcb0bcc7c8e248435b599d8deeab9249646a90`  
		Last Modified: Thu, 27 Feb 2025 02:46:05 GMT  
		Size: 3.1 MB (3087933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c26df7684cd67d2e93fedd14124d68a49f21a4a49b1db59acae9a13f0789079`  
		Last Modified: Thu, 27 Feb 2025 02:46:05 GMT  
		Size: 2.9 MB (2932788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e58ba7edaabb03d9978c0aa7ac044a9c906d5364758675ab8dc0ce2b7afe5e11`  
		Last Modified: Thu, 27 Feb 2025 02:46:05 GMT  
		Size: 59.9 KB (59920 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:130f2663c986ccd9a6744087f3d5d1edf20fe1ef58cb8b2ff9e4f6036a326e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69898898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117e34bbb976840ab06a8b3642fdb15febed070f466f464103c52252233b994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 11 Feb 2025 18:31:38 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 11 Feb 2025 18:31:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_VERSION=4.0.6
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 11 Feb 2025 18:31:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 18:31:38 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 11 Feb 2025 18:31:38 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 11 Feb 2025 18:31:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Feb 2025 18:31:38 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 18:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 18:31:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 11 Feb 2025 18:31:38 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bdcc48601bd3ca5e87a5a7bc99c08b43c14990913d5753677f13cd741c12cc`  
		Last Modified: Sun, 16 Feb 2025 12:13:40 GMT  
		Size: 37.0 MB (37026873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c58d001604f8043f97e1abcfc67d352c8e8120d5a6cbcf13c589cee25eb4ca`  
		Last Modified: Sun, 16 Feb 2025 12:13:36 GMT  
		Size: 9.9 MB (9858952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8680070b94e8dc4aff6b58cffcd547067b652f0a7da5c5b1490418120a9c912`  
		Last Modified: Sun, 16 Feb 2025 12:13:35 GMT  
		Size: 1.3 MB (1264897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b4c0bfd2cc576b13eaf2b21318b6958ab3eb0c1d832a1ad3407bcbaac05a94`  
		Last Modified: Sun, 16 Feb 2025 12:20:39 GMT  
		Size: 18.4 MB (18394981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea77b190b6655a39254dc64b8a539eeac44ec34e4dfee781f435b44809fac15`  
		Last Modified: Sun, 16 Feb 2025 12:20:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294c42c8e851c7dc76344b50b4226c0bbadb21bb8588101efea1562f3ad8b2f0`  
		Last Modified: Sun, 16 Feb 2025 12:20:36 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c0107545346fed0cc43f08c6ab2aaa15eebb5bc3a2302fd3697bdf3b0e5f8`  
		Last Modified: Sun, 16 Feb 2025 12:20:37 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6ec96b432d0a2c6561c13e2f225c655729d58c7f46f4e689ce70f2fa6179a`  
		Last Modified: Sun, 16 Feb 2025 12:20:37 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:198cf66e971aecf0a3d91d066351b77b40365280851e054384b8ecae7d7c1dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6810734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e0a9ac36509a3c78c3317be7441821fa2571f60b00818fe7865ee3928838f5`

```dockerfile
```

-	Layers:
	-	`sha256:d69b23eb3ea3ac957f8c8a5105c77185b90259c86890490c9535207e9724bff1`  
		Last Modified: Sun, 16 Feb 2025 12:20:37 GMT  
		Size: 654.8 KB (654778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61ab931d85ed2cedeb5235f81892fcb903e2a0156e904df76bd1be0773649445`  
		Last Modified: Sun, 16 Feb 2025 12:20:37 GMT  
		Size: 3.1 MB (3125582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2bcf8ab538ca6352c88d29d1ab4eee40831545d295a568da920b09f7de54fc`  
		Last Modified: Sun, 16 Feb 2025 12:20:37 GMT  
		Size: 3.0 MB (2970455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8e47e6abb724a0e624c4e3cd95c8288bb47a789b837568062bed404c0965c68`  
		Last Modified: Sun, 16 Feb 2025 12:20:36 GMT  
		Size: 59.9 KB (59919 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:dc776113c683c5fde9fcc68fcdb60c19b5eab2169ce7866ac378df6c104969e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66824066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e50806910513327afac180db22e43de50af8064d83f9e2be4da8ba5f79d28dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 26 Feb 2025 19:50:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_VERSION=4.0.7
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 26 Feb 2025 19:50:21 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 19:50:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 26 Feb 2025 19:50:21 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 26 Feb 2025 19:50:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 26 Feb 2025 19:50:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 19:50:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 26 Feb 2025 19:50:21 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938123073369393f08c1c7edbd230c579acd0590d79772f1caf7c321937e8c8`  
		Last Modified: Thu, 27 Feb 2025 01:56:41 GMT  
		Size: 36.1 MB (36122889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20972f89b5f36b01e9417dc5118251a1dc87cae21013f3249d17920d49013caa`  
		Last Modified: Thu, 27 Feb 2025 01:56:40 GMT  
		Size: 7.5 MB (7510948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b0e395b4751d0ca4526f03b9da3f5554a0bea56cb50afce65c0fd0be2b35e`  
		Last Modified: Thu, 27 Feb 2025 01:56:40 GMT  
		Size: 1.3 MB (1323231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10c8f7c2e547af22a7199f57244f5ce30071fa39ac235feebef9553c304be99`  
		Last Modified: Thu, 27 Feb 2025 01:58:45 GMT  
		Size: 18.4 MB (18397691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb7deb8aa2160d84993155bb7f84ba4974f44c76061cce402c1a8129ae5f609`  
		Last Modified: Thu, 27 Feb 2025 01:58:44 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b9ae7808cea0d9e453ca2f1df09ede76763f51859f2fcb7cc59c95321310af`  
		Last Modified: Thu, 27 Feb 2025 01:58:44 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5027a0a8bbdb8f9b347c71cdcde06e2c9509c04910c617d0e840d40cf343979`  
		Last Modified: Thu, 27 Feb 2025 01:58:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6236424aa092708addafce32436912e58136dd574488095e5c195ebad43ab10a`  
		Last Modified: Thu, 27 Feb 2025 01:58:45 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:07c8ff8961ce77259e4905a5caf535043172517b64cee80447aae8821aceca69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6512501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2220eb43b82210a75e0f81cb0530bdbde8675d712ed2b089b0523d2f5089a`

```dockerfile
```

-	Layers:
	-	`sha256:625a861b0537599b3fe5e5401f966f3b2e1520adb3f5766fdce175fab7ca75c2`  
		Last Modified: Thu, 27 Feb 2025 01:58:44 GMT  
		Size: 652.0 KB (651958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64f1fab758492f2edfb3885aefbfe429d04a45138af11b6f69646b45e088ba`  
		Last Modified: Thu, 27 Feb 2025 01:58:44 GMT  
		Size: 3.0 MB (2977900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b5a9b8b7d0d7f23a546b6d28f9749f209135427923cc44b4be4c7c38bdbf36`  
		Last Modified: Thu, 27 Feb 2025 01:58:44 GMT  
		Size: 2.8 MB (2822785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb975bbf7cf8724621cdac17156fe8904c29446c9599e1b031379634e941c7c4`  
		Last Modified: Thu, 27 Feb 2025 01:58:44 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json
