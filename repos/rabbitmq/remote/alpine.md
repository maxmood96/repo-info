## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:ea8af801a9902a409a5c96035c9f3e1114d1e2461e6ef8de21dac739423cad40
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
$ docker pull rabbitmq@sha256:9897b116cefef2707482d63c65e03a4da3ef075c64d6defb3f943bf17583843d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83449152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4b74e375d1d5416641e96d7e3d9a2f66b12ca205f7c771b3c3822fffdc4d5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:32:46 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:32:46 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:32:46 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:32:46 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:32:46 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:32:46 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:32:49 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:32:49 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:32:49 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:32:49 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:32:49 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:32:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:32:55 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:32:55 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:32:55 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:32:55 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:32:55 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:32:55 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:32:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:32:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:32:55 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732b0208544d0f24fed13173f97bd3cac88585b2da9bd65b6804c0a843fea535`  
		Last Modified: Fri, 31 Oct 2025 20:33:26 GMT  
		Size: 42.9 MB (42860345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d498dd8ac22cd265208c03c7e6311925d6a0eb92c5b6ea0fe1ce45beb9936e`  
		Last Modified: Fri, 31 Oct 2025 20:33:24 GMT  
		Size: 9.1 MB (9143878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd961c9618167dd8fd264699e3e4da22348d84b73e23243ceb7510d29de3744d`  
		Last Modified: Fri, 31 Oct 2025 20:33:22 GMT  
		Size: 2.4 MB (2374338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b61556cd43d1e1fe261d39b1d5a54dd7a3cfadd3030540394f1cf84e46cea9`  
		Last Modified: Fri, 31 Oct 2025 20:33:24 GMT  
		Size: 25.3 MB (25266396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a61d3360c9c4708025373372ad2d49acdf2db72e1547352313d3b1112bc56b`  
		Last Modified: Fri, 31 Oct 2025 20:33:22 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f66c2be4940ad059b0043b5a514cad4aaf974940c8cf5be5be9cd43a686715`  
		Last Modified: Fri, 31 Oct 2025 20:33:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f150c3e52aa4712ed5a5114b66f1d4c5d16b906c1b762c4eab70a46e91d4c30`  
		Last Modified: Fri, 31 Oct 2025 20:33:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce3b8c399608a8d07cc961750494aa5fb169e33129ad285af7a5f7c5ea572a4`  
		Last Modified: Fri, 31 Oct 2025 20:33:22 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:eb2dad180b9886732223fdef58891ace02f118d8886fa56f936d5b2f48846541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6432f22039da6879941387cafd46e210737637c9b103022e071f76fc62c98a2`

```dockerfile
```

-	Layers:
	-	`sha256:1127e9cbdabec3ed8b87254458add6740ec7b41605364da45e411d578b1656c3`  
		Last Modified: Fri, 31 Oct 2025 21:53:34 GMT  
		Size: 675.3 KB (675257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:094a2e7198ce725ee11c59f0bb0846346e7bc98badbea166380ffb2c18835bce`  
		Last Modified: Fri, 31 Oct 2025 21:53:36 GMT  
		Size: 3.1 MB (3102698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187d2db7e53d4f24bbc390ea8788a0b3929efee1fd5318f4e9a88c0b1620a423`  
		Last Modified: Fri, 31 Oct 2025 21:53:37 GMT  
		Size: 2.9 MB (2949137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8556cf453a678375a4e9e9d1c3e784aee27d324605dedce0dec107cc4fcc219b`  
		Last Modified: Fri, 31 Oct 2025 21:53:38 GMT  
		Size: 59.9 KB (59914 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:ce23130fbfb2a6a8537a636a51f4a8e6d82e5ae7abc3fd89482239552319b956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71333927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08afcde0b9964ce8b00677ae0cb6647cadb43831ac57b9563d397b5c74ea3de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:13:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:13:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:13:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:13:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:13:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:13:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:13:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:13:19 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:13:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:13:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:13:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:13:27 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:13:29 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:13:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:13:29 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:13:29 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:13:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:13:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:13:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:13:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece8897542c4f43ee106cfdc468e1d0a2bd94977ac55ef96a086318cd503a83c`  
		Last Modified: Fri, 31 Oct 2025 20:13:47 GMT  
		Size: 33.4 MB (33443033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992bab801038429dab8bf295689d9eb3ba5f6e789c8605a3168bc5d0ea3bb9d7`  
		Last Modified: Fri, 31 Oct 2025 20:13:47 GMT  
		Size: 7.8 MB (7788799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3876edb01d71588c3ad65d90bb81d446da11df4d95c66fdd829a82f8e54560f8`  
		Last Modified: Fri, 31 Oct 2025 20:13:46 GMT  
		Size: 1.3 MB (1330060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d3191bb1096264ae3a623fd6e17a89ae2aa93368a490215483205397cfcd82`  
		Last Modified: Fri, 31 Oct 2025 20:13:49 GMT  
		Size: 25.3 MB (25266207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d685bfd4fafe0a6c1fffa92ae642a7cce9653b0b574677a73c60999cff9f07`  
		Last Modified: Fri, 31 Oct 2025 20:13:45 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c87e5fe8e0c37981abd69463e1b7ad58cf6963a229f9e6d40a79e7caeb0e3c`  
		Last Modified: Fri, 31 Oct 2025 20:13:45 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab84621939bd9fcc32679c5eb09c32b229302bf753a1b1e87ec2f223440b9112`  
		Last Modified: Fri, 31 Oct 2025 20:13:45 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6160cf4408f82db86e3196439e645668d3bb1d33e6b198c7cf2cca1ac0db33b5`  
		Last Modified: Fri, 31 Oct 2025 20:13:45 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:901e4234c81b846b1d6625261e3c6e534daf6a74916bcc12a473d4f90c69a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7eef05d88b8b0586d21040dac9bf7a1c0e9e8ca69d2b0ddf90a241a3ed9dd17`

```dockerfile
```

-	Layers:
	-	`sha256:c236214ed89869432ac56b5db935c71d6fd313f6da044b137c78a450e9a2b8b4`  
		Last Modified: Fri, 31 Oct 2025 21:53:42 GMT  
		Size: 59.9 KB (59896 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:2a32f61a9950d3f8473bf9050791d2d52746276b18bea943bac82a0d4323dbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70497509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d099cc2b8712bc05af10129b62a865492b4ac32319772fecfcc7e2a2dfd977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:15:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:15:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:15:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:15:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:15:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:15:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:15:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:15:55 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:15:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:15:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:15:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:16:01 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:16:02 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:16:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:16:02 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:16:02 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:16:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:16:02 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:16:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:16:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:16:02 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f39122e09741def5a9a347fdf0b6f869ba4339b9922929c9737317e81a8312`  
		Last Modified: Fri, 31 Oct 2025 20:16:33 GMT  
		Size: 33.4 MB (33390768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644c2cda1699b58bae97011c5025bcd708d1f3ce8f192a568a33beccc5bfb60a`  
		Last Modified: Fri, 31 Oct 2025 20:16:28 GMT  
		Size: 7.4 MB (7390535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e030fecb675a2e11d9b22136c5a6b8e44b65fcb0c54b3e7dab44bb4172e6ecf3`  
		Last Modified: Fri, 31 Oct 2025 20:16:27 GMT  
		Size: 1.2 MB (1227041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca5b5ff4ab88491d981963813be3b5de1ba76fa388f50a797a45c4a4358d8`  
		Last Modified: Fri, 31 Oct 2025 20:16:28 GMT  
		Size: 25.3 MB (25265867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7371c2567cf18ef8fc34ccce36d6b7cd528b571aa862e06a50f01b4518eb0c`  
		Last Modified: Fri, 31 Oct 2025 20:16:27 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa358c951a6830a7c4e1bec712a99b849d5ac971a9ba84b817277aea1fe32d7d`  
		Last Modified: Fri, 31 Oct 2025 20:16:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8984c1ef7cc49fcc7a1c06d4e425a7a65082bc39c20a0ce312646b679b09475`  
		Last Modified: Fri, 31 Oct 2025 20:16:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afc1dec73b72a7e764abfef3d524ac540531b577a9758d5152812ed5cad6227`  
		Last Modified: Fri, 31 Oct 2025 20:16:27 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d9ce8d4201352bddb9c7abfc8fbdddd4a704742658ec810bcb1af275ec1beb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6551313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58577e5676be6772f9b4c1da402fd942403fb97a617176866febe97fb52ce584`

```dockerfile
```

-	Layers:
	-	`sha256:31e60d4c0b7e3ba0045089aeaa78321f17ac932475bd960e6adb64b593118144`  
		Last Modified: Fri, 31 Oct 2025 21:53:45 GMT  
		Size: 671.0 KB (671050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd407034f3cb0776db68a50248874f1e350cc479640b77bfe375ade20e70f302`  
		Last Modified: Fri, 31 Oct 2025 21:53:46 GMT  
		Size: 3.0 MB (2987521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79739f7db17d5d57de135c4d3903243afb323cca5c6257c7df5c0648b6ca44f`  
		Last Modified: Fri, 31 Oct 2025 21:53:47 GMT  
		Size: 2.8 MB (2832631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b90a6cd76a6c6b408cffec1d4dac3c03d0e619b16763a88729749f9897cafa63`  
		Last Modified: Fri, 31 Oct 2025 21:53:48 GMT  
		Size: 60.1 KB (60111 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:1f4dc90a9a081c4fc2f529c30a82c9fcaf8c6562221e5ddd6373454f2695c8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82507321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e631f0e2fcfed80d6759ed1a3a08ca7e1568187dfd716c6e1814db753e87cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:15:11 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:15:11 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:15:11 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:15:11 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:15:11 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:15:11 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:15:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:15:13 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:15:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:15:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:15:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:15:19 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:15:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:15:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:15:20 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:15:20 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:15:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:15:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:15:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:15:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:15:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:15:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a946dae3b29de4499b3e9db8fa0f2d3059e3805fd8797e41ee9b49d8ab2664c`  
		Last Modified: Fri, 31 Oct 2025 20:15:48 GMT  
		Size: 40.9 MB (40852068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc3b20c8b207fe25c5a905463a1dd6177d187c2aea0c5c659f2953a1dff6089`  
		Last Modified: Fri, 31 Oct 2025 20:15:46 GMT  
		Size: 9.8 MB (9824235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fce4720e0c88ede043a6685b150cab2af1cf1a026f966042cbfa42a5c7cbc4`  
		Last Modified: Fri, 31 Oct 2025 20:15:46 GMT  
		Size: 2.4 MB (2424786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce15a6aa1b5d02b995704b9dd00e4035d1093cba77b668d1ee04f3b537c4cdb`  
		Last Modified: Fri, 31 Oct 2025 20:15:49 GMT  
		Size: 25.3 MB (25266418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c9506bc5d5f42e7c5a3a643769be2e8c6f78cb746736d2326a9d19b6088807`  
		Last Modified: Fri, 31 Oct 2025 20:15:45 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960cc215c73c76fcf4146818c4dea3c5a06e3f0f9a97b2ca43f3bc44033a84cd`  
		Last Modified: Fri, 31 Oct 2025 20:15:45 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb18b08c4bd9e018064d0cadd9153ca8aa64d728ad6b00ac583cb7ff829cd3b`  
		Last Modified: Fri, 31 Oct 2025 20:15:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8c4919d681146c61c610b584fd7763491f14eba0d44028b2508494968d150`  
		Last Modified: Fri, 31 Oct 2025 20:15:45 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f24f35e124389907f37d4ac5b0d85730549d95222045078ef60418d453f05099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6895311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe378b67df1c21561f659554b377cd123fbb5d546bd2ca784497293f6c5309a`

```dockerfile
```

-	Layers:
	-	`sha256:3fdee9b019d17b5d9d517adb166f537f4c0440fe7bbbcaa48b95b97543448748`  
		Last Modified: Fri, 31 Oct 2025 21:53:53 GMT  
		Size: 676.0 KB (676050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a19819eb2eb90e652b3080cff2e5c514f419e26bb1d901ba38044cb1149e016`  
		Last Modified: Fri, 31 Oct 2025 21:53:54 GMT  
		Size: 3.2 MB (3156996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c473ac67024c629b85e67e8dcec53af4f8a2af2b166c3fab1211bac66fe8d11a`  
		Last Modified: Fri, 31 Oct 2025 21:53:55 GMT  
		Size: 3.0 MB (3002112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c282089b5c50f89c585c2c606cac0bc057c958da0b7d629e8521ab673980439`  
		Last Modified: Fri, 31 Oct 2025 21:53:55 GMT  
		Size: 60.2 KB (60153 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:b580779e55a17836051945166dfb4b048fcd8fa484d81bc250287caaf429585b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72920381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2e2ea7e3a35f6fea8b786bd6cc750212d9de8a1f558d3107044521c268625a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:14:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:14:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:14:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:14:13 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:14:13 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:14:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:14:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:14:15 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:14:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:14:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:14:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:14:21 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:14:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:14:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:14:21 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:14:21 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:14:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:14:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:14:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:14:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:14:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee08550e729b6612c1251b2eaf00247f9a6b1d6baa20517a22018ac90d021dec`  
		Last Modified: Fri, 31 Oct 2025 20:14:46 GMT  
		Size: 33.5 MB (33542335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9378f3fc50cb6216cc88e86e0b6b77402c2c3c276e92108244e37010a1ecc756`  
		Last Modified: Fri, 31 Oct 2025 20:14:45 GMT  
		Size: 9.2 MB (9159103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac60a76d27c1b5690e1cd9e25d017d07fa3407a9add304f401a955029ce42c6c`  
		Last Modified: Fri, 31 Oct 2025 20:14:44 GMT  
		Size: 1.3 MB (1332478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f77b2a4e403f5a398659a620a5c9a010d9a20ca4883e3361d7d8e5e8ad8a6de`  
		Last Modified: Fri, 31 Oct 2025 20:14:48 GMT  
		Size: 25.3 MB (25265791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2e3896da60749a415d9a0df99b9391c411b0d8d5cffb0d839ab49e3f2566f2`  
		Last Modified: Fri, 31 Oct 2025 20:14:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689361d2a21e6f7164806ceb04116691b28faa7164e60050c004b93519e82a9e`  
		Last Modified: Fri, 31 Oct 2025 20:14:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c988ae4cc1f631438af0d07d57ffc62079ce704735beda1b3dfa5746effd60`  
		Last Modified: Fri, 31 Oct 2025 20:14:44 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6942f89adffb4c1eaa4364082518b9a1bae64101b3b2bab6dd82c3396b956f`  
		Last Modified: Fri, 31 Oct 2025 20:14:44 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:961aedfd5e6c2197e82e38dcb3130b164cb95f75212710c6a49bc5b7b393c57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6759847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f24a36af76917ebb03a4bad53adf3743da9b58cc623d56a6f70c50692efa38`

```dockerfile
```

-	Layers:
	-	`sha256:12a551460c0043e9c48c81c874ecc6452b0532d75e930248aa3d310b0abb5bd0`  
		Last Modified: Fri, 31 Oct 2025 21:54:00 GMT  
		Size: 670.3 KB (670252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb20d852b91833c1b480061bff46a60e9fc45dd473eb1ee86fcc427aeee4cf3`  
		Last Modified: Fri, 31 Oct 2025 21:54:02 GMT  
		Size: 3.1 MB (3091644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94bc00501f87e58119749b52015654e6e2eadaf9f4840cabd011f09935d78142`  
		Last Modified: Fri, 31 Oct 2025 21:54:03 GMT  
		Size: 2.9 MB (2938087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bdf77ceffa41244a4d8158877182fc84378ece9d61c7e9dea5f96855c861637`  
		Last Modified: Fri, 31 Oct 2025 21:54:03 GMT  
		Size: 59.9 KB (59864 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:12cfc52e4a28c93d73232727c5df3f48ed2a207491cf664d5ae04e015f3f43aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74152022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7d99c9db2d5874e23240d0d1b45ff4a660e328d2e8ede52a43145f0f9c7ece`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:20:58 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:20:58 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:20:58 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:20:59 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:20:59 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:20:59 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:21:03 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:21:03 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:21:03 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:21:03 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:21:03 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:21:12 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:21:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:21:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:21:15 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:21:15 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:21:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:21:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:21:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:21:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:21:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde3b0587238eafb4757f1505ee9693980a934e68c7f7abcabe5dcfdc544831a`  
		Last Modified: Fri, 31 Oct 2025 20:22:05 GMT  
		Size: 33.9 MB (33925474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb1cae72f876f7e77ebe4db3c09a4bb5b6e826cffe0e37b6b043e62f47a44ba`  
		Last Modified: Fri, 31 Oct 2025 20:22:02 GMT  
		Size: 9.8 MB (9774072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cdff811b99fdab5bb1c04dded6d014c3612bcc44bf1cea5fc9ee09bad2e422`  
		Last Modified: Fri, 31 Oct 2025 20:21:59 GMT  
		Size: 1.5 MB (1452616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5605c5ba6654595ad2e8202fb1bb3829acad6884f0a9a1ef98145dec0212112f`  
		Last Modified: Fri, 31 Oct 2025 20:22:01 GMT  
		Size: 25.3 MB (25265867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41287f194fd7915aa7bdc32fa37b866a5c37f70ef9be6d1a71025427ef25f926`  
		Last Modified: Fri, 31 Oct 2025 20:22:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797e693acc3369faf32068aee8c5aa75c5cc412cf7f9ce5dd783cf93637e04ee`  
		Last Modified: Fri, 31 Oct 2025 20:21:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62efc6b1c57df28d871195aeef22848ce2b9f7875f03d6dbb8babfeb751e8c3`  
		Last Modified: Fri, 31 Oct 2025 20:21:59 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdbe0030b7110c49ea3ac8a50aa33f76d138817fe4fd890406ac14a658232c0`  
		Last Modified: Fri, 31 Oct 2025 20:21:59 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:836d87e38d6daba7fda40cea6772a9d9b4162f479f22e517d9042788e649f4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d3856457aa4721230794170816127abda0dae383fa33775123698cbc25dd32`

```dockerfile
```

-	Layers:
	-	`sha256:2d0a6ab593ab15909a3e304195edee8b79540d5b2011a775e9ec4527168e58cd`  
		Last Modified: Fri, 31 Oct 2025 21:54:09 GMT  
		Size: 669.1 KB (669097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7384c4a998117f8f7f2819c64048cc37ee69a623e8f710f8ec58664f6f1e0c`  
		Last Modified: Fri, 31 Oct 2025 21:54:10 GMT  
		Size: 3.1 MB (3108750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c9a81ce5c0777418e2307cb3fbf086dee294e5bda16f196e57fb9b5de4e282`  
		Last Modified: Fri, 31 Oct 2025 21:54:11 GMT  
		Size: 3.0 MB (2953854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb0744ea9651e83f32ebe0434910a8da78cec70aff24157535995dd6429db32`  
		Last Modified: Fri, 31 Oct 2025 21:54:12 GMT  
		Size: 60.0 KB (59976 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:29fbd3596046b0e686c0e8f9635249842ecfbe0f69f3c71c52eb2742f0098565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75949637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7d71d9341c86a4559a3a8ff8d2ebf2907717acc735197b79f778dc6d4ef66f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:00:41 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 23:00:41 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 23:00:41 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 23:00:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 23:00:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:00:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 23:00:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 23:00:55 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 23:00:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 23:00:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 23:00:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:01:34 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 23:01:43 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 23:01:44 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 23:01:44 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 23:01:44 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 23:01:44 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 23:01:44 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 23:01:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 23:01:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 23:01:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 23:01:45 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10134cdd10881c5b8872bd6a22cdee3d4f7947cf07d56bcfcb67b233a15d9c12`  
		Last Modified: Fri, 31 Oct 2025 23:07:28 GMT  
		Size: 34.9 MB (34893302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc84479dee5ea17251ec65d2bf63013f46012984d82cfc0dacc6fa4e7eb030c5`  
		Last Modified: Fri, 31 Oct 2025 23:07:26 GMT  
		Size: 10.9 MB (10906600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdf1244b1015e4f3abc2025a38925d773a84d3d23c8714af5da707a897f52e2`  
		Last Modified: Fri, 31 Oct 2025 23:07:25 GMT  
		Size: 1.4 MB (1366493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f4fc003ebbc648006e42a148cf719e3feedb9f149b92374c03280473701263`  
		Last Modified: Fri, 31 Oct 2025 23:07:26 GMT  
		Size: 25.3 MB (25266245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d2996778974410b330bf379c00903a3c4ce56446833a9a35bc6536e6a847ac`  
		Last Modified: Fri, 31 Oct 2025 23:07:24 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f45fce4291972f5f7b9e2062982b27b38e93f4c4fdd45f7295fc1b4a5754c1`  
		Last Modified: Fri, 31 Oct 2025 23:07:24 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b03d9a6ea73b622b2b8f9cc00a18a440a39bfa753b3e610d5d4c090005e4e5`  
		Last Modified: Fri, 31 Oct 2025 23:07:24 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbca45694e03cab13dfd5bd528aeb3d3f90eb8147368710ebbb3ab1902a19ae`  
		Last Modified: Fri, 31 Oct 2025 23:07:25 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fbf07b92850ce400d83f880962e1b8d343301f36ea68bba87b78973221f9a038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6871011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaa7a6df131017e13bf0e3f95de3df4e3cd4d57cb13786eda4157a514cbfaf4`

```dockerfile
```

-	Layers:
	-	`sha256:1844e427f98a577250e430d47734ec3f0f6edef866be4ea9cd2353aaa707fae1`  
		Last Modified: Sat, 01 Nov 2025 00:53:08 GMT  
		Size: 672.1 KB (672066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1f305f135df43cb74bfd1fce35a62f4a563c2927a5d8a4b71aa6829d4d55135`  
		Last Modified: Sat, 01 Nov 2025 00:53:10 GMT  
		Size: 3.1 MB (3146923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a70ade8edf2072bb55796cd7fc6af504ade025aaa6596dde1fd11bb014100a6c`  
		Last Modified: Sat, 01 Nov 2025 00:53:11 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e21df8177fd0c945efe406ad7163dc584f75544ff3c96c366d4967d7318592`  
		Last Modified: Sat, 01 Nov 2025 00:53:12 GMT  
		Size: 60.0 KB (59983 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:422bc078c76a5838464ca23b92814728edcf07452cd62a4bb0a119b0068e0f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72663100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b632095d80fdca481654041a8e7130041aa166b449620cb76778858dbc9f804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 20:23:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:23:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:23:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:23:58 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:23:58 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:23:58 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:24:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 31 Oct 2025 20:24:02 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:24:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:24:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:24:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:24:16 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:24:17 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:24:17 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:24:17 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:24:17 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:24:17 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:24:18 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:24:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:24:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:24:18 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:24:18 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151f10fe2d5970a93b2c09548b23918d27bebe3e729d40d18d105c927642f22e`  
		Last Modified: Fri, 31 Oct 2025 20:25:04 GMT  
		Size: 34.0 MB (33968406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbcef3ee149023b862d4a5c01ed000b7fe1681669f9d8c804eef402cca769ab`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 8.3 MB (8347157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc7a38ee1fe3901818cf81de72c1870a6b79011fef3b3611a15bf1da29e0956`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 1.4 MB (1430649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735665edefcf2aad4d55873503deef537e0b49d462265a8b17fc79f095b37578`  
		Last Modified: Fri, 31 Oct 2025 20:25:04 GMT  
		Size: 25.3 MB (25265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742e635b9f74cfb089d934abae9fdfe3b17ce487a6dfee24efaf182551ae3167`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986382df115e6dc31f54750e52b580a296073f3a0dd12ce90362757849e340b`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b932a6beae64243460533130ac7459630af3d0d44a748cb7d6c9be9f8ebe42c8`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c0e48355b01996594567359c479d344d831f665c938466c42aca4ad450b5ed`  
		Last Modified: Fri, 31 Oct 2025 20:25:02 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2b60b7da3f682c6362516d0360a1276df6732a742f151555b88c4de3b6194f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6570485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17705e50c22fb192a593fad926b46b1a726ae2accd953c8e40fc01f5665fa0b`

```dockerfile
```

-	Layers:
	-	`sha256:511186739443ea61e2ee0ff7d2ef23c269c1e43d8ccd128f6735bcea62df5149`  
		Last Modified: Fri, 31 Oct 2025 21:54:21 GMT  
		Size: 669.1 KB (669063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1f64fbf52761f93c864ab31b923c435c4912315b0860a99e6a4b2cf4c986af`  
		Last Modified: Fri, 31 Oct 2025 21:54:22 GMT  
		Size: 3.0 MB (2998187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021d277d901e2cb689b57977ea65b6cb59cc8b0e36ea42db35bb5d794b74b69b`  
		Last Modified: Fri, 31 Oct 2025 21:54:24 GMT  
		Size: 2.8 MB (2843321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f43c66b8e16b108c3431016c584a0de92f4e0fc8bc4b3e259646605bc2594b`  
		Last Modified: Fri, 31 Oct 2025 21:54:24 GMT  
		Size: 59.9 KB (59914 bytes)  
		MIME: application/vnd.in-toto+json
