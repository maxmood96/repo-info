## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:1bf9ce8942a362d66d21a43374bb3f087499336937e4544a50f56f203ede512c
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
$ docker pull rabbitmq@sha256:3de72be982b3160abd7a943c8ab97cf3278733aef0457804ad8037f78db808ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72270622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9195de9da5fcb7de4b543fe6089e0fa13bbf3a0e713955e23e2ed162b86dbdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d128196ad6299635045d082c903f496d1cda9c2df2313a221d1d8467df5236a`  
		Last Modified: Wed, 10 Sep 2025 23:40:37 GMT  
		Size: 39.7 MB (39739233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf965c847b1ec7782917292b5fc26380e586eb9cfcaa919f43f565583479c03`  
		Last Modified: Wed, 10 Sep 2025 23:40:37 GMT  
		Size: 7.6 MB (7599156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d91c09f917664538b1a502477ce9b9ed9e42cabff7379efc3b7998f4e08cac7`  
		Last Modified: Wed, 10 Sep 2025 23:40:32 GMT  
		Size: 2.4 MB (2374074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fb2301f95811948a665b64179c4eb6ca291e94a8e68391ea0b000510df3f08`  
		Last Modified: Wed, 10 Sep 2025 23:40:36 GMT  
		Size: 18.8 MB (18756726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acdb7d8826851eed3780f103033ffbdcc61df3489a51bd93af8e7840cec57ee`  
		Last Modified: Wed, 10 Sep 2025 23:40:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51be9c78d7e881dc1c4ad5630b67d5448de2f700c7ca65d5406df79bc3efbe80`  
		Last Modified: Wed, 10 Sep 2025 23:40:32 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41fae3d1964234f3b2da1cc8e553b83979d482864bf3f130a1bff45cf3a2a11`  
		Last Modified: Wed, 10 Sep 2025 23:40:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede6c4c96af425badd0903de0fe1fe3c7517c80eec8918adf877a7e9f5ead23c`  
		Last Modified: Wed, 10 Sep 2025 23:40:32 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8bda6fe5191c43c7649d93eae55bda507361d827414f3197da73b47b45878db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4594b4fee7257a52ca1b2feeaea9f033eaaff842d61b045f9fd65f1761c0cae`

```dockerfile
```

-	Layers:
	-	`sha256:1163df7d1976fcae080f7a35fcdd0ea24985baa19f17f7ee46a12e42fe6ac99e`  
		Last Modified: Thu, 11 Sep 2025 00:52:44 GMT  
		Size: 664.8 KB (664773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:390e983f8ab96685f164f610b582195ab7dd6b07144fd9b2d540da12ca2f58b0`  
		Last Modified: Thu, 11 Sep 2025 00:52:45 GMT  
		Size: 3.1 MB (3103686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cff0877e2ef9dd2f263ff19026d2f664e988422f40df40996455191730cebe26`  
		Last Modified: Thu, 11 Sep 2025 00:52:47 GMT  
		Size: 2.9 MB (2948839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17087f3414e2a57efbb3a963a63f9222121f9b662750a6ba37de7115cf492076`  
		Last Modified: Thu, 11 Sep 2025 00:52:48 GMT  
		Size: 59.7 KB (59674 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:036303c97739997de03af469d3382edf68b95e197c29d043d0948dcc907603c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61311493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c532ed41e9c97e3f46f77dee58f91de81d02999f92108e477fc80b3725fa3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 17 Jul 2025 17:05:10 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 17 Jul 2025 17:05:10 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 17 Jul 2025 17:05:10 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 17 Jul 2025 17:05:10 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_VERSION=3.13.7
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 17 Jul 2025 17:05:10 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 17:05:10 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 17 Jul 2025 17:05:10 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 17 Jul 2025 17:05:10 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 17 Jul 2025 17:05:10 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jul 2025 17:05:10 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 17 Jul 2025 17:05:10 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c90f2d6b1ee72fddbb18fdcb44194ba73e7d6a1803c47360ad8d9138e544f3`  
		Last Modified: Thu, 17 Jul 2025 21:50:06 GMT  
		Size: 31.3 MB (31297021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e745f5506fb357d401ab614452e7a99fc8ee17a672ca0fd764eb1b06415969f9`  
		Last Modified: Thu, 17 Jul 2025 21:50:04 GMT  
		Size: 6.4 MB (6425262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c37a748fa1512ee4ed61b3b9f28f6e28ee254484099020f5009d34d6472b1d`  
		Last Modified: Thu, 17 Jul 2025 21:50:04 GMT  
		Size: 1.3 MB (1329820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328c881948a84d10b50c553caa8c05886d3b25c9e67833ff5989bd482fc40b15`  
		Last Modified: Thu, 17 Jul 2025 21:50:05 GMT  
		Size: 18.8 MB (18756727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cee5450c10f854868d7a1e64f9a5674ba521571f8a711065b7e6d11b0add15`  
		Last Modified: Thu, 17 Jul 2025 21:50:02 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88db69eb9622171ab3bf4f462fe426a41ec5079d715fb6bc97e93fe6c09e396`  
		Last Modified: Thu, 17 Jul 2025 21:50:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a05bfc71d12f03a9bf72b48a83dfe0f02acbd8cd4cde4404633a9c92f121df`  
		Last Modified: Thu, 17 Jul 2025 21:50:02 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e01925e21cf02d8de8ec6fb844a502e33790cecf80e3e8afe7be258aa9b5fe`  
		Last Modified: Thu, 17 Jul 2025 21:50:02 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ba4d4ce6f81fe93066f62190f27b44eef57068ae9793a6dbca5c3a6a133bfbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 KB (59643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2341c5064aa919144f13adb5a873625c7a78e75c3bd67af30173989d292e3ac`

```dockerfile
```

-	Layers:
	-	`sha256:afc28180879c9680a60475bbf8366e3a2bc1784f3ed642f9a027940935d2b7a1`  
		Last Modified: Fri, 18 Jul 2025 00:53:17 GMT  
		Size: 59.6 KB (59643 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:02cfec47aba4c35620a34cdee68d1a1aec74f3b4092b0e5d51cd8e9fdc1551b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60555822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c929276c11aba0e3946f53e8fbe266e8c2cea62f705afb18420d0cfa26b095b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 17 Jul 2025 17:05:10 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 17 Jul 2025 17:05:10 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 17 Jul 2025 17:05:10 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 17 Jul 2025 17:05:10 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_VERSION=3.13.7
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 17 Jul 2025 17:05:10 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 17:05:10 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 17 Jul 2025 17:05:10 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 17 Jul 2025 17:05:10 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 17 Jul 2025 17:05:10 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jul 2025 17:05:10 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 17 Jul 2025 17:05:10 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9bc3578ddbc96b3c547f31a985352c15ecafbd2e469e0d03b875b967d4d931`  
		Last Modified: Thu, 17 Jul 2025 21:59:22 GMT  
		Size: 31.2 MB (31226634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7adfeec5783a415a897edb716397a883ce784bf6affd5bd6db96a28faede78d`  
		Last Modified: Thu, 17 Jul 2025 21:59:19 GMT  
		Size: 6.1 MB (6125174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cc84511a9985b3dcc314c462280a3ea0cd6532a6e0b3f7d067601c50442276`  
		Last Modified: Thu, 17 Jul 2025 21:59:18 GMT  
		Size: 1.2 MB (1226721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec622bca79066979c6eec071bf51883f456e4ba069f9cb16228d2e6de4b7ddea`  
		Last Modified: Thu, 17 Jul 2025 21:59:20 GMT  
		Size: 18.8 MB (18756504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98acc2afa60a975d3e462f00d669a8d013a9393179255fb0a8f5081ac74e04a3`  
		Last Modified: Thu, 17 Jul 2025 21:59:18 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d52a5188ff8974836578843a040a1fff00850238f12762e6a743772f177176`  
		Last Modified: Thu, 17 Jul 2025 21:59:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf127bd0f8a269c20a78706903c37de9b5fab802ce51688232cef0a48a63852b`  
		Last Modified: Thu, 17 Jul 2025 21:59:18 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16c742f92149e034f08b27dba1d036d616a1922f8488aed7295fc74d25bc855`  
		Last Modified: Thu, 17 Jul 2025 21:59:18 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2153ffc69d2b30806211cb8aa44c091fb4137d17ad005078a0ad368ee301d32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc220ad56e022d169b088ff3b3bf0d4891750de3fa70b0fca81f4e86d8e11381`

```dockerfile
```

-	Layers:
	-	`sha256:d51c9959c133770f730f0b48e2e1daf8a2256373fb8376fe03a7cedaa86df4b2`  
		Last Modified: Fri, 18 Jul 2025 00:53:20 GMT  
		Size: 660.6 KB (660559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855a7ec49a86b807a6e136477a66211b0ca09c957d029497c9517b89877c84fc`  
		Last Modified: Fri, 18 Jul 2025 00:53:21 GMT  
		Size: 3.0 MB (2988503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ea16d0150df02f00fc1206e274ba14bbde4bbd8344f4022ef9f83a1591d14f1`  
		Last Modified: Fri, 18 Jul 2025 00:53:23 GMT  
		Size: 2.8 MB (2832325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21124045f268440d69bacca7b11753078ec346d2e7839f7872d97675ec819075`  
		Last Modified: Fri, 18 Jul 2025 00:53:24 GMT  
		Size: 59.9 KB (59858 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:648317109b16b4c2d15c95a25673918e555cd50cb1a9125374f9c676fb9409a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70477192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b654a049dac639556c1547f301447808e25c40d9d8aa7c88625f3b410eddd11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eba2d7f22e249626ec8f468ca7abc6d105cd61e7def07562c107cdef07779c7`  
		Last Modified: Wed, 10 Sep 2025 23:42:41 GMT  
		Size: 37.9 MB (37922741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e901a506c6367d11274765baeaf2619dcd70082806b9e89ffb89f3a42818e37`  
		Last Modified: Wed, 10 Sep 2025 23:42:34 GMT  
		Size: 7.2 MB (7240466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e61a18600d5c00038c01cea9be9ec436bcc411ccf76f55561575ac5c7bbbc7e`  
		Last Modified: Wed, 10 Sep 2025 23:42:31 GMT  
		Size: 2.4 MB (2424772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088d73f4794745e7d99820e6af5846a94bcc23e22289bbfc1251d646e8c85548`  
		Last Modified: Wed, 10 Sep 2025 23:42:33 GMT  
		Size: 18.8 MB (18756718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4e6cd688d67a067f23af4dd010f72ffe150159d64983a5856235080767397c`  
		Last Modified: Wed, 10 Sep 2025 23:42:31 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526dd625be1601f684e14c9f78d0f46b9f71059c9b905050a777cad4595ae0e8`  
		Last Modified: Wed, 10 Sep 2025 23:42:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa4163a6708e7c5f97777f63befd4785790c4c23aeae6016d4856200ec1a6ea`  
		Last Modified: Wed, 10 Sep 2025 23:42:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1634ccd2fd62f6c7dcb5c7f522a33530f7352a6f653d2e48a9d23844d84da98a`  
		Last Modified: Wed, 10 Sep 2025 23:42:31 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5df8fba8c12a10478490ec0304abb073d8199f01fda70ad6c1bda38d0cf953c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6885231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de962dc84769018d013cc3c7e1d116eda5810b282052278f340003f2d5fac1e6`

```dockerfile
```

-	Layers:
	-	`sha256:4fb0bff71794a05fdd374a7cadca64f156ae27d2528a135c3511a77561e369f5`  
		Last Modified: Thu, 11 Sep 2025 00:53:01 GMT  
		Size: 665.6 KB (665555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f8defc2b53e805a9d113df88c5cd555094a1ffb341cb89c9215ab75df405adf`  
		Last Modified: Thu, 11 Sep 2025 00:53:02 GMT  
		Size: 3.2 MB (3157974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d874288f09a9a8fb0dcb9a77b02dd412736778346089253469dba5c04d1921`  
		Last Modified: Thu, 11 Sep 2025 00:53:04 GMT  
		Size: 3.0 MB (3001802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9326e7da3fa1f9a152843b38193f398bf73991160bfe03cc0e2348c077779cad`  
		Last Modified: Thu, 11 Sep 2025 00:53:06 GMT  
		Size: 59.9 KB (59900 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:aa218ca9122adf04e49ba1446dfe8eed4be245a6266ad3ece8cafd6cfe3cf12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62593672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdfae00b8c944e971376559e18a13dbc4926e7a07aa20c7ce59a8d18f43a9e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f2f7f23a209685a18efc07f22ec1dae7e194d08855f7947731f33002ce30c8`  
		Last Modified: Wed, 10 Sep 2025 23:40:37 GMT  
		Size: 31.4 MB (31380775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e597f0dd0678d506af17c3c52d5deeb6d3331a2ee1351442163f72d5ab28d1`  
		Last Modified: Wed, 10 Sep 2025 23:40:36 GMT  
		Size: 7.5 MB (7507402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a62890c86c9ad0d3e364ece3fbae62cfb7231e5fb6f7a92f0608563ae423f7e`  
		Last Modified: Wed, 10 Sep 2025 23:40:36 GMT  
		Size: 1.3 MB (1332228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5292978855a4462345dad7d1661341095b7a602e38a39f3fa4c40c0ffb5f15f6`  
		Last Modified: Wed, 10 Sep 2025 23:40:36 GMT  
		Size: 18.8 MB (18756517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b6c64ee184bff16c948535797191343b75935719ff3c21025b591e50d650ce`  
		Last Modified: Wed, 10 Sep 2025 23:40:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32475846ad6f08af3475c90b335a9afd9059a47a9748113a4e5c76ab6b18fa7`  
		Last Modified: Wed, 10 Sep 2025 23:40:36 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3537fe11d4a5966610f1acf0338d72e3ab44e37c43ef2d53fc50ca1d0fff0176`  
		Last Modified: Wed, 10 Sep 2025 23:40:36 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdd8ec93d8c8ad52834a59366afdfcf6a7e34e083059ee1c3e220eb1c175f7e`  
		Last Modified: Wed, 10 Sep 2025 23:40:36 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d510e9f15520ce0caf6bdf9cc85cb1b5be6a744c3112ea8a42e6dab62a0c1c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6749833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8453b657629d35b52db693012d756cae82502c4d517bb353f435d7501ca8be0`

```dockerfile
```

-	Layers:
	-	`sha256:19a610c3183d65384f01dab3f0c7bce560d6528aa97f1364ae0f8010d6854975`  
		Last Modified: Thu, 11 Sep 2025 00:53:10 GMT  
		Size: 659.8 KB (659773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68485152aa7fb27b0873cf728a0e59269356b8d74325e770371f4803c787610`  
		Last Modified: Thu, 11 Sep 2025 00:53:12 GMT  
		Size: 3.1 MB (3092637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bbfdb5493b3c2eaf49d94d28de23596f6ac9abaedea8c6fcb1e882ddfcd9daf`  
		Last Modified: Thu, 11 Sep 2025 00:53:13 GMT  
		Size: 2.9 MB (2937794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d74791a78adb9f157d50fbdb417f50804b50fe802fcad935d40a802da26732d`  
		Last Modified: Thu, 11 Sep 2025 00:53:14 GMT  
		Size: 59.6 KB (59629 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:30064a90b6989d3f4cbb99db796a6ca027104def50e3e30d75085e0a7f2ba3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63699290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fff7b9ea9d71ebee299267213a9352f3c0383ceaa792f62b13e670c77ab92b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498c67e7466ee5d3008de7eaa57351cd3919d917f1b66f74ec31f685d240be56`  
		Last Modified: Thu, 11 Sep 2025 00:18:02 GMT  
		Size: 31.8 MB (31757787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7395f31d677f6092c2e5bf24e4cf88d35a6ce30d2786451c949e8889fe76c70`  
		Last Modified: Thu, 11 Sep 2025 00:17:59 GMT  
		Size: 8.0 MB (8003727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1440b1dbd4dd17e8d14175cd0f372a189d7d113b4b0f6dece5610d72ddac778f`  
		Last Modified: Thu, 11 Sep 2025 00:17:59 GMT  
		Size: 1.5 MB (1452389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c73525281579d00b24c5f7894efc4b897c77b5793f98236a96e88efb0c6b7a`  
		Last Modified: Thu, 11 Sep 2025 00:18:01 GMT  
		Size: 18.8 MB (18756523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa89f82f99ba358c92260a990e0cd54f99b7623696de55f4b3a9678db099459`  
		Last Modified: Thu, 11 Sep 2025 00:17:59 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63ae8cb56f27331b68a38e1d7ee1db3e200b0114950012d4f33ecbcbfba6e7b`  
		Last Modified: Thu, 11 Sep 2025 00:17:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ae0705dc87a202fc12fa29c6e67e461a9dcbfa71510c2561b18dd5f540b7e8`  
		Last Modified: Thu, 11 Sep 2025 00:18:00 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a18fa1cc51a03312c6cd33e82469e98ae1d1766454d8d0aca67b9628cbbbbf`  
		Last Modified: Thu, 11 Sep 2025 00:18:00 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c129c3c5b22854bcccc5aca5580fbade9fc8d1fcdc015d7bdef2f5040d73cca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6781622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667225ad155f41e07be53de16be8bed9a50ffa98d93b6c026834768cb3d0c3d3`

```dockerfile
```

-	Layers:
	-	`sha256:9f52ca6bd65aa52cbb50097d31ec959c9537c43cdd47d24beaeb0defb87ad9d9`  
		Last Modified: Thu, 11 Sep 2025 03:52:52 GMT  
		Size: 658.6 KB (658608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9cfee7aa5014069fd2af87b69e4c41f14876a59b6400fe66858b4c4196548a`  
		Last Modified: Thu, 11 Sep 2025 03:52:53 GMT  
		Size: 3.1 MB (3109734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ab541a8ca8a8a5f6bde903b0bdffa3a5c679de59f51210f73e36c269b09369`  
		Last Modified: Thu, 11 Sep 2025 03:52:54 GMT  
		Size: 3.0 MB (2953550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4491aac582f804092f531a03f09320b82f7e8618151071623fa1b2bd5ebb862`  
		Last Modified: Thu, 11 Sep 2025 03:52:55 GMT  
		Size: 59.7 KB (59730 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:80dec647eff1d0bec24ad2eddcf8bb0731d03e98fe8f47dd0305c30251fc737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65117266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb2da56e0f2f9059a39431085809bbea5c0e190b69f1c6259635e97ea1a60dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 17 Jul 2025 17:05:10 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 17 Jul 2025 17:05:10 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 17 Jul 2025 17:05:10 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 17 Jul 2025 17:05:10 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_VERSION=3.13.7
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 17 Jul 2025 17:05:10 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 17 Jul 2025 17:05:10 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 17:05:10 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 17 Jul 2025 17:05:10 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 17 Jul 2025 17:05:10 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 17 Jul 2025 17:05:10 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Jul 2025 17:05:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jul 2025 17:05:10 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 17 Jul 2025 17:05:10 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03924f3b5bc380e8edf02d4c089cf98ae0c898b3028f653191cfbd92ba990e97`  
		Last Modified: Sun, 20 Jul 2025 10:03:48 GMT  
		Size: 32.7 MB (32720744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90dfe60718896288bb90fe76d4b51cb78b80bf8b1bad15dce3774c5dc3143fb`  
		Last Modified: Sun, 20 Jul 2025 10:03:47 GMT  
		Size: 8.8 MB (8758941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c92861818aeb1ab23e0493e1a59e2a6a0e6c92468ec749162b4ff2ef51110f`  
		Last Modified: Sun, 20 Jul 2025 10:03:47 GMT  
		Size: 1.4 MB (1366252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a408750dc93c857fb07d8ee1ba1dee2c3a15299d138818e0afa10adbc9d2620d`  
		Last Modified: Sun, 20 Jul 2025 10:03:48 GMT  
		Size: 18.8 MB (18756778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179e9a44facecf3a2161f7c7158f8d4ac659262af26e2c9b33665fab48f3f8cd`  
		Last Modified: Sun, 20 Jul 2025 10:03:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3b2ec61f84c8520c11e4245853d664790c775c87328aa3ca3b4f073b5794c7`  
		Last Modified: Sun, 20 Jul 2025 10:03:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4003741f8129660e03d9f6a0e1decaeb6b5e100a84b7e88518154cad8aea919`  
		Last Modified: Sun, 20 Jul 2025 10:03:46 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8cf6e494cf31bcc4e441bec64ea0adeef9ecac7338167700763c8efe00b652`  
		Last Modified: Sun, 20 Jul 2025 10:03:46 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:edd9687ee980ad7539d9f580c1895f296be53a7c8b78faa7681cf8ec0b604688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6860949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d6117975cfef2a69be8293a4f1f38206a49209704fe163b4cfc958cdf021a3`

```dockerfile
```

-	Layers:
	-	`sha256:5720fbb77c48fb4925e7d1d66e67d54da2222745062527ec72c20e7a03cdbc90`  
		Last Modified: Sun, 20 Jul 2025 12:52:46 GMT  
		Size: 661.6 KB (661577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d16a187e6b4c3e2830b7f9df74d2175bae33d7e548c70238674efd689c62b9e`  
		Last Modified: Sun, 20 Jul 2025 12:52:47 GMT  
		Size: 3.1 MB (3147907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54ee4959b4273d19523d8321c9ad63e56528363b99f1ff5f0986672b49974654`  
		Last Modified: Sun, 20 Jul 2025 12:52:48 GMT  
		Size: 3.0 MB (2991735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f9fadf371e550ace01b149fcfad99dba66545962e13abf617df41edee84ca6d`  
		Last Modified: Sun, 20 Jul 2025 12:52:49 GMT  
		Size: 59.7 KB (59730 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:53923779cda396faa80d496755080d21d389e27c9758c4931c376dea26e225d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62372366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2996c37b6e37f199ee6e8160b2e281b76a79b49f0221e0a9bb7d52867b11d1fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Sep 2025 17:05:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_VERSION=3.13.7
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Sep 2025 17:05:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 17:05:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Sep 2025 17:05:14 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Sep 2025 17:05:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Sep 2025 17:05:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Sep 2025 17:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 17:05:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Sep 2025 17:05:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d88b952b0f9bc0bb18e718e2da92b5706632023e4dd7ae5dd63450f6e59a147`  
		Last Modified: Thu, 11 Sep 2025 01:10:04 GMT  
		Size: 31.8 MB (31793375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2488a6c0b14f497398ac7b91b4ce102603804eb8c9ab2eebfa2796adac9c07d`  
		Last Modified: Thu, 11 Sep 2025 01:10:02 GMT  
		Size: 6.7 MB (6745353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d751615065600ec2f2f6e0c1e78355d32ebd9c98a21ecc28b99c0ab48da619a3`  
		Last Modified: Thu, 11 Sep 2025 01:10:02 GMT  
		Size: 1.4 MB (1430452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7536f07797663a5707a3c5591aa34b1d65d54a7083ce121eb26bb68f1ed44cb`  
		Last Modified: Thu, 11 Sep 2025 01:10:03 GMT  
		Size: 18.8 MB (18756471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e455450924bceccf4a1b9bf6c62ac0a1fa05ecc581224cdd7c34edf7525b83`  
		Last Modified: Thu, 11 Sep 2025 01:10:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b677d6f5f51ed26ae8381f2afa3550b01b4c55b0fc09129c912c6d8fb5ccc8`  
		Last Modified: Thu, 11 Sep 2025 01:10:02 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467194231603d970701c75215770c86cf2c060ebc5904a40bce54910e1e5fb9c`  
		Last Modified: Thu, 11 Sep 2025 01:10:03 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33944eccee608f69ea754056fce77af062199f5a7146ba72a256c91947f3a7cf`  
		Last Modified: Thu, 11 Sep 2025 01:10:03 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b855278c849b9d5431618c1ad2efaf5f6e4cab2c11916da2548c159c12df182f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3635326eef5502671eeb2c3cadffa4fe87959177f29ecd436c8e635231e81088`

```dockerfile
```

-	Layers:
	-	`sha256:5a062be07b75661a5b083b25ea291d19075197c14d43013123c145fd0c212776`  
		Last Modified: Thu, 11 Sep 2025 03:53:03 GMT  
		Size: 658.6 KB (658580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2e61cbbe87ae6833363dd19888e09029d92d0b9e3568529a160cec71e89b305`  
		Last Modified: Thu, 11 Sep 2025 03:53:04 GMT  
		Size: 3.0 MB (2999177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6e4e81b256e03363b63eccd078eb98803a70224bce13c897cfe8f845f968a86`  
		Last Modified: Thu, 11 Sep 2025 03:53:06 GMT  
		Size: 2.8 MB (2843023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa1fbaa0f7dc53696f444d20267883afc5384d91f1ca3770e72776029a28941`  
		Last Modified: Thu, 11 Sep 2025 03:53:07 GMT  
		Size: 59.7 KB (59674 bytes)  
		MIME: application/vnd.in-toto+json
