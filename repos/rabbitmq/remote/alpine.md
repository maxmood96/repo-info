## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:8489bba72d91465b2ed422394966d270858252844cc7bd91dfb8ab3dd43fdaea
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
$ docker pull rabbitmq@sha256:60f00ad7ba2c53f4e12149e24f3a112907bbe598b5d0a4cfa9f6fc387177071e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84164602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b67972411c95a578353fb325d9d9653d2e531e1cec82523f0d80244059a3f5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:37:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 15 Jun 2026 23:37:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 15 Jun 2026 23:37:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 15 Jun 2026 23:37:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 15 Jun 2026 23:37:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:37:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:37:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 15 Jun 2026 23:37:36 GMT
ENV RABBITMQ_VERSION=4.3.2
# Mon, 15 Jun 2026 23:37:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 15 Jun 2026 23:37:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 15 Jun 2026 23:37:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:37:41 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 15 Jun 2026 23:37:42 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 15 Jun 2026 23:37:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 15 Jun 2026 23:37:42 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:37:42 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 15 Jun 2026 23:37:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:37:42 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Mon, 15 Jun 2026 23:37:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 15 Jun 2026 23:37:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:37:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:37:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 15 Jun 2026 23:37:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4299c123606593b0639ddff0175d3cfb361e406690c35914c420288953b61047`  
		Last Modified: Mon, 15 Jun 2026 23:37:59 GMT  
		Size: 42.6 MB (42623376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d8a5b44e3bddf27bad02a57777b0844ddcb24bb8eb69deba07a12a56e7e811`  
		Last Modified: Mon, 15 Jun 2026 23:37:57 GMT  
		Size: 9.2 MB (9206064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6553d9e71295ee63bcfefee959b4838fbedfa4c4b355296d919685ad1b5cbe`  
		Last Modified: Mon, 15 Jun 2026 23:37:57 GMT  
		Size: 2.5 MB (2465151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7cf49232bb101cace23e1452e937568ffd81cceff1ea8dd87eeb7cdf4f945a`  
		Last Modified: Mon, 15 Jun 2026 23:37:58 GMT  
		Size: 26.0 MB (26004075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045098cb73fdca82f807c289d0c41ccf25eff056a5c53c5fe3177483ce799957`  
		Last Modified: Mon, 15 Jun 2026 23:37:58 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07450890ae3a8516e33e15bd68967abaf5bf5f0c6c5a58442324e5a3e089a65`  
		Last Modified: Mon, 15 Jun 2026 23:37:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962d96fb52c33a128f8d26aedceb42796c66071423edc14e1182a67fbd19c7f9`  
		Last Modified: Mon, 15 Jun 2026 23:37:59 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdd19e4e855ddc51d81075a5e82c55910bb67cd74d2459938c1749e2d6744d9`  
		Last Modified: Mon, 15 Jun 2026 23:37:59 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8fa901d71e12d0015c31d2aec5177722fce14a407d953db60199dbb9ebd76458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6963430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d95dba535ab7c3f8ebf846ab466bbd73f87d39be4f07c221c2f52c941326d86`

```dockerfile
```

-	Layers:
	-	`sha256:5d4d670fafd7c6a793d234904db8ce1a75d3dad6d7c9c828961a3128f71e6c2d`  
		Last Modified: Mon, 15 Jun 2026 23:37:57 GMT  
		Size: 675.8 KB (675815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51787db3408e1ca2b6717820e190a309b1480b1a6458639e0bb4a4fdb491b1b`  
		Last Modified: Mon, 15 Jun 2026 23:37:57 GMT  
		Size: 3.2 MB (3190523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f281174f9754787bdbff34b32c623313f4d609d674465489c58647ae591c95`  
		Last Modified: Mon, 15 Jun 2026 23:37:57 GMT  
		Size: 3.0 MB (3036779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7abbc1a3b10da10e131e6c26540d4e0ed868e5c62f789ff43c9b3d45c4c6f`  
		Last Modified: Mon, 15 Jun 2026 23:37:56 GMT  
		Size: 60.3 KB (60313 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:6eed6c6e5a28e77cf41eae1b16f9b6e7f4bd7c3708b7e6cac2a206aca824c6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72362321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f494e19f286522a39b060945ec1dd67bc73b9bdc514a997b9a045e76a1895b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:19:44 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 15 Jun 2026 23:19:44 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 15 Jun 2026 23:19:44 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 15 Jun 2026 23:19:44 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 15 Jun 2026 23:19:44 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:19:44 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:19:47 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 15 Jun 2026 23:19:47 GMT
ENV RABBITMQ_VERSION=4.3.2
# Mon, 15 Jun 2026 23:19:47 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 15 Jun 2026 23:19:47 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 15 Jun 2026 23:19:47 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:19:56 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 15 Jun 2026 23:19:58 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 15 Jun 2026 23:19:58 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 15 Jun 2026 23:19:58 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:19:58 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 15 Jun 2026 23:19:58 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:19:58 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Mon, 15 Jun 2026 23:19:58 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 15 Jun 2026 23:19:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:19:58 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 15 Jun 2026 23:19:58 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e115f1597d5ecfae26d1e69826dca1a4590446cc0651fa46693557cc18a7dbdd`  
		Last Modified: Mon, 15 Jun 2026 23:20:06 GMT  
		Size: 33.5 MB (33518084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2944a570bfb8f817f97c043ade03667e74181d3b62db76835eb717daedc2d1`  
		Last Modified: Mon, 15 Jun 2026 23:20:05 GMT  
		Size: 7.9 MB (7862479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c318fdaf622f2806c20b197c86067dd9f197aed2e0482b837904841c6788f612`  
		Last Modified: Mon, 15 Jun 2026 23:20:05 GMT  
		Size: 1.4 MB (1404174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bdbb094f2ec345ba57c37bf0f0ce78510fe78e41b2b2fd0c5953b57debacfb`  
		Last Modified: Mon, 15 Jun 2026 23:20:06 GMT  
		Size: 26.0 MB (26003976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded5ea0aa0965e41eb5ca18e012ef5a384df45531c05d392f29967aa8f0d9381`  
		Last Modified: Mon, 15 Jun 2026 23:20:06 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c822071cf12cf4e843143e45f362739bd8a58bb3334fffb74fb1f568c0b12804`  
		Last Modified: Mon, 15 Jun 2026 23:20:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42fdaa5eff89822febf0a4b2f335cff6702a6c8a5150cd0b3d530614e21d37b`  
		Last Modified: Mon, 15 Jun 2026 23:20:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6074c0e5962c298352a1fd42f2f3eff688be1ee02876472b2a97bf7c5a3f0974`  
		Last Modified: Mon, 15 Jun 2026 23:20:08 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9dd16c1d3d010765f839a1cebd7c380cc362fe663c4992e1eb3a651656037591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 KB (60294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9516f02e17050b9d77fc887d3c100892743df1b08b03e79c19f4c516fb2494e`

```dockerfile
```

-	Layers:
	-	`sha256:fa22b53cf12e73e7f80600e913b92f19ca8b50bc53776e4562dd9a20c0ffcb71`  
		Last Modified: Mon, 15 Jun 2026 23:20:05 GMT  
		Size: 60.3 KB (60294 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:b6c0db488bb63bae467e54e34269f63b0ff34d6e9feccf3b59b7154a6c3b7957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71457262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416b5c568d932342be77c8db0fbd62e8e79115387891e2c6d7096aced51f0704`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:18:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 15 Jun 2026 23:18:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 15 Jun 2026 23:18:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 15 Jun 2026 23:18:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 15 Jun 2026 23:18:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:18:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:18:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 15 Jun 2026 23:18:53 GMT
ENV RABBITMQ_VERSION=4.3.2
# Mon, 15 Jun 2026 23:18:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 15 Jun 2026 23:18:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 15 Jun 2026 23:18:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:18:59 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 15 Jun 2026 23:19:00 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 15 Jun 2026 23:19:00 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 15 Jun 2026 23:19:00 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:19:00 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 15 Jun 2026 23:19:00 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:19:00 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Mon, 15 Jun 2026 23:19:00 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 15 Jun 2026 23:19:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:19:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:19:00 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 15 Jun 2026 23:19:00 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197ce17d013fe5f85f92d1619125aa60c9a717d4c816410713fb7fcf44a3b072`  
		Last Modified: Mon, 15 Jun 2026 23:19:16 GMT  
		Size: 33.4 MB (33430306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6848cba1b88e0b0ba5f85659fab4a24b2210e7dd953d2a0ed799e669144a4a01`  
		Last Modified: Mon, 15 Jun 2026 23:19:15 GMT  
		Size: 7.4 MB (7442923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dec7e3d6838e24f36b47e42f6ede2b35b265afad566ae39305dd43c5ea7f1d`  
		Last Modified: Mon, 15 Jun 2026 23:19:14 GMT  
		Size: 1.3 MB (1295485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f5e22cf06d095cea252d496727534ef2216e0a088b5fcc3435066355991c9c`  
		Last Modified: Mon, 15 Jun 2026 23:19:16 GMT  
		Size: 26.0 MB (26003679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cb29839f70b73f4f8851398a8335273f3a5515783361e249dc9a1754251cba`  
		Last Modified: Mon, 15 Jun 2026 23:19:16 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb84ad90d60a68ce5d0e0ad9c2f5ba53ef520ca34228fdfd3750d2412ce0bdc`  
		Last Modified: Mon, 15 Jun 2026 23:19:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6140f0963c76f279a22cd20dd4dc729a77ff4518b48e14f2374c423793e9e87`  
		Last Modified: Mon, 15 Jun 2026 23:19:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972bd8d1b0658ee72fc41a8ef8e8b8bd443e5702676854c0d97da077c03a4bcc`  
		Last Modified: Mon, 15 Jun 2026 23:19:17 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:60a411d2a4d32f287e0eaa13b3a0966b3ea1e8d777f964f3eaf13c060530d726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c85942f54b533e1e9c852b7b7a57a0bb6ad292102c0c4d310140a6fa6260cd9`

```dockerfile
```

-	Layers:
	-	`sha256:f871c53bd7914ec523a2d4a2a4e535f668e27ee00ff2944226aa3d3c8676202b`  
		Last Modified: Mon, 15 Jun 2026 23:19:15 GMT  
		Size: 671.0 KB (670958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d67d8a189b4cc56bb438a87c0bcf6a1e37dc8708e088cd61a880ddd6f2a6c68`  
		Last Modified: Mon, 15 Jun 2026 23:19:15 GMT  
		Size: 3.1 MB (3057015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c635aafd75747efb217b74b43f63b4c4ddda24ca4f64029e93c7c818f7bcfb9`  
		Last Modified: Mon, 15 Jun 2026 23:19:15 GMT  
		Size: 2.9 MB (2901941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d192175cab618ed3d04c61768c9c499c1029cfde947c8a9e076bcdbbaeca0277`  
		Last Modified: Mon, 15 Jun 2026 23:19:14 GMT  
		Size: 60.5 KB (60510 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:14e717267bd0df9f3f3beba7831084bddb5d0a963bb1f0f01b13d254397b2ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83195702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99a34a6fee13830792e9011e1ac94a82cbae8f4c10d3f3c96ff120e08bacf4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:30:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 15 Jun 2026 23:30:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 15 Jun 2026 23:30:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 15 Jun 2026 23:30:45 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 15 Jun 2026 23:30:45 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:30:45 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:30:47 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 15 Jun 2026 23:30:47 GMT
ENV RABBITMQ_VERSION=4.3.2
# Mon, 15 Jun 2026 23:30:47 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 15 Jun 2026 23:30:47 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 15 Jun 2026 23:30:47 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:30:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 15 Jun 2026 23:30:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 15 Jun 2026 23:30:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 15 Jun 2026 23:30:54 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:30:54 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 15 Jun 2026 23:30:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:30:54 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Mon, 15 Jun 2026 23:30:55 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 15 Jun 2026 23:30:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:30:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:30:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 15 Jun 2026 23:30:55 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96feb052d2b08b43dbd7357ad9a80b8dfed3cd48d724c68db72db2c28191560e`  
		Last Modified: Mon, 15 Jun 2026 23:31:12 GMT  
		Size: 40.5 MB (40483621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1707a7742a2a5f9a5b8063687103dbd9778ead1c7b62eff5376104ac01a2e55`  
		Last Modified: Mon, 15 Jun 2026 23:31:11 GMT  
		Size: 10.0 MB (9992283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42deb0f52aa7c72a5355503657caa1e2e06d39dc27e68b4ac564af78e1e6a066`  
		Last Modified: Mon, 15 Jun 2026 23:31:10 GMT  
		Size: 2.5 MB (2514036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d44d0202b65edbaa4367a247b80b16e2ef477d2406862ab275038bcde0f5fd`  
		Last Modified: Mon, 15 Jun 2026 23:31:12 GMT  
		Size: 26.0 MB (26004142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a32f96bec6fdbb79edb1911dd61241356d9e03bfd4b277df061ccf28e835bb0`  
		Last Modified: Mon, 15 Jun 2026 23:31:12 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127ac58de81428930cdf284246ce60d1ef7e4c780ea085909a1d8ab25d8e8b39`  
		Last Modified: Mon, 15 Jun 2026 23:31:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3760ec29ae1bb67bfaf66686ca692a4db8a489d33ae98d08e9a28fd764a9681`  
		Last Modified: Mon, 15 Jun 2026 23:31:13 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9312c9b96631b488ff357ce27c0e61aff9b98babb31d8fecebdf55191dce9c61`  
		Last Modified: Mon, 15 Jun 2026 23:31:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a47cde1f363991179634b6bc00c2da33d9543b895bb03d056c0731b9dcd3312f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027ed1f9db0a916ab07988055a4516948b4020fdb02f5ad0892e3a1bcce01c14`

```dockerfile
```

-	Layers:
	-	`sha256:e8856566b355a05f302f83732e3c1704e70926c948b70f4b81859f17d759820d`  
		Last Modified: Mon, 15 Jun 2026 23:31:11 GMT  
		Size: 676.0 KB (675958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7bdac4f9e811bb5f8063bac9bb4fd53c912020aa49a18d1e2cb2ae521c30be`  
		Last Modified: Mon, 15 Jun 2026 23:31:10 GMT  
		Size: 3.2 MB (3227483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6facd3fb14fecf829e9e817ea66b1aeadffda353c970b1a4126188a4896ed3`  
		Last Modified: Mon, 15 Jun 2026 23:31:11 GMT  
		Size: 3.1 MB (3072415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f7476a611bae9d8d124e7e1bd6e4888ec9b30ae8ddef88f04830c0db4bd35f`  
		Last Modified: Mon, 15 Jun 2026 23:31:10 GMT  
		Size: 60.6 KB (60552 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:039a3ca06949c08b0c07ef0f1955a0e3137ed99624e74e0aa3828e12bc437036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73783717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24179fdb78b28d0580bba6dc5089185ba15a234ed4680071b340f6f9e359e57a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2026 23:19:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 15 Jun 2026 23:19:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 15 Jun 2026 23:19:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 15 Jun 2026 23:19:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 15 Jun 2026 23:19:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:19:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:19:35 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 15 Jun 2026 23:19:35 GMT
ENV RABBITMQ_VERSION=4.3.2
# Mon, 15 Jun 2026 23:19:35 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 15 Jun 2026 23:19:35 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 15 Jun 2026 23:19:35 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:19:41 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 15 Jun 2026 23:19:42 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 15 Jun 2026 23:19:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 15 Jun 2026 23:19:42 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:19:42 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 15 Jun 2026 23:19:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:19:42 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Mon, 15 Jun 2026 23:19:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 15 Jun 2026 23:19:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:19:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 15 Jun 2026 23:19:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794d9a0e8a86a73cbe17c3a099fd77d83aa4e626a2705d38f5e249eedca5f169`  
		Last Modified: Mon, 15 Jun 2026 23:19:57 GMT  
		Size: 33.5 MB (33483207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40510ea9cb6f326b48d8c39f1fcce5c24c5d165baef32fec5b9300f79ea4209a`  
		Last Modified: Mon, 15 Jun 2026 23:19:57 GMT  
		Size: 9.2 MB (9196012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1993b39d32481f7fda29622d2311572562325559a8d23c155c5495fc07e82e71`  
		Last Modified: Mon, 15 Jun 2026 23:19:56 GMT  
		Size: 1.4 MB (1408639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db60a39c36d017852e3abb9b09544a9e1caa28e56f74b2641ba6783112005418`  
		Last Modified: Mon, 15 Jun 2026 23:19:57 GMT  
		Size: 26.0 MB (26003663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef423abc35d9478bc549dec1f1ce3a6eefed323faa63e984f76f67d8440244a`  
		Last Modified: Mon, 15 Jun 2026 23:19:57 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80374eac21be565c329fa3638ac5e5e2e431a11b3eea1c8fdcf78ec77684bff6`  
		Last Modified: Mon, 15 Jun 2026 23:19:58 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b05024ce278cb671ede0cbe91ddff3b005f3511bbf5f17b27d70d902a871ce4`  
		Last Modified: Mon, 15 Jun 2026 23:19:59 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d439fb17f156b0f2b180849564895767d2e2a89247cf3ad89444da3469848e13`  
		Last Modified: Mon, 15 Jun 2026 23:19:59 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d551abce6e92b21e17854cd2d769820c62d1806000a0dd063d9999ba2641607f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cb4a58bb6bc4ab542be7be00091c24b13c478c4fa53786afd26c81a8f3ceb8`

```dockerfile
```

-	Layers:
	-	`sha256:b668870644047d10db1bac3cac432b79df5d73a1f8dbe28222f6d2a8ec7a169a`  
		Last Modified: Mon, 15 Jun 2026 23:19:56 GMT  
		Size: 670.8 KB (670810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783a97725971d09a6795a58b4f5e0e475ffbf11cff5b580b02d0c04cc2372c15`  
		Last Modified: Mon, 15 Jun 2026 23:19:56 GMT  
		Size: 3.2 MB (3168776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e385c6a3be0fc322ba272972da6ce367251b379de8c099291174aea94d638c87`  
		Last Modified: Mon, 15 Jun 2026 23:19:56 GMT  
		Size: 3.0 MB (3015036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7dbb01571fa4172785f27d61043a23674e38c3914a7ffba983fe0ba8df484f`  
		Last Modified: Mon, 15 Jun 2026 23:19:56 GMT  
		Size: 60.3 KB (60263 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:2e4af1a18f2806e493d7a85f6d764d4911e4f0a50f41c45a6f900f4465f0070a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75437120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff1b5fc761ef4fdb68dc51eb2d62f5b9fc808679824ab3c829d2239dddb135a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:36:31 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jun 2026 20:36:31 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jun 2026 20:36:31 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jun 2026 20:36:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jun 2026 20:36:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:36:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:36:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jun 2026 20:36:36 GMT
ENV RABBITMQ_VERSION=4.3.2
# Wed, 10 Jun 2026 20:36:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jun 2026 20:36:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jun 2026 20:36:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:43:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 15 Jun 2026 23:43:16 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 15 Jun 2026 23:43:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 15 Jun 2026 23:43:16 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:43:16 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 15 Jun 2026 23:43:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:43:16 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Mon, 15 Jun 2026 23:43:18 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 15 Jun 2026 23:43:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:43:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:43:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 15 Jun 2026 23:43:19 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa22709dd4be137b4bda4ecdaedd05a24418c560140baaa183a4a76219488f2`  
		Last Modified: Wed, 10 Jun 2026 20:37:22 GMT  
		Size: 34.1 MB (34091524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79befadaa45c78a7913de7300aa6a9bce59638f88d314c0bfe135b474212e83`  
		Last Modified: Wed, 10 Jun 2026 20:37:21 GMT  
		Size: 10.0 MB (9966909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c76dbe7ea1428c0045a108842102e5c8b379c8bf956d0cf3ec76dc747311f3`  
		Last Modified: Wed, 10 Jun 2026 20:37:20 GMT  
		Size: 1.5 MB (1542240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f132b0116dc439f7c5674584d35708b0619305bf739cea84fb912c22e02139`  
		Last Modified: Mon, 15 Jun 2026 23:48:25 GMT  
		Size: 26.0 MB (26003765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b005f1a9fc9db2ad83de029143e3bacc9a42eb2a87143b69c18e46dc61b683f`  
		Last Modified: Mon, 15 Jun 2026 23:48:24 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa864cfd5a3dc5f9bc7e011a8accaa286e7e2f15932d0e5e5f2aa1801844808`  
		Last Modified: Mon, 15 Jun 2026 23:48:24 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef757a5adbd8d9f753f7d1273f949ec80bcd4a2b76d6a7a99a38e4da4ab09854`  
		Last Modified: Mon, 15 Jun 2026 23:48:24 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47e88e2dfc80e622780796cc3b7de814fef12d74ba7e327b5e066d444b087a`  
		Last Modified: Mon, 15 Jun 2026 23:48:26 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:04d27dd4071a4bbead473e693d6a9cff6069b5f3a12dcd27677bd824bea95bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6938086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3402c62c753209123969437a57795e530659931acfd4e7c364f1032acd82d259`

```dockerfile
```

-	Layers:
	-	`sha256:62890cd22fe2fe636587bbef0a5c113120412f62d77402a8fee7dd13db88429a`  
		Last Modified: Mon, 15 Jun 2026 23:48:24 GMT  
		Size: 671.0 KB (670955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d2153520c4ec64b0b91766ef3c895627eb5add94049448eb1a3216c13bc3da`  
		Last Modified: Mon, 15 Jun 2026 23:48:25 GMT  
		Size: 3.2 MB (3180918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f123d5ea7cee219f29dfa69cd0c7122bd40ad522c74b8df27ba7996a34d2ab2`  
		Last Modified: Mon, 15 Jun 2026 23:48:25 GMT  
		Size: 3.0 MB (3025838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c866afd13ce7988364a1531a9cc36aa758dfdcfb3e3a31c1e04028e9247f5c1`  
		Last Modified: Mon, 15 Jun 2026 23:48:24 GMT  
		Size: 60.4 KB (60375 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:ec4064397083029bd5605701d635ba6b4ae8eda1aa26184170ddd3264b7c420b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79355413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2f0b0858aa1e5688c2a194fdc23c17d83939164d79da31a841f467ebe9d98f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 21:17:13 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 11 Jun 2026 21:17:13 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 11 Jun 2026 21:17:13 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 11 Jun 2026 21:17:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 11 Jun 2026 21:17:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 21:17:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 11 Jun 2026 21:17:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 11 Jun 2026 21:17:25 GMT
ENV RABBITMQ_VERSION=4.3.2
# Thu, 11 Jun 2026 21:17:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 11 Jun 2026 21:17:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 11 Jun 2026 21:17:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 03:27:04 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 17 Jun 2026 03:27:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 17 Jun 2026 03:27:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 17 Jun 2026 03:27:15 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 17 Jun 2026 03:27:15 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 17 Jun 2026 03:27:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 17 Jun 2026 03:27:15 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 17 Jun 2026 03:27:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 17 Jun 2026 03:27:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 03:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2026 03:27:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 17 Jun 2026 03:27:15 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e876acd4e29f557e99a2e338e5e1518f4245c8925b70ceea18945751e9deb11e`  
		Last Modified: Thu, 11 Jun 2026 21:22:12 GMT  
		Size: 37.5 MB (37516254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb79c4557377acdcbbb7372d718d8c950c3cf358f58cce4818378a8dcdfcbed`  
		Last Modified: Thu, 11 Jun 2026 21:22:05 GMT  
		Size: 10.8 MB (10796132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801bcc2f820961ee7f92b114278ce4cb15dc3cfa6ebc606c44772fc04b2e1826`  
		Last Modified: Thu, 11 Jun 2026 21:22:01 GMT  
		Size: 1.4 MB (1449596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad50b0fcae7e750f2546ce66fb1bb471eddb7616217d60e8e4f6c0de5a55844`  
		Last Modified: Thu, 18 Jun 2026 17:10:21 GMT  
		Size: 26.0 MB (26004016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787beb8900425b740834ed2a9e434433699fc879311f18d68e999a2e5563a596`  
		Last Modified: Thu, 18 Jun 2026 17:10:16 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627ef4a34542146e25d11fb3b25c6d673ecb0e28d89c0cb01e4ad54db7deea9b`  
		Last Modified: Thu, 18 Jun 2026 17:10:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78d768b180b37b54f829f63db1b18142548e0ce3a23a66d52205fa0da622e9f`  
		Last Modified: Thu, 18 Jun 2026 17:10:16 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12ad00d1a33bcd50c1c7874ad9dfe3bbea7b02e018f0ea8fe4d31b9bf7f4661`  
		Last Modified: Thu, 18 Jun 2026 17:10:18 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:38a377bc98fc59a6e6e843448340a8f75645a4c50685eb8c226c1656a57c7487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7017304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5284e3fade56b43dc995432ddf62339c451052c4fa40ce1fb927e1494e73a1f`

```dockerfile
```

-	Layers:
	-	`sha256:337b234c1c4897ffda10cbb5e2ec6f4a0c1468cafd02063fa0302fdf752cbd0c`  
		Last Modified: Thu, 18 Jun 2026 17:10:17 GMT  
		Size: 673.9 KB (673924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22043ceb455a1eeee043981caa3f7c45b42f3e776cff50e2f635ebf80698dd15`  
		Last Modified: Thu, 18 Jun 2026 17:10:17 GMT  
		Size: 3.2 MB (3219033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7a533ed8f8ba3a39f88c2d504d4b796e402a4104da353460859cf2cbd3af34`  
		Last Modified: Thu, 18 Jun 2026 17:10:17 GMT  
		Size: 3.1 MB (3063965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149366013a2ac08057363fd384e21b0abf1e7ef5e3f120e6546ee3e983a38662`  
		Last Modified: Thu, 18 Jun 2026 17:10:16 GMT  
		Size: 60.4 KB (60382 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:d9d8087c49bb3e289bec7c8f95d1ed451200ddc2a823d5ca02af31af38f8faa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73544607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ff544a9ec9ad32e68f2537e0d800532468df1f7a64c130b34a1f16f51607d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:43:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 10 Jun 2026 20:43:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 10 Jun 2026 20:43:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 10 Jun 2026 20:43:46 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 10 Jun 2026 20:43:46 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:43:46 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 10 Jun 2026 20:43:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 10 Jun 2026 20:43:51 GMT
ENV RABBITMQ_VERSION=4.3.2
# Wed, 10 Jun 2026 20:43:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 10 Jun 2026 20:43:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 10 Jun 2026 20:43:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:26:57 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 15 Jun 2026 23:26:58 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 15 Jun 2026 23:26:58 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 15 Jun 2026 23:26:58 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 15 Jun 2026 23:26:58 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 15 Jun 2026 23:26:58 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:26:58 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Mon, 15 Jun 2026 23:26:58 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 15 Jun 2026 23:26:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:26:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:26:58 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 15 Jun 2026 23:26:58 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209109586c257575d5477c8024bbe62c09ac50b5515af08c6c3c57981758c3e4`  
		Last Modified: Wed, 10 Jun 2026 20:44:31 GMT  
		Size: 33.9 MB (33946875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a842297c512fc4e6a1cfebe52a3b6084a1513836d5f2e9c35c9bb8b52fa7556f`  
		Last Modified: Wed, 10 Jun 2026 20:44:30 GMT  
		Size: 8.4 MB (8350140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ec7c9e2f1f4a432410b71995f73d6e6092556731912c691305a9117c80c358`  
		Last Modified: Wed, 10 Jun 2026 20:44:30 GMT  
		Size: 1.5 MB (1515532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9fb148c1e06c5f1778bb18de72b5361839d2e38085acfb0ce75fdf2824fb98`  
		Last Modified: Mon, 15 Jun 2026 23:34:10 GMT  
		Size: 26.0 MB (26003786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ea5a9bd25d21a3863b4eb24afac138e20e6103fa6cefb966040f0e87f857b7`  
		Last Modified: Mon, 15 Jun 2026 23:34:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca2307c88427f4c8efd34d4323647a592870aa1d0d31181e28e59d08437eb5`  
		Last Modified: Mon, 15 Jun 2026 23:34:10 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa673ae772946b970af2025edb84dd291f48ee7c2407a7af3f977b4a1b36bb86`  
		Last Modified: Mon, 15 Jun 2026 23:34:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f426185f5adbe25158e687330ab288343e835a6901a8abec36657f2379c6ab21`  
		Last Modified: Mon, 15 Jun 2026 23:34:11 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0eda11a70fded9c7f2209d548b17cc459e7db2205f5aaa59801ad51f1757dcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6714468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6f8414103c2b13c617c0c3047090aaf8b65ba7ca3e684c25ccadbc1b3497e6`

```dockerfile
```

-	Layers:
	-	`sha256:430ed97144bb8bd208b227ded5dcd4a4e84491d680e352e3b454a21716f6f646`  
		Last Modified: Mon, 15 Jun 2026 23:34:10 GMT  
		Size: 670.9 KB (670921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e08338253c3b4ae06f32f97454a8fce987b4ded21afbd78114fbb125fa828f`  
		Last Modified: Mon, 15 Jun 2026 23:34:10 GMT  
		Size: 3.1 MB (3069142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67adfbde745e72c06a59d306ad094e18abd92aa267e49480664fb8a7d852b9f4`  
		Last Modified: Mon, 15 Jun 2026 23:34:10 GMT  
		Size: 2.9 MB (2914092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:889761d8b995c73411fee12f7a14450510a9ac0dfec53d8301ad12f48dda82a0`  
		Last Modified: Mon, 15 Jun 2026 23:34:10 GMT  
		Size: 60.3 KB (60313 bytes)  
		MIME: application/vnd.in-toto+json
