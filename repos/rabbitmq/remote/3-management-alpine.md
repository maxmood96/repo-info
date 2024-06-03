## `rabbitmq:3-management-alpine`

```console
$ docker pull rabbitmq@sha256:506754b291dde25382ddaae7f4fc87c29fa3316d77ba422c76e4fd2401dff90b
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

### `rabbitmq:3-management-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:f0858393ea9f058f1054de95952107800ed14b31b27ac478db2606068b830736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88972898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a339706d0272da1d48e6c7d94daf6981cd443b6a99269fa5e787bf08a35f7692`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.3
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c1666b2c13f3d2a5750b65b0dc5608a6c4595b58267ded3214a4f7b21d2f5b`  
		Last Modified: Mon, 03 Jun 2024 19:07:28 GMT  
		Size: 41.6 MB (41561262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8689f0214d1efd1ea522300fc7c8897263b3cc3bedf29b9c66ac2698c89e0b6`  
		Last Modified: Mon, 03 Jun 2024 19:07:29 GMT  
		Size: 7.6 MB (7567787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56356f4fc37373d8c84591858ccda010686589f182529a8802a56449b562b21`  
		Last Modified: Mon, 03 Jun 2024 19:07:28 GMT  
		Size: 2.4 MB (2405786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e09ac0aed3d874446fb1c4732d31e77b55f9e118adb2c4f3a0900b0d2930c3`  
		Last Modified: Mon, 03 Jun 2024 19:07:28 GMT  
		Size: 18.7 MB (18719256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea39665d8a9bd759dd94bdfbd1e4cb30b34b39e7a714c2a90d053d3173896df7`  
		Last Modified: Mon, 03 Jun 2024 19:07:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79fb845653d6565ffe55d487ea93009b77128bfb83e9fe8db52e94ed9b8e569`  
		Last Modified: Mon, 03 Jun 2024 19:07:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8339e1c57127d8efaed3889422430aa54dce6fe83d6348462a16857d0f541a`  
		Last Modified: Mon, 03 Jun 2024 19:07:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ed5c85134ced889eeefe949ec9a872ff5481c541980755ee639f463ed35c75`  
		Last Modified: Mon, 03 Jun 2024 19:07:30 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371b28ec2a29b14759fe00bd6daea416b8926f9356004a6fd690a137cbb6f8ce`  
		Last Modified: Mon, 03 Jun 2024 19:53:05 GMT  
		Size: 15.3 MB (15308329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:92aa5aee07dea7466ec0beacf4fa3a103415e03eed228cdffd6d1be34b81cedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2053532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35a072eab068d3a25c5b515b71f5fc1661a18d72a7fdbd088cbdf8f6e0bc972`

```dockerfile
```

-	Layers:
	-	`sha256:affe0b8a63d13615d789aaaf9610359ff7ec016bd80776e7d923fe0280bf46af`  
		Last Modified: Mon, 03 Jun 2024 19:53:04 GMT  
		Size: 2.0 MB (2042385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c601754ea83fd4bbf4a5e7616b43585fd53c1f44fb17024ed8136fb9a4f773`  
		Last Modified: Mon, 03 Jun 2024 19:53:04 GMT  
		Size: 11.1 KB (11147 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:cad0ba3423de900d915a47f527141e06987113ae744988c73e71a87296092d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78835138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9219683e4b97d46ec1786bd4f9de73bc57d6f1cd36973e8de11cfdfefc13593`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00607d26fe4ad540fa2d3ebaedc81d0b83b84a5ec9aef2e35343e4ce5f875d7d`  
		Last Modified: Fri, 03 May 2024 00:04:34 GMT  
		Size: 33.2 MB (33180623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde0fbd1fe43760aa096f29012565b371973403f1d1f661180f9851d8d43229f`  
		Last Modified: Fri, 03 May 2024 00:04:33 GMT  
		Size: 6.4 MB (6400980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200bcbdd504f1c13f69059319477d019fbd5844e3c8eac86a17644d686b27715`  
		Last Modified: Fri, 03 May 2024 00:04:33 GMT  
		Size: 1.4 MB (1401666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e791228781b85f5136a0e33313dec603c93dc9bdc9163304d1552da74845412a`  
		Last Modified: Fri, 03 May 2024 00:04:33 GMT  
		Size: 18.7 MB (18706563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec614562b08f0d8aaecfe64e1d01675d0bcf4823ff196ece9dceeae99f201cd`  
		Last Modified: Fri, 03 May 2024 00:04:34 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c2c0bdbded48cfac4fe2b2e78b4d011d477cd214000ef6290437cc1bb239b8`  
		Last Modified: Fri, 03 May 2024 00:04:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81254efba9881a07842367c12c744d565bc6df19702e87f176e89e7d69ac758b`  
		Last Modified: Fri, 03 May 2024 00:04:35 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9357eb389a3acb563ef8fe0e196cd87173bbe315a3621fbc13eddc013e79fb8`  
		Last Modified: Fri, 03 May 2024 00:04:35 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757b645f2768764fbf7fe67d7178613ecff358485de358de0c0bd9a28d5a455`  
		Last Modified: Fri, 03 May 2024 00:56:51 GMT  
		Size: 16.0 MB (15978163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5da08d60b0defe28846bac0930cb247fae9afa76d4ffcef917bf5399128c59b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3c4828ad8c80780d4635d2f564b5070fb71d74820b2d7c494f9791bab79e02`

```dockerfile
```

-	Layers:
	-	`sha256:3a22a9c3cf58d2633d4e9ab6405a2cebc46dc84f5c59043b6a0f2894c40a89a5`  
		Last Modified: Fri, 03 May 2024 00:56:48 GMT  
		Size: 12.4 KB (12432 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:2ab6f5d2fc466aecbece4765a4d7a4622a4073fa21c9dad2871f18311dfb64b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77729030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937f07ad521dd1c644709bb300763deaef453a641a9b62e28a873d7f91017f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8161d8f3e6dc629e15a16b01b9791a16c8529b37abccc2afcfbf3a17d9f5bce5`  
		Last Modified: Fri, 03 May 2024 00:22:46 GMT  
		Size: 33.1 MB (33080541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e4557c740fb15b47eece7174157004d20779729dd2e9ae8bb6107caf8a86f`  
		Last Modified: Fri, 03 May 2024 00:22:45 GMT  
		Size: 6.1 MB (6099224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b468f5d884bed8d02c8db363ac490e31f132ee0c89f3304e1ef934e3338dedd`  
		Last Modified: Fri, 03 May 2024 00:22:45 GMT  
		Size: 1.3 MB (1305609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a6b3daf8faeebe6aeb8e0b00404d3184d7642b960a27923d6558d642d3a7d1`  
		Last Modified: Fri, 03 May 2024 00:22:46 GMT  
		Size: 18.7 MB (18706661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3557657b03755a80d67a37bbc1c4050a8de0fbc9e817aaa865a07f23b71fc41`  
		Last Modified: Fri, 03 May 2024 00:22:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1860e55de1b1f0aaa2e70b506476b2bf38b0ad164aba14201f98973b2b380b7f`  
		Last Modified: Fri, 03 May 2024 00:22:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cf48eec463d2bc5bf3760f086e7d50b4c7782474af0a8bbd28a109652a780a`  
		Last Modified: Fri, 03 May 2024 00:22:47 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c6e7335c47001246e8fc6c54c7f634d9ce612c5cec8c36a6225f9596564d3d`  
		Last Modified: Fri, 03 May 2024 00:22:47 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d8ec0a8cb7aff97d0002481f524b3df68abab80bb647b7fadf6098590300f`  
		Last Modified: Fri, 03 May 2024 01:08:42 GMT  
		Size: 15.6 MB (15616348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0add98d368b4cc97e74004b4d91b93bd64b73f81656bb9d185dc92a17b2ff690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7a375085ec14cbf5a74040daeebddf41f3260cbbe735c937628095437897b6`

```dockerfile
```

-	Layers:
	-	`sha256:02d571f5d71d2bf8522fd523f34e172617b3d8841fa05eb96847faceec658ca0`  
		Last Modified: Fri, 03 May 2024 01:08:41 GMT  
		Size: 2.0 MB (2041710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e52490d371825aad0276280a09c1cf1cc138d4e18b688b8daa16bc08f8971ff`  
		Last Modified: Fri, 03 May 2024 01:08:41 GMT  
		Size: 12.7 KB (12651 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:1c2afb134fbd71aba3e1628034153513af3b16108962df906d2304aab0a6a0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86899418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbb2b598031f24612e3a4d245cf40aa15ee1a085955c8687e49e9fc37563931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5c8847845aed6a3781a464cd18365e0cda3688f2c241c55ecebdeb203b8bad`  
		Last Modified: Fri, 03 May 2024 02:42:38 GMT  
		Size: 39.7 MB (39682713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2663a3b03050496c42d29e24ec56507e1cf57f6c1e3951b4e79a9031be8a04f1`  
		Last Modified: Fri, 03 May 2024 02:42:38 GMT  
		Size: 7.2 MB (7189423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988d62de9ae0ebc881db8c3b6a859a4e704ff8cadb35fd3b7876626d9e6f522c`  
		Last Modified: Fri, 03 May 2024 02:42:37 GMT  
		Size: 2.5 MB (2489919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83702914d34cdb65958d40296fc6cc6cec1970f476a470cc55db55176b23c297`  
		Last Modified: Fri, 03 May 2024 02:42:38 GMT  
		Size: 18.7 MB (18706463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1b309f49ae40426ade76a42d7f70b47b4f8561c36d8b2d931b694922d770f`  
		Last Modified: Fri, 03 May 2024 02:42:39 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d071db94b20101f9b7f6669d732263f6a9f7f54ce5b245c4ac254c70eef7ff`  
		Last Modified: Fri, 03 May 2024 02:42:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4df7a5ad30f4e860c2b758a1c7e8a4020033db38087fafa4c7203647d40aed`  
		Last Modified: Fri, 03 May 2024 02:42:40 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b61a2f13c3e01d4f126db8d49883ef456eac5a30e1de994f234d85a932f1fd`  
		Last Modified: Fri, 03 May 2024 02:42:40 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0e8f8d0a0d8fbb4061737b14c6dae0319e7b35a7517854ee55e4fd57a07163`  
		Last Modified: Fri, 03 May 2024 03:41:53 GMT  
		Size: 15.5 MB (15481440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4dc52b69050bfee36998859b0cf8f13eafe9ec70b7c2ee5cba08b47f5b29bb1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c9b7b7c5c331564eccfd722fe774940d1dbfead63a956c3763e3e9c2939e58`

```dockerfile
```

-	Layers:
	-	`sha256:530728582fbae64af8f734962678b69e573da7e8ff26ea596536a8eb9f0ea453`  
		Last Modified: Fri, 03 May 2024 03:41:52 GMT  
		Size: 2.0 MB (2041515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:819f2514c40647c43f4649ce31d7e3cddead2e199b6e9f81b91fe8e9f483fb1b`  
		Last Modified: Fri, 03 May 2024 03:41:52 GMT  
		Size: 12.6 KB (12591 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:a311771183009f3330f15f0794e147ffbd812bb2614aee3b4cdce34462b27e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80961199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ca533b542c9331987dcf0d86fcbea5e048f7a4dc95393018451d366eb4b40d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.3
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53472ed25a544a2c9730d214f55d7477d8ee092d1bf0575e65e631f5f723cb9e`  
		Last Modified: Mon, 03 Jun 2024 19:07:12 GMT  
		Size: 33.4 MB (33354190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d2af33ef152852dfb8b63d32ac038dbbc4703e5a6e186a22e49e0d7ae27b6`  
		Last Modified: Mon, 03 Jun 2024 19:07:11 GMT  
		Size: 7.5 MB (7493804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8378d080afb47187f121c808a43cd801cfa2f96698fb90b1c1a348f72ae0c8d`  
		Last Modified: Mon, 03 Jun 2024 19:07:11 GMT  
		Size: 1.4 MB (1404308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfad940a067639142a1f3f6e34ea8e3cf541329532e85f7ae72da6aaac143cc`  
		Last Modified: Mon, 03 Jun 2024 19:07:11 GMT  
		Size: 18.7 MB (18719521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b52dab1b97db73bf3b7ca9d0a735fdaa01c2da23ea118f1340f29457c90c698`  
		Last Modified: Mon, 03 Jun 2024 19:07:11 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1f9e3f8003675c836ed02a363fd0839107ab26c4437a22f3aa653a98f36946`  
		Last Modified: Mon, 03 Jun 2024 19:07:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e57411cc62cc7dcbaded2c08390453c0b2be95f853bb0ecbcc0e657987460fa`  
		Last Modified: Mon, 03 Jun 2024 19:07:12 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87a85befad7a6b27a755e0f77b5a7927ba3cf648057128edec0e41ce165cbfb`  
		Last Modified: Mon, 03 Jun 2024 19:07:12 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261373f74f8828c268464cf14cb34d58f7d8984fdb089e5f8206e76a19aeeb82`  
		Last Modified: Mon, 03 Jun 2024 19:53:05 GMT  
		Size: 16.7 MB (16743538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2737fa6653de136dad2b4556a594604ce354c5336a54adfc95c78e6dff1f745b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2053305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ee1f5b8985b307d7e79800d224dd6bd9a8c2c70e9c20eb9ec30f766cf96c3f`

```dockerfile
```

-	Layers:
	-	`sha256:a24b31bcba611f0edd22af8014fba8b10dca212962d0f4188de101cd28a387fb`  
		Last Modified: Mon, 03 Jun 2024 19:53:04 GMT  
		Size: 2.0 MB (2042190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd4bf700e95929d8ae5a9ecbad9acdb74ceb2a49759406f3cf316ca9d455b5d`  
		Last Modified: Mon, 03 Jun 2024 19:53:04 GMT  
		Size: 11.1 KB (11115 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:dacd1fd9631bb2af17a150199239b0a576cdbd83e3c9e04cd83119ca8f5a14ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81978761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f9f30e4b6dab73f70be7aed17d3008be0683a000c2116588b25401af37596b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceef9865cd34272590a2110e6313647be4032492b52d578256780578e8aa295`  
		Last Modified: Fri, 03 May 2024 00:37:44 GMT  
		Size: 33.6 MB (33609094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2201192a44ea3615320ba0dc078ef7e6e479967aba6fdc940709320fcdbeb67e`  
		Last Modified: Fri, 03 May 2024 00:37:42 GMT  
		Size: 8.0 MB (7981827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d9765c2cf3f0f21ed63b9d85bd3bdc520bda649ebbe494237c0c4c5eaa963a`  
		Last Modified: Fri, 03 May 2024 00:37:42 GMT  
		Size: 1.5 MB (1515653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7d00daa5f30911b18b0b17ba8f7949835f97b13d3e5578838848fa16d1d011`  
		Last Modified: Fri, 03 May 2024 00:37:43 GMT  
		Size: 18.7 MB (18706732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a454a180738293f6427053c6b31e2a0bbee5bf5a65d1de8b5dacc9bbfd4312`  
		Last Modified: Fri, 03 May 2024 00:37:43 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8fdd367788818d3a2331910c4679f81b74ec96708b90f0be2c53c925b670c`  
		Last Modified: Fri, 03 May 2024 00:37:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8680b7829f83cb50fb42874790d3f27a405c1c9e07638e46a6641e4ee2e68430`  
		Last Modified: Fri, 03 May 2024 00:37:45 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdac70d89d39b8eb7562de2794afdad79f5f70a8b1e63bc36f66e1abdb5e544f`  
		Last Modified: Fri, 03 May 2024 00:37:44 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114a8c686363304299146379d40a17f0c91c27f2e10ba26e502a4471f7aaf2e`  
		Last Modified: Fri, 03 May 2024 01:18:31 GMT  
		Size: 16.8 MB (16805352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c463417ad80dd9721fa6223cd42784aeb2531ad2fe9c942a813f3ccc30b1e512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2052543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93bc4bfc5e636f0e3f2fe824275b4659458bfff40f77346ee4b18a25190fae3`

```dockerfile
```

-	Layers:
	-	`sha256:867a3cac05da663d6f2652290846d4b8c877acf6be454267fd31920aaa65a68e`  
		Last Modified: Fri, 03 May 2024 01:18:30 GMT  
		Size: 2.0 MB (2039924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832190b74ec0c6a26b7d38de5cf3dca70ef2fc6051a1051462bdabe09c3d92e0`  
		Last Modified: Fri, 03 May 2024 01:18:29 GMT  
		Size: 12.6 KB (12619 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:4d3ce0e68d7d31418f257b276f0962f84d0b7b059e15555cf8297daa98f90880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80592905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186eff7b864ac7f26f8ff6d49b407d050af3b9eb6cc2c326523c18e8650d3e14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.2
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b171ae1b998ab06ec70ad1b55143dc513c163f4039a481861e0866329910f6`  
		Last Modified: Fri, 03 May 2024 00:45:55 GMT  
		Size: 33.7 MB (33684742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7015fd44ec9d29c9e3903af7006a9ed877f23aad3fbbe4b2d64c6b84d610f7`  
		Last Modified: Fri, 03 May 2024 00:45:55 GMT  
		Size: 6.7 MB (6706511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2695f2206d9968a4a860020a840f4722608fd63b011b01f3e69bcfdbe6070a04`  
		Last Modified: Fri, 03 May 2024 00:45:55 GMT  
		Size: 1.5 MB (1496506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70ed73bc995913dcb9c9099c6c33e7177611bc361f5c8ff105b865e295a9a6`  
		Last Modified: Fri, 03 May 2024 00:45:55 GMT  
		Size: 18.7 MB (18706676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c5a2f031506766bcc7d486e100e7fab84884dd4cc27c3cedebf4b603b11705`  
		Last Modified: Fri, 03 May 2024 00:45:56 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6fd924d86509ac09becfb9cec284555a62205dff0b3eacbbbb9a62b32d24db`  
		Last Modified: Fri, 03 May 2024 00:45:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7077dd2809b3644f2bf6ea7a946c580f49138db9ea88e1c10c481bfeeb069f`  
		Last Modified: Fri, 03 May 2024 00:45:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49606ee0d2f62b9ade0c594d89c01a0c6797c3db14494ae4bb551ad8196b5c39`  
		Last Modified: Fri, 03 May 2024 00:45:57 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a8c4f05972b063e989261a18aca81dc10fb3d1af1cddc8365fb152a3463b4a`  
		Last Modified: Fri, 03 May 2024 01:19:25 GMT  
		Size: 16.8 MB (16754084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fed4568812b193e86c5b2acf17fc481cc116d408b121d897ddc21230d7c9bfc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b4d23e7cc56b7314820fb3bd2db5eb30be5622adf35561754cf8ab52b55242`

```dockerfile
```

-	Layers:
	-	`sha256:fd624204f43db1e3afff0b160e1f48f5651f5ce24d30df9e3ddcdcfff44b5d91`  
		Last Modified: Fri, 03 May 2024 01:19:24 GMT  
		Size: 2.0 MB (2039380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61b7ba87972c384eadcadfb33f1bbb60544a5f2423c691fe1b6bc731dd7451e`  
		Last Modified: Fri, 03 May 2024 01:19:24 GMT  
		Size: 12.6 KB (12575 bytes)  
		MIME: application/vnd.in-toto+json
