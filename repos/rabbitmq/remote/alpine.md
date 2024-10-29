## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:9ee4c5b80010e22260018adb61312550dc0a37aa20cb74488de8baecc9f37fa2
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

### `rabbitmq:alpine` - unknown; unknown

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

### `rabbitmq:alpine` - linux; arm variant v6

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

### `rabbitmq:alpine` - unknown; unknown

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

### `rabbitmq:alpine` - linux; arm variant v7

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

### `rabbitmq:alpine` - unknown; unknown

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

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:3dc2608f43fb184ac02c7d0c29b2ec6a63283cbf560e4ba9cd292e12abd51f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73433148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e97e4b7d01441dfa7b3c1ef2dd0521d866033389e989fc7e911daa904932db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cdca88f4a2ba624db135fc97dc5dcfda94c25c5148e63fe07edb15b8a46595`  
		Last Modified: Tue, 29 Oct 2024 05:54:11 GMT  
		Size: 39.7 MB (39693751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb875533b102d39982ccbe0a61f52c23c9853958ee38ccdbc9a31e0878435049`  
		Last Modified: Tue, 29 Oct 2024 05:54:10 GMT  
		Size: 9.0 MB (8995914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843d028fae0e98ee66b79d3a36736047b9a3598824ce80a37cf9d8798b29beb8`  
		Last Modified: Tue, 29 Oct 2024 05:54:10 GMT  
		Size: 2.3 MB (2321297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c4eba14111760c40af434f5b3aa799181159ae4573f3608327e6f7899f274`  
		Last Modified: Tue, 29 Oct 2024 05:54:11 GMT  
		Size: 18.3 MB (18332792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d909a05dd9c2c68e623d4ac93ff4c8c7d7bd85c921d54c71db6e3b697239f2ab`  
		Last Modified: Tue, 29 Oct 2024 05:54:11 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c4730f641baede4404d6decdfe4fc35c1d2fe8392485ec91e9a2e0513e3a35`  
		Last Modified: Tue, 29 Oct 2024 05:54:11 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da5d9f22ec1375bb9cc3c363b5e7b08811443585db60e96f5aa0723db5e163c`  
		Last Modified: Tue, 29 Oct 2024 05:54:11 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab814bbccad21e1f28d56b933e8177c4853ddd23f39a03454d3c928924105ebb`  
		Last Modified: Tue, 29 Oct 2024 05:54:12 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:38f4ec18e5881de8002defc222c7735a0662ea3aeff8a4fd03fdd910370bcc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6490549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c7a15d6ab2ac922ee36beef6fb810877727ce759a4fb543c4bb9ba81b901bc`

```dockerfile
```

-	Layers:
	-	`sha256:b1c431e2bca7d66eff6ebb30b2fff58a9b59e98f0c4b85e3720e1fe92518be95`  
		Last Modified: Tue, 29 Oct 2024 05:54:10 GMT  
		Size: 653.7 KB (653727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c70e9f185f5d6d6771d49940cae021df8934ee8f39f1ff4f42c36754d41176e`  
		Last Modified: Tue, 29 Oct 2024 05:54:10 GMT  
		Size: 3.0 MB (2966342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a575e0ed04d95f5e2b0bb9a48edce43e1acde4ed588b175410ebfe0203a3f937`  
		Last Modified: Tue, 29 Oct 2024 05:54:10 GMT  
		Size: 2.8 MB (2810548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191d6257c315ee75bdc037d57c84224e99c1d5510542cb2f6d59dd5bd7a21c04`  
		Last Modified: Tue, 29 Oct 2024 05:54:09 GMT  
		Size: 59.9 KB (59932 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

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

### `rabbitmq:alpine` - unknown; unknown

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

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:7559d012cd511666ca842ed2b7e9db7dd4f4bccb1f376ba438f4857d85c4832c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65705676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8e1811e5320c7e5ad423848b7e87fc760a26ef503a0c394e1ea732582910cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb2381aa0450053c3a73882eb4489bca34dc89128c4b45cb61f421108b6e494`  
		Last Modified: Tue, 29 Oct 2024 06:09:11 GMT  
		Size: 33.6 MB (33618951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3b4893fe46444d686851e53cbd5b8a8331ab0b03416aee04e6b0b06a45e273`  
		Last Modified: Tue, 29 Oct 2024 06:09:11 GMT  
		Size: 8.8 MB (8834056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b36dfbe9046a7d7cef9270202d7b81a616b99473d01d728df96f193485260e`  
		Last Modified: Tue, 29 Oct 2024 06:09:10 GMT  
		Size: 1.3 MB (1346087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7ef7c2fffd71f271cd0b4579aefc72873120ca77e88bf22050dce3cef00f68`  
		Last Modified: Tue, 29 Oct 2024 06:09:11 GMT  
		Size: 18.3 MB (18332421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9cc32f9f588ccfd14a84c3e33843536bb02fb3dad52b904d33887d2db26804`  
		Last Modified: Tue, 29 Oct 2024 06:09:11 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b12fff42b1b55f054d21483c8ac29f664d936cb6f34f1fe9505093961f938d8`  
		Last Modified: Tue, 29 Oct 2024 06:09:12 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b0608052da7b95f93aa0d41039f059961a5fc581ef86178db8d91e79772691`  
		Last Modified: Tue, 29 Oct 2024 06:09:12 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b26049ebd696515a212008cd7aa586490c6989e037723f8a04cb7729abcd8df`  
		Last Modified: Tue, 29 Oct 2024 06:09:13 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b32fc387d1dc28e08827d692724b91dc021e9bbfbc5c322bdfb5c3d29a7fc460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d13e71bbed841300da4e9b9096aad18628ff5a5d752aab9a79e509c1b69e33`

```dockerfile
```

-	Layers:
	-	`sha256:15ffa322a4163c4b53f552e56ad9b6e01fe341a07e79a71878c2b8b60c9d29ca`  
		Last Modified: Tue, 29 Oct 2024 06:09:10 GMT  
		Size: 647.0 KB (647048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf1f1f4a3f7dd36c3079bf2eda102d0a5155d17ebd01af7951f7a5ead8c8c45`  
		Last Modified: Tue, 29 Oct 2024 06:09:10 GMT  
		Size: 2.9 MB (2938820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5972b53646f9a11af71cacc1d71978b2230ee4c07d766d2fb4395da18ff2998`  
		Last Modified: Tue, 29 Oct 2024 06:09:10 GMT  
		Size: 2.8 MB (2783014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4e3389c3b04a02014b8d2fda82c99f7088ea20a6a8ab45d6c65e4935d516877`  
		Last Modified: Tue, 29 Oct 2024 06:09:10 GMT  
		Size: 59.8 KB (59755 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

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

### `rabbitmq:alpine` - unknown; unknown

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

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:50a1f7dbb4096efab1f7b58cd53b13477fc12300d4c8543f18c2a0d8f0877332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64294104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcea01096fe485d7e127ce96e3af87f0559c67c5b126d30d1dbfceaa72e79ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abbbdb8dedeacfd09d0db41ec29e715d6dbc8325bbf2f8b4d908de2db9066de`  
		Last Modified: Tue, 29 Oct 2024 07:09:44 GMT  
		Size: 33.7 MB (33691102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686cde50f9044d1114b8bbc9b1361407ddb2bfa2136a139ef8643a007518bc67`  
		Last Modified: Tue, 29 Oct 2024 07:09:43 GMT  
		Size: 7.5 MB (7481825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa228c75c7fe8712605d3fbe1c6294bb50ffddbca35546e414dfc24b7ff51fd`  
		Last Modified: Tue, 29 Oct 2024 07:09:42 GMT  
		Size: 1.3 MB (1325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6677f64a7fb6190295f2e15450553cd0b2f6f54526a322e4f5a8c99403e5885d`  
		Last Modified: Tue, 29 Oct 2024 07:09:43 GMT  
		Size: 18.3 MB (18332616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e1303fa59e03534f70b992ed1d089132281fe8954cc2e3dcfad3452bec4990`  
		Last Modified: Tue, 29 Oct 2024 07:09:43 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b701e6139d73cbe17a3202242e7f90e6930d23f9852ee70bae313583bd7a66`  
		Last Modified: Tue, 29 Oct 2024 07:09:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239e3ce2fa702759bf9ccac76ffa0d61df4c597d888c9c3f232aa049303957ce`  
		Last Modified: Tue, 29 Oct 2024 07:09:44 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24142e61aff8d73a105840e1620ff43b9953e90787435832e46fc29317fbfdc2`  
		Last Modified: Tue, 29 Oct 2024 07:09:44 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:11596ae50535f1bae2cb3ac75a5ff299ad80ee779aa66ee4c7070c8dae0a189d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6262683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab46c6687d7314ba3587691aec5e3c12e28f3a206774d87bb072ae7d909ac67`

```dockerfile
```

-	Layers:
	-	`sha256:e47fcd297829d02f0f0639518fa09cb7f5cf2af530ecfc649054853b5ed8c345`  
		Last Modified: Tue, 29 Oct 2024 07:09:42 GMT  
		Size: 647.0 KB (647014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dce2f4b1aa867ac82078baf984f20dcc903cbe1aeec4fffb175c1a4030acc5a`  
		Last Modified: Tue, 29 Oct 2024 07:09:42 GMT  
		Size: 2.9 MB (2855873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496c37e2babb40d5bcad54a53871550d24cb2f43dac2f63da5c3075d557eb97b`  
		Last Modified: Tue, 29 Oct 2024 07:09:43 GMT  
		Size: 2.7 MB (2700097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:727b738dc398fa1d63a5d1fe8cf124f5add0c9fa8f3a979e5d6c48281fcc647d`  
		Last Modified: Tue, 29 Oct 2024 07:09:42 GMT  
		Size: 59.7 KB (59699 bytes)  
		MIME: application/vnd.in-toto+json
