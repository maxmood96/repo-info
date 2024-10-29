## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:b918bbf5bc9a50f6b863130f961e0da66d799ab0f3a5f857bf24982fada40d5e
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
$ docker pull rabbitmq@sha256:e9cf0f03254dee0b29608b0512b1104b552a5e6ecefc501a9ddfb59192e96382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74057441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee906cd58847d48059674b54f4e811697149b8272e332409c279c3f12977ecdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 21:23:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 28 Oct 2024 21:23:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 28 Oct 2024 21:23:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_VERSION=4.0.3
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 21:23:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 28 Oct 2024 21:23:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 28 Oct 2024 21:23:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 21:23:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 28 Oct 2024 21:23:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c89b37eb3f8fb56387d6bfe62a3c521e49728f4bdafdbaa497be9c2b221877`  
		Last Modified: Mon, 28 Oct 2024 23:11:49 GMT  
		Size: 41.6 MB (41579817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6ec4ab7713fa60572d36cab17ce28aeb7312ceb2506646d1c69ae391445eec`  
		Last Modified: Mon, 28 Oct 2024 23:11:49 GMT  
		Size: 8.3 MB (8284886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e966f077a736c075145a932a3a357e8bd1ecfc455474f8b14624cec6019249`  
		Last Modified: Mon, 28 Oct 2024 23:11:49 GMT  
		Size: 2.2 MB (2234335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d851dcb0d8a20f786d822cfb317e567ec66d3a24d5c0f55f755580f42d5c5412`  
		Last Modified: Mon, 28 Oct 2024 23:11:49 GMT  
		Size: 18.3 MB (18332850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7c1bd086bcdd2b6e00add2bf11fbc1ee62fbce24f72b1d0887f53076eba8ab`  
		Last Modified: Mon, 28 Oct 2024 23:11:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88ab35b4d3f979269a9174d2f47f18ea04a42b65c2d055adf3f385139dd3b2`  
		Last Modified: Mon, 28 Oct 2024 23:11:50 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc11a9f8f9b5ef2f24f2a7d3238509b4ec16f028d1a4b7ea6e431e8cdb60ace8`  
		Last Modified: Mon, 28 Oct 2024 23:11:50 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41be1fd29e1ea33c45b750456d4483925b06b2c1c778fb8ee099df18ca3aafb7`  
		Last Modified: Mon, 28 Oct 2024 23:11:50 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7ebf14dae2081e2c53ec549910737b03e17491c0d5b4e7822048f25b99e4fffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6455913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8ba4cba48e7efcb8f0a50ed48b9d854c2606d0017cf5f252eee885ce5cfaec`

```dockerfile
```

-	Layers:
	-	`sha256:bbeadf32f319aeca74164efbfbd87416fb4cae29f01706cc1f87d68a739c1398`  
		Last Modified: Mon, 28 Oct 2024 23:11:49 GMT  
		Size: 652.9 KB (652933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fc71a35b09d7fc4d5d8e1742dbd4b6fad5298e1f909f7618a3107e8c7cabe9`  
		Last Modified: Mon, 28 Oct 2024 23:11:49 GMT  
		Size: 2.9 MB (2948875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07cd4d24752bc390c178990d535d7a53b8ccc340b7087936f66a5d512cb04263`  
		Last Modified: Mon, 28 Oct 2024 23:11:49 GMT  
		Size: 2.8 MB (2794406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81abbd6d1433635439730aa53b4f3c7541231edcd93ffca53f6e4173a01e9478`  
		Last Modified: Mon, 28 Oct 2024 23:11:49 GMT  
		Size: 59.7 KB (59699 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:0d84eece596ec14d31809101b7b128fcd22b9cbb9f81923ab36da429a145964a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63207709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d40864749685754d9720f2d60b236d910407c7e3900c4d5744bfc6bb8953da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 21:23:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 28 Oct 2024 21:23:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 28 Oct 2024 21:23:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_VERSION=4.0.3
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 21:23:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 28 Oct 2024 21:23:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 28 Oct 2024 21:23:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 21:23:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 28 Oct 2024 21:23:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed534a69666bd022097e876968b2ab66b463d0be3df4d7a61cdadf3e699f4930`  
		Last Modified: Wed, 09 Oct 2024 23:02:25 GMT  
		Size: 33.2 MB (33196705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eff7390bbe7c995763ffdc9d2291fe825e45188f9c74da10eb086693e66623`  
		Last Modified: Wed, 09 Oct 2024 23:02:24 GMT  
		Size: 7.1 MB (7079928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1b129092755c094b08e0e8eb9f420e3aedbcc5c997b01086238adf06e015c6`  
		Last Modified: Wed, 09 Oct 2024 23:02:24 GMT  
		Size: 1.2 MB (1230053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4fb78bc69567c02cbcbe43e34deb1a501b75c4c26727424835a2d89a4d0b56`  
		Last Modified: Tue, 29 Oct 2024 01:06:28 GMT  
		Size: 18.3 MB (18332773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8450399f510a8a8892bff243cb1f9a94a456914518a61507cbe14bfed595da6`  
		Last Modified: Tue, 29 Oct 2024 01:06:27 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f6759cb32e2e709b7bce30903ee5450a18332fcee3816c28ff0bb44a83a2ba`  
		Last Modified: Tue, 29 Oct 2024 01:06:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43c6072e14544b58e4d06daa46bc47f3fe7111978000adce122e5083b81722f`  
		Last Modified: Tue, 29 Oct 2024 01:06:27 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0570e84a2018556654eb9cf8095ace10850f8c2a58e205efae693b203fa8b011`  
		Last Modified: Tue, 29 Oct 2024 01:06:28 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6e3e56fbad1f71305e2c0a48e819e4a7daca1db681369ea3c6264aca4b922765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 KB (59671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff6d837ceb9a23df13f24f6390722a71d36f359d1941353078160f0b886f488`

```dockerfile
```

-	Layers:
	-	`sha256:02adae05a21c831e8545ac82e53f4382c39182292de4f357ec9984ca0eed0caf`  
		Last Modified: Tue, 29 Oct 2024 01:06:27 GMT  
		Size: 59.7 KB (59671 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:0af94b827fe89da152c76876b7370ec45ce27f7ea35b80778355636a816db030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62371793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558d0b737a5398e65c17099e14b72e5ff3eb3891f1520f18255e62046718e33b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 21:23:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 28 Oct 2024 21:23:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 28 Oct 2024 21:23:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_VERSION=4.0.3
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 21:23:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 28 Oct 2024 21:23:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 28 Oct 2024 21:23:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 21:23:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 28 Oct 2024 21:23:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1f67f28e10afeeb5df7b753ce3c23c80e4e4ae97ea19ca8709eaf48c068734`  
		Last Modified: Wed, 09 Oct 2024 23:10:27 GMT  
		Size: 33.1 MB (33092591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5bb9d41ac48da80a09bcb8fa50d5dcef44144067bd047330d564dc74e86ef`  
		Last Modified: Wed, 09 Oct 2024 23:10:26 GMT  
		Size: 6.7 MB (6716586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f58409d17f8213ead54ed35d31298ac48b082e7d85b04e8db73806bb292cee7`  
		Last Modified: Wed, 09 Oct 2024 23:10:26 GMT  
		Size: 1.1 MB (1132947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42e1690609861770fa56b01803b9540b31ed1f1470206f02e986e42a5882cc8`  
		Last Modified: Tue, 29 Oct 2024 04:59:45 GMT  
		Size: 18.3 MB (18332426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8118f62e46040738e5d0871a5aecc6cf598a1e581242c693b7fbb3139c9477`  
		Last Modified: Tue, 29 Oct 2024 04:59:44 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d9a6c3250ae31386769daffa06ccbdba2fd60d72d6fde82801a4253e2f8af`  
		Last Modified: Tue, 29 Oct 2024 04:59:44 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0f6b981f5964c91266a6fd69acc0373b97cf4dd005ec7d4b7a2af84d310e98`  
		Last Modified: Tue, 29 Oct 2024 04:59:44 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416d865493d3abda83875fb8380cac6b2ca98e5fba1c2478146f6549cca22ab8`  
		Last Modified: Tue, 29 Oct 2024 04:59:45 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d80148f337a2031e853518b2f8600aad3853458f107de4450c55edf6255dad88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc3444af9be026fcb1dcca4dce3a60e5d56af4652010a99c82e483fd63b07c1`

```dockerfile
```

-	Layers:
	-	`sha256:73274cbe6b2aeb39e41ad7e0f45b28357619b72ea8abc39dac3376d0f776331e`  
		Last Modified: Tue, 29 Oct 2024 04:59:44 GMT  
		Size: 649.0 KB (649004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8b2668009e955d9969296aa45d0d73015766cb6000a9d4a006af4280fe6acb`  
		Last Modified: Tue, 29 Oct 2024 04:59:44 GMT  
		Size: 2.8 MB (2848415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d7f38f92898d9d59dbf6d4fcaad4b123e014b294a1719992bc8b68fe0bf140`  
		Last Modified: Tue, 29 Oct 2024 04:59:44 GMT  
		Size: 2.7 MB (2692615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae326b0e2284727f58654d7010938f4ac2144a561e2ba97ee782b4456d62cb4`  
		Last Modified: Tue, 29 Oct 2024 04:59:44 GMT  
		Size: 59.9 KB (59886 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:da055328473269139022cea36c6159f03c281095c5eab70e05550f8379f3d709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73409224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ca00e1598c2d8ae00317a43d93815e227d711c22e5995cf917fb86bf6fdb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dd0fedca3a17179cb65d292514d9e5e38984126a794fb25c2d90ee8f939395`  
		Last Modified: Wed, 09 Oct 2024 23:13:25 GMT  
		Size: 39.7 MB (39693537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a0adb5b179620c713a2a9b89c503d480e94a60a3a427991cb9e46682773e29`  
		Last Modified: Wed, 09 Oct 2024 23:13:25 GMT  
		Size: 9.0 MB (8995937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d29ac149ba8ca99d18911526655bc8fafce02694421047863c8ab60662577`  
		Last Modified: Wed, 09 Oct 2024 23:13:24 GMT  
		Size: 2.3 MB (2321280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4211b0e014272175b221a29d61bf36ed1628843001724f9bf560bb05fe38ce60`  
		Last Modified: Wed, 09 Oct 2024 23:13:25 GMT  
		Size: 18.3 MB (18309082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a8ec127ba82cd312ee55b32313c240cbf84a9e664f97716b0a4c9479d1495d`  
		Last Modified: Wed, 09 Oct 2024 23:13:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4edb406e2703dae7e096fc8673f21e697d78285cb7241d75f6489f5e7ee1b54`  
		Last Modified: Wed, 09 Oct 2024 23:13:26 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2277919ec4d5f6bcaa61716fa3897423806b24ad8183754fdb9ee951e4182c`  
		Last Modified: Wed, 09 Oct 2024 23:13:26 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89978ebd6e4f3e52f38345cd200fd0987530423d39b1dc59d8899a251b6570fd`  
		Last Modified: Wed, 09 Oct 2024 23:13:26 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a621a17f9c5b69db0629614b4b3cf63f4c9ef126d1da2bf6f08b74cfcd11c390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6462150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68400a92ed91391e24ed32953a270116a62804f103f18851856496dc6c49e223`

```dockerfile
```

-	Layers:
	-	`sha256:64a0ecacc717881b7c9e711858d34237bd8cb89c172bf99fae6b0d68d30f51c7`  
		Last Modified: Wed, 09 Oct 2024 23:13:24 GMT  
		Size: 643.1 KB (643140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3d926d9a54ff53a7f8fef14ddd2cfbc2aec9c287dc8cbc5dca42233649969b`  
		Last Modified: Wed, 09 Oct 2024 23:13:24 GMT  
		Size: 2.9 MB (2948865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3909ec74df18bbb3b32aae4d09f7e6b48c56e3bce491871461d7b0ad664a00f2`  
		Last Modified: Wed, 09 Oct 2024 23:13:24 GMT  
		Size: 2.8 MB (2810243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88fa5eb61623aa590b6e4e8c4a46e5f7230e0715d43a5544d1e0758087c15bda`  
		Last Modified: Wed, 09 Oct 2024 23:13:24 GMT  
		Size: 59.9 KB (59902 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:b4959eebd0119caf8994a423fc314e1b000f47a517de55f446623b6cae0d9ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64719996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bccde37636ca39a507a3472a223ff88dc99d99c50e3baffa8f18b0612e6663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 21:23:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 28 Oct 2024 21:23:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 28 Oct 2024 21:23:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_VERSION=4.0.3
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 28 Oct 2024 21:23:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 21:23:50 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 28 Oct 2024 21:23:50 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 28 Oct 2024 21:23:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 28 Oct 2024 21:23:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 21:23:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 21:23:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 28 Oct 2024 21:23:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512fab11d96859bb224fabe40d84a01e75905114a5b87b74c0a4e254ad0602d9`  
		Last Modified: Mon, 28 Oct 2024 23:16:36 GMT  
		Size: 33.4 MB (33360051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433be84c18ed7067625f74980e99edffe600340eb3fc53d63c82e1d0343efe3f`  
		Last Modified: Mon, 28 Oct 2024 23:16:35 GMT  
		Size: 8.3 MB (8324910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0305bf029565893dcaef71a90c3e84294a207e6621af4d5a8f9591685cd29321`  
		Last Modified: Mon, 28 Oct 2024 23:16:35 GMT  
		Size: 1.2 MB (1231494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecee364bfd7c625db54aef676573266713eb8675d4b90798c46e7985288c627f`  
		Last Modified: Mon, 28 Oct 2024 23:16:36 GMT  
		Size: 18.3 MB (18332629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e677f015713526dd8ed34da746510599c4cf7220fa6c8b4ca243264ffc0a27`  
		Last Modified: Mon, 28 Oct 2024 23:16:36 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e67ceba0f5b5848cd45bcdc09bb1867ab70a722df5681fbb6379bc47b93a20`  
		Last Modified: Mon, 28 Oct 2024 23:16:36 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e2846c831446a46a466fb845b55da4cd3f7773eb573e5be6f22ebe01de2755`  
		Last Modified: Mon, 28 Oct 2024 23:16:37 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a036713907dbd53dfd8b5fe7eacdded0dfd98c1105629e8dd792c3131443bd`  
		Last Modified: Mon, 28 Oct 2024 23:16:37 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ad0c1a8c856d88c6ddb4d6c7c0ded7ace1d97cfad2b170c9573441f70d51f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6431578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9503c80b996ca700e4a073143b48969a3bebbdeba33cc29e57b111faf229e7e`

```dockerfile
```

-	Layers:
	-	`sha256:ee64c4b63bc90c465f3f1a0858181cfe743dbf514021965d3776eeac97640149`  
		Last Modified: Mon, 28 Oct 2024 23:16:35 GMT  
		Size: 648.2 KB (648205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5fc8312b488c4a38f413ca7bb3fcb71f2b4889e35a781d1aee505d5cfeda247`  
		Last Modified: Mon, 28 Oct 2024 23:16:35 GMT  
		Size: 2.9 MB (2939093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d35521e62b3d1bcb6595216ffed2fb6534ff129c852b6b1ef77ce6d749ce1e7c`  
		Last Modified: Mon, 28 Oct 2024 23:16:35 GMT  
		Size: 2.8 MB (2784628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d2174507c513cc2d4c98c8661c6e2d1e1fa17485023f6205994e3d7ae5bc8eb`  
		Last Modified: Mon, 28 Oct 2024 23:16:35 GMT  
		Size: 59.7 KB (59652 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:861e72333537b01f5210c96d299fdff93efb6ffa492e9233681e98996851e79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65682194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cddda9df9c038a90138c505cb1b018efb6d051ee1b6740ae9e8963dfe70d6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c3725fd5f7e57bc4f1a96f26eb2059163ea872bc99ce3b7e95323e120196f0`  
		Last Modified: Wed, 09 Oct 2024 23:07:09 GMT  
		Size: 33.6 MB (33619115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f1da942a53dc6c8e0ca86a5e6d5923f854652d8006323e22e238ff1bcc04f7`  
		Last Modified: Wed, 09 Oct 2024 23:07:08 GMT  
		Size: 8.8 MB (8834111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bcf4da01d6bdf49a1a973b4ae84b89efb8a395cbc74ca213d48f8edb78dcc`  
		Last Modified: Wed, 09 Oct 2024 23:07:08 GMT  
		Size: 1.3 MB (1346113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be35d6ad5aa399be7bdc55716f2e6f89bf9514e0538c89eeea691def70053d1`  
		Last Modified: Wed, 09 Oct 2024 23:07:08 GMT  
		Size: 18.3 MB (18308684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f26e793c557c8e891bd1630a0e15eb0e1292404c9557b61d44b87eb6ed7e50`  
		Last Modified: Wed, 09 Oct 2024 23:07:09 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a3a2fae83d1e64e99b86b39dd587f9c091b8791fccbe0299b2d1c56393be65`  
		Last Modified: Wed, 09 Oct 2024 23:07:09 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6f3d5cfcdea77fe3859734d11531b5208e18ce49b1b1d80b3d41092d94f04b`  
		Last Modified: Wed, 09 Oct 2024 23:07:10 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eca6ee6b2a0d8307f3c2ad143128b1ef711e2092154beb078621c12b011f544`  
		Last Modified: Wed, 09 Oct 2024 23:07:10 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2f6e5da83622097e617b0a912be5e4f5799a9fbadae839bd8f7ef95d7aef588a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85e6e2e8972a5e247dafa20beab54bbd31594ff15a837d1803a0a5e7e7f1bb2`

```dockerfile
```

-	Layers:
	-	`sha256:ad2fb4b7385209fb73c77e69ef6180bff212535e7381e9003e48e69ad943d373`  
		Last Modified: Wed, 09 Oct 2024 23:07:07 GMT  
		Size: 636.5 KB (636461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74c226ff72dc687c433e39fe1bf52e71b0493b1475b572c638250e128b27c21`  
		Last Modified: Wed, 09 Oct 2024 23:07:08 GMT  
		Size: 2.9 MB (2921343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdeb15ffc3d62d3374285bca5f6dbbadd475f1e1a57c71177f405991b2a72e22`  
		Last Modified: Wed, 09 Oct 2024 23:07:07 GMT  
		Size: 2.8 MB (2782709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3deddac317f6addea19ade1a02ec683b755bef25da7cf2f0ef6260c01c94c9a2`  
		Last Modified: Wed, 09 Oct 2024 23:07:07 GMT  
		Size: 59.7 KB (59726 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:d4c2d5247a06a2fe699af7fbad24b806c2b9ec541c2455776c80943c04289a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67397258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d15122d2d6007ef95ff92a6bb086c6245a994658b4fd215eb08e7c759a8c4dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cb7009e10a8373603194c86e272035a9e7a0dbefb7c7861625a3a1ba9d2dee`  
		Last Modified: Thu, 10 Oct 2024 01:35:07 GMT  
		Size: 34.6 MB (34577584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1109d7df9129e6afafd5d03ef57f307fd040222d78e4d0b84f2faefaa26854`  
		Last Modified: Thu, 10 Oct 2024 01:35:03 GMT  
		Size: 9.9 MB (9866563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e60063055b8b0eb14d51996060e0937f12d29664fadae40e9df2eec1b2cc61`  
		Last Modified: Thu, 10 Oct 2024 01:35:02 GMT  
		Size: 1.3 MB (1270917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dd1f31c02b979593b87af4ec25b087a75e8c0b2f6a11ca7e7f3ebcd1b89776`  
		Last Modified: Thu, 10 Oct 2024 01:35:05 GMT  
		Size: 18.3 MB (18308993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6995c3cbffda65dc578c1842e39c23b86a35b1fe7ee6986a9cc8b8d78d9371e5`  
		Last Modified: Thu, 10 Oct 2024 01:35:03 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6488b53c20f1bb05d8d5675ae992f441e7e96f1d7979959d2f8a5adb89a6e2ca`  
		Last Modified: Thu, 10 Oct 2024 01:35:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e13e72ad6b6751f51f8436273c6da1325bca65327268a5a66c3dbf808b70e27`  
		Last Modified: Thu, 10 Oct 2024 01:35:05 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f34543b104eacd4df0c20d1699adfcc9a0506f9cdff92966319c776ef56c7da`  
		Last Modified: Thu, 10 Oct 2024 01:35:05 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3dbed965392b91b25a0109d1aa1eeb9493cd521d87710be0678cb225eae19f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6435340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ff5f02a189d2a7db5670ba821fab6344181faff1c364afe8d104537a1173ed`

```dockerfile
```

-	Layers:
	-	`sha256:65b7bd5d5daa5fc5f542bb36d155ecc19c3f57f7e75e5e196547bc7eee5ae655`  
		Last Modified: Thu, 10 Oct 2024 01:35:02 GMT  
		Size: 639.3 KB (639304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f00e83cffbf46790451894a872c56a5afb812c3939b96e8893f7e00a9c6831ca`  
		Last Modified: Thu, 10 Oct 2024 01:35:02 GMT  
		Size: 2.9 MB (2937466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990300e9b74f4c9d1691a87d7f8d4f4c892bc69034adf69cdfefc6eba142d1ab`  
		Last Modified: Thu, 10 Oct 2024 01:35:02 GMT  
		Size: 2.8 MB (2798844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3acc3558956b8e7b60070fc3f0d00df6c7ba0200dfc1440f0ff1ffc51d34ea`  
		Last Modified: Thu, 10 Oct 2024 01:35:01 GMT  
		Size: 59.7 KB (59726 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:4cdd9808798c96ac3286cc6de8055d9e30c9960059218199d49585ea4ab29657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64270195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a14d7ccc65aed94375dbefbf16b11b90568e0bf7bc07a95b93af1f85ef3a8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 09 Oct 2024 11:34:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_VERSION=4.0.2
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 09 Oct 2024 11:34:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 11:34:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 09 Oct 2024 11:34:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 09 Oct 2024 11:34:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 09 Oct 2024 11:34:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 11:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 11:34:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 09 Oct 2024 11:34:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b045940514f9cfd17b1037a792b5167041c3475400b7ccaa5c1bb0bef2bbc9`  
		Last Modified: Wed, 09 Oct 2024 23:10:07 GMT  
		Size: 33.7 MB (33690961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adc1031e8a15301a663696d51b3dd38581a5d4e618510411c0ed38b7c795386`  
		Last Modified: Wed, 09 Oct 2024 23:10:06 GMT  
		Size: 7.5 MB (7481820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516480edf240888d77ca795cd0c38729b3e62520a347721e4ec4614f3be8b542`  
		Last Modified: Wed, 09 Oct 2024 23:10:06 GMT  
		Size: 1.3 MB (1325185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ce251c770ddbc6f339850df632d122b195546f01e11f0726675fd9aac9b06a`  
		Last Modified: Wed, 09 Oct 2024 23:10:06 GMT  
		Size: 18.3 MB (18308878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472672ea75ebdcf9ed582b1ad12cb1bd103f59db94d19beb8e1696f3c4cf1cc4`  
		Last Modified: Wed, 09 Oct 2024 23:10:07 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f60ffe4ca0a38013f02c57ad679eb45a95a71da71a4cb9d96269a3e45d833ad`  
		Last Modified: Wed, 09 Oct 2024 23:10:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760595f46b4cbd011585d9fc4497441c19ac620a29c4626ba86e26248e001f9d`  
		Last Modified: Wed, 09 Oct 2024 23:10:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5ae32a2189685eb95be3e146e0089c8d0e123433b6832898075ec23c70720`  
		Last Modified: Wed, 09 Oct 2024 23:10:07 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a7a153cfa4a0a9bb204f7e6e8fd3fbe432a22df48c0f6a71c1e6495c7ebbf670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6234285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe4a79c9b9f8d6752b9dd424ebfd6fc1ac217625abf46fd95021e8bbe98b239`

```dockerfile
```

-	Layers:
	-	`sha256:7c5c25800412bd28f232d4c5779704c1022d15cb202450cde3682c140c51f75e`  
		Last Modified: Wed, 09 Oct 2024 23:10:05 GMT  
		Size: 636.4 KB (636427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8a2a91d0afd3a2ea3c55243d8eac03c23c4e2bc096cb342649381f582b6fbd`  
		Last Modified: Wed, 09 Oct 2024 23:10:06 GMT  
		Size: 2.8 MB (2838396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ef8248f14353f682e3bbb0f855bd913bb788af5cffd379276e4566b3a8d0f34`  
		Last Modified: Wed, 09 Oct 2024 23:10:06 GMT  
		Size: 2.7 MB (2699792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7253e6678556d67160a03624a29254bc0d83be96c42421b3738ea9565bdef186`  
		Last Modified: Wed, 09 Oct 2024 23:10:05 GMT  
		Size: 59.7 KB (59670 bytes)  
		MIME: application/vnd.in-toto+json
