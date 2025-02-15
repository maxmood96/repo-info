## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:7561ed4a2be9a4673925bc641f97ca808bfda7c0868f29b85e209301b9d5b7b6
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

### `rabbitmq:3-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:ffe91efbae61a6885d4aa711806cbb81d6885d2b4246bd951f0fa1c8e54d0d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74003910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e3a5e4bfaa6f37ce1383c920eb277f4fbb157e32511810306a8161f4f0ef81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 12 Feb 2025 18:05:13 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 12 Feb 2025 18:05:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Feb 2025 18:05:13 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d4b40b79487100da1937228f1d06eb6172857bdd9c557d55324fc2a0aecdad`  
		Last Modified: Fri, 14 Feb 2025 20:38:33 GMT  
		Size: 41.7 MB (41725616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92f9ce475b3e1192dc4309ea792692d961567213dcbf13f9603f92b5d862f40`  
		Last Modified: Fri, 14 Feb 2025 20:38:28 GMT  
		Size: 7.6 MB (7600311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559d55bde23bd1b32473acd148006c2459aed54bb0927c89a76621b912e5cdf0`  
		Last Modified: Fri, 14 Feb 2025 20:38:28 GMT  
		Size: 2.3 MB (2277747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25b693183dbec3bf9674c676331a53f8795b78524b6ef94eef9ed32bf7567a6`  
		Last Modified: Fri, 14 Feb 2025 20:38:28 GMT  
		Size: 18.8 MB (18756239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3288550033f885d686a3a1c73e527861537566c4082749257631a5d5d40468`  
		Last Modified: Fri, 14 Feb 2025 20:38:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1799b1ae1fa3806c5c36b0599364b43ef473c405170ec92608e57a36e6c3919`  
		Last Modified: Fri, 14 Feb 2025 20:38:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f815e3bafdc4534b9e023cbdc57cb55df10045f9898187bf81a1a96173193a`  
		Last Modified: Fri, 14 Feb 2025 20:38:27 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54878108b4c08f41b01e926c49528b3d1bc92af1fb4374cb06c8ebc726dd1e27`  
		Last Modified: Fri, 14 Feb 2025 20:38:27 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ef93740c715c9ec9297886b4191e44f88f0e9eb6901943c977435fa740d68a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6457290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a522506f63cc3f6b080d98190407d02d1a9944de1f7e247cd023e2e7f32de965`

```dockerfile
```

-	Layers:
	-	`sha256:8f0aeff66c922f2f03c263034d09d238ae0c86504ca116c4ab12664cae4b7e31`  
		Last Modified: Fri, 14 Feb 2025 22:52:24 GMT  
		Size: 538.0 KB (537954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f30361d5a1acf2159e39730b8bc8f105223bc33ece0b25685e41d15158dddec`  
		Last Modified: Fri, 14 Feb 2025 22:52:24 GMT  
		Size: 2.9 MB (2931975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bb61830ccfdae90ec1cfb68ad683fade9d64ac801365d151293f2019636b72c`  
		Last Modified: Fri, 14 Feb 2025 22:52:24 GMT  
		Size: 2.9 MB (2927783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29624863983787ce46c6f507809a85b670d8eabfc7876c681111df2e40b5acfd`  
		Last Modified: Fri, 14 Feb 2025 22:52:25 GMT  
		Size: 59.6 KB (59578 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:85fab9c5f3fb4e6e52fc202cacb09754723386c336ea2207feba53543a22cd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63058661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfb2a985e49eedf9fb36496501d7172dcf72c0b2621859b411d145337826ce9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 12 Feb 2025 18:05:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Feb 2025 18:05:13 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88df697798f5eb5b49c899379bcea6e6153993c9c9f0a684d0b508aea30fddec`  
		Last Modified: Thu, 13 Feb 2025 01:54:07 GMT  
		Size: 33.3 MB (33285949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf998a61b549069e8c58cd8bcdfb662370e251cd82d5ee4ae7389b397cf7cf5a`  
		Last Modified: Thu, 13 Feb 2025 01:53:52 GMT  
		Size: 6.4 MB (6425537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccfff3831ae9c2367d6fd58b4ffb8c7e9e319ebe56610744069fb2ee3cb49c6`  
		Last Modified: Thu, 13 Feb 2025 01:53:51 GMT  
		Size: 1.2 MB (1225396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ab43a5194bdb5d5e3b42c02358ccd38e83b2b3934e2106a94900801d13f96`  
		Last Modified: Thu, 13 Feb 2025 01:53:52 GMT  
		Size: 18.8 MB (18756151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef681d107044ff66f78cc28207e7bd7091cc7e650cf794478124f973d60f0805`  
		Last Modified: Thu, 13 Feb 2025 01:53:50 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fe5b5ed5406cb918daf2171330dfc75f2871ed01659da43ebe279cccacfd55`  
		Last Modified: Thu, 13 Feb 2025 01:53:51 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49da4dd4b74c7bd9aeadf3bf142997099fb548c8b953b45d78b484f6292b62fe`  
		Last Modified: Thu, 13 Feb 2025 01:53:51 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532a902a5bcd5173f1197c05cca549dc5e755162bdbf810526944c2109fe9f7`  
		Last Modified: Thu, 13 Feb 2025 01:53:51 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c3546b10bedac2d52216e686148c3bae4b0c0e7aa70d41bc9f41b07eea9508f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 KB (59550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8a548ae7803acd1a8f49651fd7310ea14c8407333df00850ec6a127007e918`

```dockerfile
```

-	Layers:
	-	`sha256:6a7b81cdc161c7e5fbae93198fbf5f7f0a420544c6a8e686d0fef737b0edc709`  
		Last Modified: Thu, 13 Feb 2025 01:52:59 GMT  
		Size: 59.5 KB (59550 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:8309bc76f1877dcd714f32decc81dd10558e36d27e995367ab2abd65122756bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62331608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a555598814dbf0b76381cd70c9ffe679db09945624380833387fe0caac630952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 12 Feb 2025 18:05:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Feb 2025 18:05:13 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c15b6cffcfeaf0908e03140a9f7fda955710a944d05903a7bf103066454539d`  
		Last Modified: Thu, 13 Feb 2025 02:26:34 GMT  
		Size: 33.2 MB (33217967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db80d319710169fd2f48e88562489f12f1298775caf938032c5a5030685d34e`  
		Last Modified: Thu, 13 Feb 2025 02:26:39 GMT  
		Size: 6.1 MB (6125517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8ae0b63383a6290afad5c80c99c6b8b6f56bc17ac1ae75213ac0f0819fda6a`  
		Last Modified: Thu, 13 Feb 2025 06:00:40 GMT  
		Size: 1.1 MB (1133193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad1d79e202c704ba799131c0fa884fac00f8cd5c4b25cf0c7dfb89ee3a83764`  
		Last Modified: Thu, 13 Feb 2025 06:00:42 GMT  
		Size: 18.8 MB (18756075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7021bbd9bf04838277232838af67e5061ff844eaf2130248c9cf111019bf7a`  
		Last Modified: Thu, 13 Feb 2025 06:00:43 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8475ffc56a776aa426fa12ba21c66c6780b8035222a73ee84669671a9f97e7`  
		Last Modified: Thu, 13 Feb 2025 06:00:44 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f607bcda881d39ceaf0e4d678790574bd404294991f601cbf61963a2b3bb61`  
		Last Modified: Thu, 13 Feb 2025 02:26:41 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be22c699ac9834d228e41400668d0e7648702710eac9f7829b844a8fdd400d37`  
		Last Modified: Thu, 13 Feb 2025 02:26:44 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:96b32355cf8f45ca5cd374707237b7bfc0a00c2c26f8def151144b78c35dc651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6492214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a917c7f2b85cfdccae2957e98d3860226cbaad00822aa0f6b74d9c1fb4ada3`

```dockerfile
```

-	Layers:
	-	`sha256:3f5e51f04498252b8247b82cd1da6435e24c46041474345a7c542359e2d1d352`  
		Last Modified: Thu, 13 Feb 2025 04:52:42 GMT  
		Size: 651.2 KB (651207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e941e779201b830e96a319ead1f5b052cda0e57402ed237498299474e1a55c9d`  
		Last Modified: Thu, 13 Feb 2025 04:52:43 GMT  
		Size: 3.0 MB (2968946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ad7d56a448b72e9576cfddf7a04354acf806c592296b46c332f661ba5951a1`  
		Last Modified: Thu, 13 Feb 2025 04:52:44 GMT  
		Size: 2.8 MB (2812298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a14bcd0ab71a1adefdc66cb30c60a890a05721c84c751413f58eece7c14b231`  
		Last Modified: Thu, 13 Feb 2025 04:52:44 GMT  
		Size: 59.8 KB (59763 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:f0286df04605ba2a16ace26b7ac909b3a26bf5ad92da1072b39c52ca7ad25f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72226059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9647a836373dafa5e3eeda10f5d83718283263664be639fccee71acbc02b93f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 12 Feb 2025 18:05:13 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 12 Feb 2025 18:05:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Feb 2025 18:05:13 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4a8e4d7d175f2c70479d5d87ccaa5162abb41027422d3197e8a4c36fe4be8`  
		Last Modified: Sat, 15 Feb 2025 06:06:19 GMT  
		Size: 39.9 MB (39912065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1b685980568379017027aa39092cef104b5558d67b8720c9148e020b880fa3`  
		Last Modified: Sat, 15 Feb 2025 06:06:18 GMT  
		Size: 7.2 MB (7240542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa43621e11f1c173ffd382337ab22570191a3edc8349f9052f09d039caf63f`  
		Last Modified: Sat, 15 Feb 2025 06:06:18 GMT  
		Size: 2.3 MB (2322453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d96ec58a234a204a600f891cf7dbaaa44a5c76d29957b85d3aa02b64b7eb63`  
		Last Modified: Sat, 15 Feb 2025 06:06:18 GMT  
		Size: 18.8 MB (18756224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e90b14824a58d5b5f7d0886e330ee040ec31b107d1a84e008884364aa974d`  
		Last Modified: Sat, 15 Feb 2025 06:06:19 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38887d4abd7b64f90f115b988c10535cc800fec07d8a4e6bfff35c808749d093`  
		Last Modified: Sat, 15 Feb 2025 06:06:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8e1f502ea8c96658d863f37646b9895c7866628a60797223f74a0c63f8247`  
		Last Modified: Sat, 15 Feb 2025 06:06:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f0fcad9b9e38d4ea5a18b00413c5342e5c66262a1a593a08f4f992312c784`  
		Last Modified: Sat, 15 Feb 2025 06:06:20 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9bf378908790670cc4d5c16a3dc4d57e3b0ff4e4ccb9f6d9b03d39c904a8a6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6834826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2269485ed62a8152713c946c0fee1701f1844fdc465d8232be5c2d371adb90`

```dockerfile
```

-	Layers:
	-	`sha256:68273afcb3561d7009c1507aff610d0a4d141dbd0429c9292263e6067242ecdf`  
		Last Modified: Sat, 15 Feb 2025 07:52:33 GMT  
		Size: 655.9 KB (655855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c6b6c3413971e68c55ff269eacc2c6a2c19be199d42a6abd7e481564dd26e2`  
		Last Modified: Sat, 15 Feb 2025 07:52:33 GMT  
		Size: 3.1 MB (3137903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9765dc1b3f552053eeb948ea450856040c442279f1bfa14120d93b01ca1dfa04`  
		Last Modified: Sat, 15 Feb 2025 07:52:34 GMT  
		Size: 3.0 MB (2981261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999cadb4381a241b50fcc91a6bdd91d4ad886699bd8d71a01d48bb5581e46766`  
		Last Modified: Sat, 15 Feb 2025 07:52:34 GMT  
		Size: 59.8 KB (59807 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:bcf7a1ade6edbddcc15221e62b529a0d49cb38b17a0daa6f14442b03ed3332a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64329548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9670a78194ee44e4324dab7fd2959c53d3a83eff2ea16706cf10d6f80fbf4e16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 12 Feb 2025 18:05:13 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 12 Feb 2025 18:05:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Feb 2025 18:05:13 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47798aeb6f93acca9d5bd6a54fcaaf65869abba6ff592821b08ace8ecaa579cc`  
		Last Modified: Fri, 14 Feb 2025 20:36:58 GMT  
		Size: 33.4 MB (33369840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d281aa66fac0d1de907562bb8ffd53b2afc17ad462f716e64a69f436e4628056`  
		Last Modified: Fri, 14 Feb 2025 20:36:56 GMT  
		Size: 7.5 MB (7509155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0457533f3ffd7d08431d7cd65122557166f945c42a8ecbb631022f314d49a39a`  
		Last Modified: Fri, 14 Feb 2025 20:36:55 GMT  
		Size: 1.2 MB (1229224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f531b97b3977294f76f9caa050aac66eb5edc756a4057134da9c70e749dbabe5`  
		Last Modified: Fri, 14 Feb 2025 20:36:56 GMT  
		Size: 18.8 MB (18755965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ad0833ceb4437b6682254a393f8e591a9d729a036f87ba0cb3554000a28065`  
		Last Modified: Fri, 14 Feb 2025 20:36:55 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8346918c2da303ae53d761d98b0c4663d7b1cba142ed3a4dbe06d238b304be`  
		Last Modified: Fri, 14 Feb 2025 20:36:55 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8920335ef908a226ccd1cddad2e03861dbc467401c6ca3bf899a956a0829d592`  
		Last Modified: Fri, 14 Feb 2025 20:36:55 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f262bad3f1471951b3db84b0e594e903c92d21a80d91dfc680c2791e72616324`  
		Last Modified: Fri, 14 Feb 2025 20:36:55 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:dfbeabc0583b974a003450e59f2b9073d555cb7bdf2022b69da685a86cf90996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ca0f19566430ec3d3b8926f05730b1c487b85b74f17242bc1bfec7ee973d0c`

```dockerfile
```

-	Layers:
	-	`sha256:b0d99b1c231a2b7b3f8e7780fb53327cea401a7e39b7ef69e2f39d35b63d5321`  
		Last Modified: Fri, 14 Feb 2025 22:52:34 GMT  
		Size: 533.3 KB (533308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594c8323ecd8c68223344e45f7f0801d66d2b1934e8140ea464def9d3a54a5a9`  
		Last Modified: Fri, 14 Feb 2025 22:52:34 GMT  
		Size: 2.9 MB (2920926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8351ba44c5ca707e5603c30d289f82f398bdc759881c2c2da44a350aee7bfabd`  
		Last Modified: Fri, 14 Feb 2025 22:52:34 GMT  
		Size: 2.9 MB (2916738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afcafae1a63ad0fde215376828a87bbc4f622c3c3fd5e03052539eafcfd062e`  
		Last Modified: Fri, 14 Feb 2025 22:52:35 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:74b10a036f4d7ed544c0a5db8229f6b0ca2fb1e2ba37c2fa3f396530a78f49b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65430267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0455ea9914e3595282e0e5c3c504072cfa92b0a02a9a5c99e832e94b86942e4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 12 Feb 2025 18:05:13 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 12 Feb 2025 18:05:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Feb 2025 18:05:13 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3681c4b6a9cd189feb4437c2fe33c659230f8f5add55562d6fe3d40bdafb3f`  
		Last Modified: Sat, 15 Feb 2025 01:08:53 GMT  
		Size: 33.7 MB (33749260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f67f0c2a02f34b4c86783d6a33e63a31b8b7cb1db22837862d625b0afe5b818`  
		Last Modified: Sat, 15 Feb 2025 01:08:57 GMT  
		Size: 8.0 MB (8003846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907eedd9bc6565c47d34b16eb6567ce3e84e09b7cea6af949fe1199f77be9e1f`  
		Last Modified: Sat, 15 Feb 2025 06:00:34 GMT  
		Size: 1.3 MB (1344976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1634a715aa088328342dbd2b68c3edf22cb5dd70ac46e8f773ebeb26085c04`  
		Last Modified: Sat, 15 Feb 2025 06:00:36 GMT  
		Size: 18.8 MB (18756092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f567a2505d96a4c05f435bee822033c0485a53258c4786e0540eeac286d02838`  
		Last Modified: Sat, 15 Feb 2025 06:00:38 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef296aad48c40a026d724f53808b658e92aeb24f6280469a06eba32136057e96`  
		Last Modified: Sat, 15 Feb 2025 06:00:38 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91eaa663eda3ab488c9f47c68790b313f3fac2709d60485f516fd6ae78b89c27`  
		Last Modified: Sat, 15 Feb 2025 01:08:59 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95dd85fde6afbcb6a6f0104296d02574d89203a28325d36bc85a2aa0f6e20a7`  
		Last Modified: Sat, 15 Feb 2025 01:09:01 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ef1831b86bfa043377236e5d241852ce2d6145438f29b222bf98e381ddfa99a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6730519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b801b5ec3b3ee1fe9cf6ab71077c4bd766280da9a5ad6b342f0faff3541bfa`

```dockerfile
```

-	Layers:
	-	`sha256:82e2cdc4ababec1685e18b6caaae5279b138278a084b7d27883cb1542b103254`  
		Last Modified: Sat, 15 Feb 2025 01:52:32 GMT  
		Size: 649.3 KB (649262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8775c1946dd2110fab45b2d38e4a6a667768de07c06c1a691a69f6c28a6fdee3`  
		Last Modified: Sat, 15 Feb 2025 01:52:33 GMT  
		Size: 3.1 MB (3089138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:765887d530c3dc8212666bb24f8bc12da5a22a290e53571e9174f86434798241`  
		Last Modified: Sat, 15 Feb 2025 01:52:33 GMT  
		Size: 2.9 MB (2932484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5ca15ae705307717e640753d24d3fdd459c8dc28d7956403050a10abccfab9`  
		Last Modified: Sat, 15 Feb 2025 01:52:33 GMT  
		Size: 59.6 KB (59635 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:60363432edc81be0022459dbe7c1ce1a404a77a86be3004ad436da271626d03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66833174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a0b6ad6c6bcc2ab7bf376e4134b03711301e51432ac769adf58ab11b7e4ed4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 12 Feb 2025 18:05:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Feb 2025 18:05:13 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb85317daf7aec761283406b99d1c26fd2b58a68a7c0647d8703d986a2ccb7f2`  
		Last Modified: Thu, 13 Feb 2025 03:29:24 GMT  
		Size: 34.7 MB (34699459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138c62dd8e5d4cc3eaaaf11cdab1bf0134e66196a0665c1a992a92913b76ee06`  
		Last Modified: Thu, 13 Feb 2025 03:29:27 GMT  
		Size: 8.8 MB (8760507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0d5d12ebc6f768d05d2cf2ea887770122eaf2a423ad4d523cc47830f43d3c4`  
		Last Modified: Thu, 13 Feb 2025 06:01:18 GMT  
		Size: 1.3 MB (1265035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c7a60538a0b0d8395a2a8703e5d8d1434cb2cd17ce0ea45655075e166c65f5`  
		Last Modified: Thu, 13 Feb 2025 06:01:20 GMT  
		Size: 18.8 MB (18756164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3faf529b65f862b2796f1c8f875428ed47677a150fc3265e0ce92ce151c4694`  
		Last Modified: Thu, 13 Feb 2025 06:01:21 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ae598f93a232e9a775615003c3eb36a8dd9ab35dd256112bcee7a57a892372`  
		Last Modified: Thu, 13 Feb 2025 06:01:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891b19ca242b277c70d732a12f4e200c782a044b396f49beaeadad8fb1de7ac5`  
		Last Modified: Thu, 13 Feb 2025 03:29:29 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a937092a3b61f875bab8438ae6f6c37d8a460a3bc67b8ef7bca61a91a6c7a4`  
		Last Modified: Thu, 13 Feb 2025 03:29:31 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:30fb089fd89338b14757fd44790725bb49816bf7d43466713ea0b6a71387de4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6808616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c9ac14140f656d2ff1c66d5b8b763f8e8d62395dae33e69f7cf7aac5c775a7`

```dockerfile
```

-	Layers:
	-	`sha256:cd461455b305dd3edec9d5dcd4f11e1b8c504427f2cc653893e26e8c6d469620`  
		Last Modified: Thu, 13 Feb 2025 04:52:56 GMT  
		Size: 652.0 KB (652048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72bf0be8d50dc6d04a4816a42f1e1e7e0aa47e05339f1fadf8459f140c037a03`  
		Last Modified: Thu, 13 Feb 2025 04:52:56 GMT  
		Size: 3.1 MB (3126787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009375a190e636d59fec87070669002a42ec4966c6c621d717b64090ead76812`  
		Last Modified: Thu, 13 Feb 2025 04:52:57 GMT  
		Size: 3.0 MB (2970145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd66b4a6b76781cbccbfa018054a19ea8c31b4fc9fc3e794191e38711c8d2901`  
		Last Modified: Thu, 13 Feb 2025 04:52:57 GMT  
		Size: 59.6 KB (59636 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:ca95fc8f533fed67e2a68709f4fccfb8aacf58e4381598a56aae39573168490b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64071378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70ac545d49ac2c78c7581a7bd6382279081038ccc2ac15ea312ef3a0579364b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 12 Feb 2025 18:05:13 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["/bin/sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 12 Feb 2025 18:05:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 12 Feb 2025 18:05:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 18:05:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 12 Feb 2025 18:05:13 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 12 Feb 2025 18:05:13 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Feb 2025 18:05:13 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Feb 2025 18:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Feb 2025 18:05:13 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 12 Feb 2025 18:05:13 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb9fe9456bf501a451fa193653d6a2ed4885efee72c30e37403245fc616347a`  
		Last Modified: Sat, 15 Feb 2025 07:10:10 GMT  
		Size: 33.8 MB (33777435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b08644cebc9de39e6fb741fcbb5f8d40c22bc4427b61cf9efd49d3c0916cd`  
		Last Modified: Sat, 15 Feb 2025 07:10:13 GMT  
		Size: 6.7 MB (6745385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c178fb67667e2a5ec671789fdb6f54be1a07ef2680ff605dade251e1ef5bb2`  
		Last Modified: Sat, 15 Feb 2025 07:04:18 GMT  
		Size: 1.3 MB (1323210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32465d4719cab536e3189a3c9268311c3a1497e696ac0f9bc92449349bc7c05`  
		Last Modified: Sat, 15 Feb 2025 07:04:18 GMT  
		Size: 18.8 MB (18756031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7559da4fbfa28bd83dbe1c065086d9dcd0ba88eba0f8d573061dacf2b8f116`  
		Last Modified: Sat, 15 Feb 2025 07:04:19 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29ae9dae5aaac91703ad57a4b2a635e1e7a79be13ca876bdb0802e67f3f8432`  
		Last Modified: Sat, 15 Feb 2025 07:04:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac72ae0427bd9a94c8e176ff9138922c0cd7392efa3bbc2574cbcac0fbde43c`  
		Last Modified: Sat, 15 Feb 2025 07:10:15 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0012b5f6e02bf62169b4306e96a22b65a11fb5a663148bad0cb526c8379c52`  
		Last Modified: Sat, 15 Feb 2025 07:10:18 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7c87762fb43fff427f0bbeca9ae94c556ec8ead981335396404f240a7103e836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9983329fcd3b88cb33ef11c75bfd3275c3e942c9c40da1702a8c88a02afb1bf4`

```dockerfile
```

-	Layers:
	-	`sha256:f43e66207a4cf296bcea80a900da691a45d2ca852447ed79424fb47f4f6e28ea`  
		Last Modified: Sat, 15 Feb 2025 07:52:46 GMT  
		Size: 649.2 KB (649234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef87736d434bb5b4c1bda648a4eb3e4f1f423bb375f45b145d385307c60ad026`  
		Last Modified: Sat, 15 Feb 2025 07:52:47 GMT  
		Size: 3.0 MB (2979111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b03c608e79c0639704a03ab608be5d167d78bc48afd40bb2e73a3a7ff471f2d`  
		Last Modified: Sat, 15 Feb 2025 07:52:47 GMT  
		Size: 2.8 MB (2822487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42006bb48b46dd38b3a51886f5c8dbea0aff3634b388f7d052c90313b006ca3e`  
		Last Modified: Sat, 15 Feb 2025 07:52:47 GMT  
		Size: 59.6 KB (59580 bytes)  
		MIME: application/vnd.in-toto+json
