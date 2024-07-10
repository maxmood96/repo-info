## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:4d69261ff51b786d0137568264ebe799f57802069eab62d9ac6d8e94f51b6bf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:3-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:e4f262decc7d674cc908ac94f7265e3048c20115e548d2baa0e534ca456fdb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73656202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699e1b0aa33d9e1e4d78055991755e3a51d222e216a55d047ee478f2ccef9133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jul 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jul 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jul 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c2c43635a6c3af9bdf9475c24e9376d762cd31163cada832523d5d29207a08`  
		Last Modified: Wed, 10 Jul 2024 18:09:11 GMT  
		Size: 41.6 MB (41565162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6cc05955edf897be1602334954630036124978454c38aee224e5b29579e3b6`  
		Last Modified: Wed, 10 Jul 2024 18:09:10 GMT  
		Size: 7.6 MB (7578161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61361850cebe1dc3cb8fab243221c40edd6dd87c82463e658d393d560a91e521`  
		Last Modified: Wed, 10 Jul 2024 18:09:10 GMT  
		Size: 2.4 MB (2405760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9387cf68524b0ffb280195f2f6e0cde15a1d56b9fe5ef193c0efb52159a6b283`  
		Last Modified: Wed, 10 Jul 2024 18:09:10 GMT  
		Size: 18.7 MB (18688036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a0498477f4335a26ca6b22e62108e0afac50e2141ed517517272b491a6c72b`  
		Last Modified: Wed, 10 Jul 2024 18:09:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b8d9b88589ba3fbcf317ec4a80ab4cb36073d18fb6824ed6d6888422b1685c`  
		Last Modified: Wed, 10 Jul 2024 18:09:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f7844dc2a22996628f34b0ab2bb74e594d0e370821d8e3eb33b938d053ea6`  
		Last Modified: Wed, 10 Jul 2024 18:09:12 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0b5b8744de0d4ad3e277885f859f51719e9523c6f1c27a51b8ffddb7a2b61d`  
		Last Modified: Wed, 10 Jul 2024 18:09:12 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2ac8371637c5fa83869e8766a7b29f912f82b6f69e4e1bc2dfcdce428aa64418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6745517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac58958bdcf9560adeae7cabf85ff7007eafe5a1189b132707d11aaebaf8b11c`

```dockerfile
```

-	Layers:
	-	`sha256:79da2fa3040812e480a84aeefc7b2e7a611fd7a35a93fd280c9dde75def2a962`  
		Last Modified: Wed, 10 Jul 2024 18:09:10 GMT  
		Size: 999.0 KB (998958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54a0f5ef1470d10a1cd815579e96d72bcb602ec02aa4f972c28a5aba08983fa3`  
		Last Modified: Wed, 10 Jul 2024 18:09:10 GMT  
		Size: 2.9 MB (2903571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:455cbc6e85817c522df170d3642987af12f8572e80bc06dfb3d85d4fe251ca36`  
		Last Modified: Wed, 10 Jul 2024 18:09:10 GMT  
		Size: 2.8 MB (2781449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3577340f8f82e013c71922727e9eee601d8c78226ecc27398a6c670514ec6eac`  
		Last Modified: Wed, 10 Jul 2024 18:09:10 GMT  
		Size: 61.5 KB (61539 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:b39ea4dc46934d2578684ad4b5c2e9406f189f184574baf63026e08c739f1ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62853008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7341271588075554c47ef326dbe9294959e4461d5e16f447f7f849b7c8023246`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jul 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jul 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jul 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3334f096e59e131ee1ee2d5ad6e49b83d9c72183d3386d7196ca930cfeecbda1`  
		Last Modified: Wed, 10 Jul 2024 18:05:15 GMT  
		Size: 33.2 MB (33181757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b83794296b0ad7f4419929fdbbc27f8dd51370a1e23c195d5adb14a06f65b7f`  
		Last Modified: Wed, 10 Jul 2024 18:05:15 GMT  
		Size: 6.4 MB (6406020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0320492edcd3a4c1604cf75e18fdf4c2d034fbc7f7d97b40c7fda0eccab10c94`  
		Last Modified: Wed, 10 Jul 2024 18:05:14 GMT  
		Size: 1.4 MB (1401698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd47de3c43a0c975f48f3c81508636e98908be3e5dc9413add041bb2cabd1835`  
		Last Modified: Wed, 10 Jul 2024 18:05:15 GMT  
		Size: 18.7 MB (18687877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a9a0312d1ac4dba59711860570a8ad4957c7ec0245c4ac22ebfdb9260aa8ad`  
		Last Modified: Wed, 10 Jul 2024 18:05:15 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ea2926e7b7282761ef8d867783646e0f0668bb417961f95353007f92278c4c`  
		Last Modified: Wed, 10 Jul 2024 18:05:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e8fef9754a53e3270214c2d21836bea9b0640245d11b8af34cb3ae471209ca`  
		Last Modified: Wed, 10 Jul 2024 18:05:16 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6effe67595f86eda623dfc463f92fbc532fdc86f6fbd029f607b794629df4b44`  
		Last Modified: Wed, 10 Jul 2024 18:05:17 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7ff9840ffe0ff4612daeb743f5f33d0e023ec0c0d73d2290a9ba0014252ef6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 KB (61507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff24e038bb5d89a6f4b5437a75e437fb429389b409f17e80927ed78265ff9a8`

```dockerfile
```

-	Layers:
	-	`sha256:f81b0fda875fca90ceecdda5f3072eae28b94d274b92947574b80fb878abcde6`  
		Last Modified: Wed, 10 Jul 2024 18:05:14 GMT  
		Size: 61.5 KB (61507 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:0c6265d01c5a941d1288566040531db847f92d7a6931ab7e2e508237e5ae534c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62112276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c863cbb978a81378222d20dc9f2c989a4012805c61d4af259cb152d94a41da1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:32 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Thu, 20 Jun 2024 18:00:32 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jul 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jul 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jul 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254598cb4fc93da43910bfc9f1479631212334795f7c458fc2903c8cc576412`  
		Last Modified: Wed, 10 Jul 2024 18:10:22 GMT  
		Size: 33.1 MB (33083927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d94790621fadb9e1b965cd55f71554804f394ca920539d518ef4c384ca9caa5`  
		Last Modified: Wed, 10 Jul 2024 18:10:21 GMT  
		Size: 6.1 MB (6106923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0723f71177f0a31f64b7dcb5ffe2d988c5d826e32e60aac676f238672506b522`  
		Last Modified: Wed, 10 Jul 2024 18:10:21 GMT  
		Size: 1.3 MB (1305640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25ceae77d0c7d524d0de4176afd58bdb5635e3fb41115a4929e95dcc1f40f23`  
		Last Modified: Wed, 10 Jul 2024 18:10:22 GMT  
		Size: 18.7 MB (18687539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365603b9f8219ab56fc6a311e019732676c84c9ccfc6c7dcaa30540f50e49604`  
		Last Modified: Wed, 10 Jul 2024 18:10:22 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86220be2c8f1e7642e6a141e23ee2857dbe137e24d0140f97195942bcd498849`  
		Last Modified: Wed, 10 Jul 2024 18:10:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5779233b369fc1d03958d89b3cce8e3752b980715eba3b5af48b6a623eb290`  
		Last Modified: Wed, 10 Jul 2024 18:10:23 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad6fb3a59a80992c6270f8dc4012f4fc91fadc3754bd69bc4620f4168f69609`  
		Last Modified: Wed, 10 Jul 2024 18:10:23 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e25dabd9f3c12d819ac6d13e7f85e6ab85f9f40b5d1310267c80c1ad2aebf860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6539615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac19a3bbecbb9e9d603076f30e26b2e67140610ec4fd30805887ae527f25b5c`

```dockerfile
```

-	Layers:
	-	`sha256:7e2cfd822f11d3d1c95d6dfd34d65c89e2fd7b9494a4eaf89b7f75f8f02f00ca`  
		Last Modified: Wed, 10 Jul 2024 18:10:21 GMT  
		Size: 995.4 KB (995352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e82db84fc7012ec066a9dba0d82325a75c1c281f17cae5b4779dcd3cfccd2865`  
		Last Modified: Wed, 10 Jul 2024 18:10:21 GMT  
		Size: 2.8 MB (2802886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c00528e005242f1a803ed0bad6222cf06c544c9627c474fabbb90545b49a43`  
		Last Modified: Wed, 10 Jul 2024 18:10:21 GMT  
		Size: 2.7 MB (2679653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e5340ef087bc36bf506432c2833a6f93159d8067d9208510ae3d978d6ca46a`  
		Last Modified: Wed, 10 Jul 2024 18:10:21 GMT  
		Size: 61.7 KB (61724 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:4126ff14641b1d8dd80cdef84f5ed949b56fed191ee2043387106aa423e525e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71422632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a36f1b94241b8cd282aceed182c78492a2f73bdffe06e4c75aafd45ba370ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jul 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jul 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jul 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fceda3e307722ad140549db7183261a480ff9f6c29e7ea07aa44bea4702286`  
		Last Modified: Wed, 10 Jul 2024 18:11:03 GMT  
		Size: 39.7 MB (39684775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a757b103424c1afc4f4cd5e0c8f8d19d6ef4d649e263eeda1fe9cfe2b13e5`  
		Last Modified: Wed, 10 Jul 2024 18:11:02 GMT  
		Size: 7.2 MB (7200836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b50762e28f88d0e3706f6bc3090f6f9615fc0b60f03a6538dd8c907a8cf2c9`  
		Last Modified: Wed, 10 Jul 2024 18:11:02 GMT  
		Size: 2.5 MB (2490009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124cf2483fd87a43d555d8f162d70b6704271f3d249a75a05421abf1942191c6`  
		Last Modified: Wed, 10 Jul 2024 18:11:03 GMT  
		Size: 18.7 MB (18688059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f3913a3262581f4da4ec6eb74e93793f444b038e8f43130794dfa953b0f11`  
		Last Modified: Wed, 10 Jul 2024 18:11:03 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9196b63abc8bf356d7c7a6a4e611fd44009578c73aa5c66ddaa9b65cb976b9b0`  
		Last Modified: Wed, 10 Jul 2024 18:11:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8505111e0124060b5c1c06d5d2277ba7a4dcd341287833d7fa789fcb1fac52`  
		Last Modified: Wed, 10 Jul 2024 18:11:04 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e75bc17569e83df6ed022bddb9728ea35423c987d257abc9e9936232f4fe4ce`  
		Last Modified: Wed, 10 Jul 2024 18:11:05 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:81c539df2fcb8e6855325a8fae7ab9ac99434ffdebb7daa7aa89bb343769e63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94662b40ee4bd4ad441826753e397cac093996d91768376668ae7eb539fbc7ca`

```dockerfile
```

-	Layers:
	-	`sha256:f63dbad67a5234dcf830b1795f775f5ba2c347817123ee4e6d7eeaf6ee7d5499`  
		Last Modified: Wed, 10 Jul 2024 18:11:02 GMT  
		Size: 999.6 KB (999646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c9246425c8670c2e0aa10258245d0e548f31f0d0d354d1589b31d0c3da7dd63`  
		Last Modified: Wed, 10 Jul 2024 18:11:02 GMT  
		Size: 2.9 MB (2920819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da05ca8ea88e32abc15e9f3ec0a5d46b59199a1181a0fa53e18c9444db52aa02`  
		Last Modified: Wed, 10 Jul 2024 18:11:02 GMT  
		Size: 2.8 MB (2797590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd4ef0de43be0062d34fb51227cc899692b1dc84f6ebd1957003a27098cf60a`  
		Last Modified: Wed, 10 Jul 2024 18:11:01 GMT  
		Size: 61.8 KB (61839 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:a0436fa0b217aa92198b3cfaee0499b648ca5a6e1f45393ea9b7c110da63ba37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64205419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9081915dfef883a26fc00f58c7cf001c7d7b32945d40caf41158ebb4850d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:29 GMT
ADD file:fef5870f3bb90ed437c0331d7e65e52da6728b66d231aea95a605935fef056d7 in / 
# Thu, 20 Jun 2024 17:38:29 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jul 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jul 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jul 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e9c6bf0d8f3154c26ee87ffe9feb02c91666069b8cbe0668cfae10922ad80c49`  
		Last Modified: Thu, 20 Jun 2024 17:39:06 GMT  
		Size: 3.3 MB (3250890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f02d805e089e78ce70e89dd2ee13124dcde76730992c1f9710ecb2e4c9f7ba`  
		Last Modified: Wed, 10 Jul 2024 18:08:18 GMT  
		Size: 33.4 MB (33356089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89398f1f1beae3c61a30b40036d903bc6d65ed5f117225848707dc4ebea3202f`  
		Last Modified: Wed, 10 Jul 2024 18:08:17 GMT  
		Size: 7.5 MB (7504786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8f9c4cc198418a3f58db3ebeac3ff8afc5a85064d889a612fc52ad5cb60e64`  
		Last Modified: Wed, 10 Jul 2024 18:08:17 GMT  
		Size: 1.4 MB (1404394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c57fd46cb831975329fb2114edb9ae62891c264c6eb21062798cca143e3fe6`  
		Last Modified: Wed, 10 Jul 2024 18:08:19 GMT  
		Size: 18.7 MB (18687508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ffbe3a9a9022d8c1f958c55ab58337f3d99166ec7b7b5bb4d8f35e44e6c1a7`  
		Last Modified: Wed, 10 Jul 2024 18:08:18 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c11f0d6a2b4ce6b325e5532c3aa66583827b76b1538fed2cef38be911b2a0e`  
		Last Modified: Wed, 10 Jul 2024 18:08:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a6a6fb3e862bf5ac322394683154a26079cd416fc9c51852008af5653247c3`  
		Last Modified: Wed, 10 Jul 2024 18:08:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3787a7888b20713c1866e683619d514fca43cf369faa70cb34ba89838f1ec8`  
		Last Modified: Wed, 10 Jul 2024 18:08:19 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a9610f2746249fc093b29c4fa209e5d0ff48d0d5bc76ef228dc553ad815b343d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6721617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b39c466241764ae1a7e4b148a93159dffa1d659c2f68ae324bade6161d617a4`

```dockerfile
```

-	Layers:
	-	`sha256:77de19216e0eac15139d735bff22dea69683d681459e443a711a4a0688d55409`  
		Last Modified: Wed, 10 Jul 2024 18:08:17 GMT  
		Size: 994.7 KB (994659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac96d5e6db9fc6a6937606b0eeac9db56d74d675b487a0b105990b570f5c2e61`  
		Last Modified: Wed, 10 Jul 2024 18:08:17 GMT  
		Size: 2.9 MB (2893793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ecaa1d00d1ab90f8a33e6a4b16894b411bb8383f50904fd897cee719c8a8c31`  
		Last Modified: Wed, 10 Jul 2024 18:08:17 GMT  
		Size: 2.8 MB (2771673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04acb16bcd9dcdf458f298fef98c2054e6f2fc491c78ef84842ffa121fe7c13`  
		Last Modified: Wed, 10 Jul 2024 18:08:17 GMT  
		Size: 61.5 KB (61492 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:bbdc72283e31723ed8c98452b74015c456f424d934fe5d61a27ac2b18f2717fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65171274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c58c3f12fb7295e9d54268d01fcdc97cf2ddf894611c2c3db47098faaf9cbc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jul 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jul 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jul 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6dc387746c90f018fce9b6b99873606a0ffd76c16e7c6558b38525edca108d`  
		Last Modified: Wed, 10 Jul 2024 18:14:18 GMT  
		Size: 33.6 MB (33612843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eca75a03cc905525880a1ed2f845987b0f23719ff15e267fe23a241f7d1d4b`  
		Last Modified: Wed, 10 Jul 2024 18:14:17 GMT  
		Size: 8.0 MB (7992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0922a6eb6bccf1dd8232db9bdf0db1f76fe777ec67f178d62279c0e9ac751f58`  
		Last Modified: Wed, 10 Jul 2024 18:14:17 GMT  
		Size: 1.5 MB (1515699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3808f6b6c33897edd3fc84ef3cb5e3cc1bfae52fefed89014efb9c22f91da88`  
		Last Modified: Wed, 10 Jul 2024 18:14:17 GMT  
		Size: 18.7 MB (18687480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb960824df5c0cf4a21b6c7f90e67f116fa3380062033fa7b55fd3278b04e51e`  
		Last Modified: Wed, 10 Jul 2024 18:14:18 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022505369290b31de14fa400be58e590de22ef3fb4ddce1be03450882279f566`  
		Last Modified: Wed, 10 Jul 2024 18:14:18 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa42ff36ea04746b029b9340fb33f54973737d46e4c14b29887906b180757f25`  
		Last Modified: Wed, 10 Jul 2024 18:14:19 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea187331f04ecc2fa6c9ef57ef2f552bf21f111626d843c5cfe8eac65e53568`  
		Last Modified: Wed, 10 Jul 2024 18:14:19 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2da0cdfa106d527f1b27d08b52bc8da9d6992561f7ac2e8ff592e19529ad362c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6718330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c42f956c377df48723cde876ec4e4077cb65c3cf398e50893d3814e04f3d176`

```dockerfile
```

-	Layers:
	-	`sha256:d7a18929dd5f2c765569c1ebb0fcadb7b582610544ac3e8fa763250e02e48ee9`  
		Last Modified: Wed, 10 Jul 2024 18:14:16 GMT  
		Size: 993.4 KB (993396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f36db4b5083df6160ceacdaeec883f6d36d5cbd9136e32c4bc4534b5dd639c52`  
		Last Modified: Wed, 10 Jul 2024 18:14:17 GMT  
		Size: 2.9 MB (2893289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd7249239da6d0d8071d13e452767c16daf35cee3386d3caf955d2cf3418dbbf`  
		Last Modified: Wed, 10 Jul 2024 18:14:17 GMT  
		Size: 2.8 MB (2770052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37af4494b023971defeee588cbe083e29fb13845ba70eead367acbdd58e12eaa`  
		Last Modified: Wed, 10 Jul 2024 18:14:16 GMT  
		Size: 61.6 KB (61593 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:6024be8cddbe6cb0954557f91ae82832d4555a55b1f05a29a18991529bab3234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63847871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1716552c9c8a34a8c6b6875391be5394d315cf0ab9ea829199c7aca43764b28b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jul 2024 11:05:22 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_VERSION=3.13.4
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jul 2024 11:05:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 11:05:22 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 10 Jul 2024 11:05:22 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 10 Jul 2024 11:05:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 10 Jul 2024 11:05:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jul 2024 11:05:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jul 2024 11:05:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 10 Jul 2024 11:05:22 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6ccad83c4803fbe91ecd2f681435deba8aacfcfff5fb38b99eeebfd8dd20cf`  
		Last Modified: Wed, 10 Jul 2024 18:12:25 GMT  
		Size: 33.7 MB (33687895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818b1220e98bca151b1d7b53b65113c3466ac465b6a6f39ee90ee4a71dcc26e8`  
		Last Modified: Wed, 10 Jul 2024 18:12:25 GMT  
		Size: 6.7 MB (6721777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae3e4008f3a5aa1de8db6974539fa26277b770bd6fb7738f896725a34f2e49f`  
		Last Modified: Wed, 10 Jul 2024 18:12:24 GMT  
		Size: 1.5 MB (1496561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa175d058ef8131d14e23eb962fe7773ccb71e3a23b4e2920b2af349813cb67`  
		Last Modified: Wed, 10 Jul 2024 18:12:25 GMT  
		Size: 18.7 MB (18687397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035a8488d0c66c8ea0ab32da6da3ea158117badaf842482816223ea3fd4a62ed`  
		Last Modified: Wed, 10 Jul 2024 18:12:25 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e243e643d130606d00e5fe3dcd4a1743864660cc2fc1183cfdf499892c0552a`  
		Last Modified: Wed, 10 Jul 2024 18:12:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c18d0e362f05c2c6b7c33fc58028afc8a519db4412f5dd3e5430dea09d56da5`  
		Last Modified: Wed, 10 Jul 2024 18:12:26 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8071edb104bee8f8a8d73c50f8b4f8381a5077430304c997208bef2f161e9201`  
		Last Modified: Wed, 10 Jul 2024 18:12:26 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:82663e69b601824a4e20e976a659d0b9408b4c54da96f30fd3a622c6d404b985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6552399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70cd5d59c17db5617197ef33224ffe817c82e3709ace52919148f66f06f8e96`

```dockerfile
```

-	Layers:
	-	`sha256:ce623a8a51ca8e44dfdd3087a20026d3de644fac2788d95ee83ffbfa0203c30b`  
		Last Modified: Wed, 10 Jul 2024 18:12:25 GMT  
		Size: 993.4 KB (993362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e8b11ef732fac9b0acec019a766d808439f69093f95cbe4482b276a8d27ddc`  
		Last Modified: Wed, 10 Jul 2024 18:12:24 GMT  
		Size: 2.8 MB (2810358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa6235739319ac486f26767f56324c1e58b3f4b14de5b8ba94e16a58ebf1d85`  
		Last Modified: Wed, 10 Jul 2024 18:12:24 GMT  
		Size: 2.7 MB (2687141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b0ee5cae9422d99d5d0549a10bb12b6408c713141da6c6d1c663c125eb2c0a`  
		Last Modified: Wed, 10 Jul 2024 18:12:24 GMT  
		Size: 61.5 KB (61538 bytes)  
		MIME: application/vnd.in-toto+json
