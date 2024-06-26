## `rabbitmq:3-management-alpine`

```console
$ docker pull rabbitmq@sha256:45b2e137b64baeff1f7f4230588be8f1a08b16939a4b64f5da57c59e5dcd3282
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
$ docker pull rabbitmq@sha256:c01be497320fe7f7dbd599f4cea0b47098e397f122899d016638972d52c7e245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88994884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d803c8cd1804bd5c2d92336db42a18363072de7c2b4d266ea3a629cd233a5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 22 Feb 2024 21:58:15 GMT
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
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85c7ed83b232c1163f2ba8382bf309487385f541e6f84cd0e452bf840377b82`  
		Last Modified: Tue, 25 Jun 2024 23:03:35 GMT  
		Size: 41.6 MB (41564331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb801f4df1dd51dc2a5a118cb0e8fab12f469ec600bae289597be3bc14ce7b0e`  
		Last Modified: Tue, 25 Jun 2024 23:03:35 GMT  
		Size: 7.6 MB (7578225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167df1e5ba071ccf671629387d2a8e5ac39ef7b5e84368a99bac608b349490ac`  
		Last Modified: Tue, 25 Jun 2024 23:03:35 GMT  
		Size: 2.4 MB (2405737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2860840a2fa760e148959301df12f5fb1497cfd9cffc49c14932b047252195`  
		Last Modified: Tue, 25 Jun 2024 23:03:35 GMT  
		Size: 18.7 MB (18719189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288f8a38ba9089a5dd386a5c4d222868ed48d1ab512b8f4a3ddf7dc76329b98a`  
		Last Modified: Tue, 25 Jun 2024 23:03:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3ed98fe0030585e8c2f7cbfb755e44d4f50d9151bff84ce161359fc0cd073f`  
		Last Modified: Tue, 25 Jun 2024 23:03:36 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b725bc0e713d09602d2fb808d521d4aa06aaf63d22a63c2ca3bc5c8b60390b`  
		Last Modified: Tue, 25 Jun 2024 23:03:36 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b07312ba4649561703a126735952fc49669eff86c3c24671f57f629a1aba40`  
		Last Modified: Tue, 25 Jun 2024 23:03:37 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936b04598aaa16925daa6bf9888241c55ca5416a5738dec393e332ac925cc5c1`  
		Last Modified: Tue, 25 Jun 2024 23:55:44 GMT  
		Size: 15.3 MB (15308320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:98c84cdfc1049951a0064ec502ba9e5eca9e79f92196e36af6bbdcababe92eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2053609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cdd4672e2603075afcbf567c157df8f334d0659a1a3b0bc44fa14bb613ebd6`

```dockerfile
```

-	Layers:
	-	`sha256:808159d0d0b4bb3f284fc599c2ce2ad23f5ac24d6f35e49cc189a47f00d30995`  
		Last Modified: Tue, 25 Jun 2024 23:55:44 GMT  
		Size: 2.0 MB (2042416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d1ed91ec5abb689314579657563f12bd5dc465a552264e8c9a8b430955ecb7f`  
		Last Modified: Tue, 25 Jun 2024 23:55:44 GMT  
		Size: 11.2 KB (11193 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:f586d0da3c6d1125991ccbace686d6a9c522fb6bcb65dd316783d886d63523c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78862955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636de6095e92e80a7ef866fc2534b41f301fd050c0a793d5212afb30b86b9455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 22 Feb 2024 21:58:15 GMT
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
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210802f2ea35a00183510885a92d8127ff9431d70f6b810b8deef9fdc734e14a`  
		Last Modified: Tue, 25 Jun 2024 23:03:57 GMT  
		Size: 33.2 MB (33182153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c45dea1889c1acd9e29d87f2a5da1e3210bd6f369e536f97e486fc2d1bbe1`  
		Last Modified: Tue, 25 Jun 2024 23:03:57 GMT  
		Size: 6.4 MB (6406023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347df8e91c7f27faa3e2dbb773f4c252a85173917ca90c9fe62fd116c9ca6935`  
		Last Modified: Tue, 25 Jun 2024 23:03:56 GMT  
		Size: 1.4 MB (1401711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f434cfc1b0c9832baf7cef6a26b37af66ff4e566c69122d296ba982d998c9eb5`  
		Last Modified: Tue, 25 Jun 2024 23:03:57 GMT  
		Size: 18.7 MB (18719238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb3e72810e1e534a565b4faccb0aa6bfb7c3da323899b06fe265e550feb4dc8`  
		Last Modified: Tue, 25 Jun 2024 23:03:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165c4ae0009f2508d9999bd36408e92c70736799c75b6da828c1497425252377`  
		Last Modified: Tue, 25 Jun 2024 23:03:58 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7a49c9ed86c226fd6a44413c29769a87294e0e7a46823efaa33d7a4b98ce13`  
		Last Modified: Tue, 25 Jun 2024 23:03:58 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad8aed6508efe24b1384f07b4d65e7eeee4c578bb2544b3b1146f0b2c4bf1e3`  
		Last Modified: Tue, 25 Jun 2024 23:03:59 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff412fda4b866458db6b7e82fdb8328e6f9630f52195c5d44d873d91683e3a2`  
		Last Modified: Tue, 25 Jun 2024 23:55:52 GMT  
		Size: 16.0 MB (15978163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8acf7320d49191e6e09aa24de1e9c05d98af6fd30c2b3f8eb40a084f3ec4ca1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 KB (11065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c819c93486fffc7183303c1472178cc17c8d2eb6717b0920688b7560fde0a958`

```dockerfile
```

-	Layers:
	-	`sha256:81df68d2189af76661284481d74f8389b0fb325646c2d6c70fc115fbabf7b664`  
		Last Modified: Tue, 25 Jun 2024 23:55:50 GMT  
		Size: 11.1 KB (11065 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:400ce60b1b5f81914e49477e71333ada7721a56c337ecfa845bf7be324123ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77759623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec47755b9eb9f44f6a6cfdd33bf1d5f04a7554b043c4887d27e13f0f0bdd5892`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Thu, 22 Feb 2024 21:58:15 GMT
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
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfd5582b720571a9b0fecf087be95698a31fbc0ad3c3a98c0d2fa9d8babcdf5`  
		Last Modified: Tue, 25 Jun 2024 23:08:43 GMT  
		Size: 33.1 MB (33082852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ea1a4b0ef2c2066a40f416025c307b0f24c1c3d8bf1fa7b8a98d478667541f`  
		Last Modified: Tue, 25 Jun 2024 23:08:42 GMT  
		Size: 6.1 MB (6106917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51c6db569f3778f35cd636e54bd12dda08925d9eb013d499c5bbd6fb99e5a44`  
		Last Modified: Tue, 25 Jun 2024 23:08:42 GMT  
		Size: 1.3 MB (1305653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5478ca4d458a80ade17b3801b46ded14824345ac5a690ec28b72de6c9dd27e`  
		Last Modified: Tue, 25 Jun 2024 23:08:43 GMT  
		Size: 18.7 MB (18719476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd539c5dad3218604f6fda30a7588f50b8563c8a5b14908e9063c3adc37f1b1`  
		Last Modified: Tue, 25 Jun 2024 23:08:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2995d6316b65b7d9057254bb1ceef9d638b0d47e0ac8399896c31231e8f07c0`  
		Last Modified: Tue, 25 Jun 2024 23:08:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf2afb64790c7893e536df1f20668149a2586ed5a106556f224f53dea764e80`  
		Last Modified: Tue, 25 Jun 2024 23:08:44 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a7578a7c49f9b49e81986eec00d590931d1f5e9a7e1a0eab3e7cd6ff3f3ad`  
		Last Modified: Tue, 25 Jun 2024 23:08:44 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c897a674bdb09268acd6ceae85dd4290d179491192fbcb90ff5740c6db34ac`  
		Last Modified: Tue, 25 Jun 2024 23:56:34 GMT  
		Size: 15.6 MB (15616472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1a77d17086643b9c93f61b693f57b0e4c550b30eef8df3bbc5afc3572e83f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6605f43f25b104478fe6d8e891638dbd6bd65e9531327cfabc3e5625185425d1`

```dockerfile
```

-	Layers:
	-	`sha256:50003f44bc0a0850e2d18bd5422415fa3fb26c34769bf2e518fe324ed2cf610e`  
		Last Modified: Tue, 25 Jun 2024 23:56:33 GMT  
		Size: 2.0 MB (2043339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7c16a9e985618d440e24e2cbb9682cc706b68752e9cb20069e275f12e69ca0`  
		Last Modified: Tue, 25 Jun 2024 23:56:32 GMT  
		Size: 11.3 KB (11284 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:3369545c94f746d5b4f397b2ea7cd3ba0b236c4bd345e812b5d6f8d21a997423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86935226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1655cfcb124bac69fd4063f2dfbfa246e837cdb433e4c38b2f79f91f12383dc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 22 Feb 2024 21:58:15 GMT
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86161a1758b23064987a95dea988ce9deea94bc419df67af61453a482950213`  
		Last Modified: Tue, 25 Jun 2024 23:48:46 GMT  
		Size: 39.7 MB (39684721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1258770cc387d1c97bf7340ce28985ffd573cc6f7f801fdca5733612388a272`  
		Last Modified: Tue, 25 Jun 2024 23:48:44 GMT  
		Size: 7.2 MB (7200827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b188a876c7e7d5f4835a13d6092e78201c7e2c2420ab4f5dfed5117ea78cae4b`  
		Last Modified: Tue, 25 Jun 2024 23:48:44 GMT  
		Size: 2.5 MB (2490022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51ee54c66756c915bcedbd417e7abfe407bc73131fbdc8374cd8ab92ca72652`  
		Last Modified: Tue, 25 Jun 2024 23:48:45 GMT  
		Size: 18.7 MB (18719243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a8082ddc702652c822ed4cccae8a202c4c44ab19ebf57843c65e60d9e0d7ce`  
		Last Modified: Tue, 25 Jun 2024 23:48:46 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b532717a5c2534553617f9f378d42b24bac018802a653a8393a29b7964f06477`  
		Last Modified: Tue, 25 Jun 2024 23:48:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbe73de5e4ef0becd8dfb72f633c8da60d2b4cd94a05833669f332b0428f352`  
		Last Modified: Tue, 25 Jun 2024 23:48:46 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14cadb34dd1d4b30ebcf4c8ce15f115d88b366b3d6b91f50fd4aa0792790218`  
		Last Modified: Tue, 25 Jun 2024 23:48:47 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22685bd6eef1dc08f2b7496db9eaf7d711963f1176b5e273ce612858dfae74f`  
		Last Modified: Wed, 26 Jun 2024 01:04:49 GMT  
		Size: 15.5 MB (15481456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8f1988e7d2bec13ce2ecf050c5c245dceddc1de7474a061213019e7ffad19a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfb9f800d5a0d3a080ddc89de1c50fe6709d150c9254d6075c5300926ba9b7c`

```dockerfile
```

-	Layers:
	-	`sha256:a81be3927e53391945919020c3073d66d7ccd16aaf6bcc41f227cc90b5947a18`  
		Last Modified: Wed, 26 Jun 2024 01:04:48 GMT  
		Size: 2.0 MB (2043189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837b2460d12830ac254032d7f8a384e6072d94848ad1d5a3c6a4bf644b31ce84`  
		Last Modified: Wed, 26 Jun 2024 01:04:48 GMT  
		Size: 11.6 KB (11593 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:bca080c1b4b1f290ea25cc5a0da656a6704f62f70d2e5140a3e27ecc681bfe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80979676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f6ecad684156077d47f87b35ec5787ca84d418e9e1abba4a6bb2eb8a52d64a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:fef5870f3bb90ed437c0331d7e65e52da6728b66d231aea95a605935fef056d7 in / 
# Thu, 22 Feb 2024 21:58:15 GMT
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
	-	`sha256:e9c6bf0d8f3154c26ee87ffe9feb02c91666069b8cbe0668cfae10922ad80c49`  
		Last Modified: Thu, 20 Jun 2024 17:39:06 GMT  
		Size: 3.3 MB (3250890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68093fdd390d3e8574e176e81bdd668ed93da413c3f952a41f1987bef1340364`  
		Last Modified: Tue, 25 Jun 2024 23:03:18 GMT  
		Size: 33.4 MB (33354792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25cf0af378487fe97b587c84250a773131429a5d50b119dfe5a0e2351d4bfa3`  
		Last Modified: Tue, 25 Jun 2024 23:03:17 GMT  
		Size: 7.5 MB (7504765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188039b29e1ce017750595388d8affbec3d1d97552786bae3cb3b8e959a61c9b`  
		Last Modified: Tue, 25 Jun 2024 23:03:17 GMT  
		Size: 1.4 MB (1404375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb2bf9fffd8416d95326182988f51363286cf6d6384e91cad79384041003183`  
		Last Modified: Tue, 25 Jun 2024 23:03:18 GMT  
		Size: 18.7 MB (18719443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e64000fee0830ad879de1e31b4044527d5ecff26d95c86b69e0b6061a1f32a`  
		Last Modified: Tue, 25 Jun 2024 23:03:18 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fecd8965543e2727644f2247cd00e8c6ddfc26e2d1a8c2cafb6e9a0c3d22123`  
		Last Modified: Tue, 25 Jun 2024 23:03:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1645b9a9aed09c160f4e0cb9e537014864b1fa5e2231f9bb8350f4a0248812`  
		Last Modified: Tue, 25 Jun 2024 23:03:19 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aa09ab52abc6242f23c760784d78768bae3590fdbed111594a8576212ef293`  
		Last Modified: Tue, 25 Jun 2024 23:03:19 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e223adc13b15841f3e6eeeb671c9479be015483d634de579b52ea8b982633a9`  
		Last Modified: Tue, 25 Jun 2024 23:55:44 GMT  
		Size: 16.7 MB (16743656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:698600eea6a626b69dc05e0eb3f9f3bc8ed75ed38a8fddf822164b866af046fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2053385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77569f750e44ac2c9d35e3e80476b910772fd2182a51d97a85dcdc7f62b42889`

```dockerfile
```

-	Layers:
	-	`sha256:03a25fad9e9f449a1a91d4315255aa5a9ae44466185971f1a042561a753a4ef8`  
		Last Modified: Tue, 25 Jun 2024 23:55:43 GMT  
		Size: 2.0 MB (2042221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ee58493f696e65d693b8d7f3d4efbd91349c29b52858de68c5e32bb24f0ecd`  
		Last Modified: Tue, 25 Jun 2024 23:55:43 GMT  
		Size: 11.2 KB (11164 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:b2258fadb440dc1677f6afd2704952e161b2cfca02fb961adf73a8444786e16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82004554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b511fe201de3c76eaeae722c9c54e86a852a963cad72ba75cbf50b9207923477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 22 Feb 2024 21:58:15 GMT
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
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9916ff05de722b6e7353ed6886f06f776a1564a1e02ecc14e244e8b97d73b9`  
		Last Modified: Wed, 26 Jun 2024 00:03:40 GMT  
		Size: 33.6 MB (33608736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11df5be3043bb8491e45ca9cdc4def4259a9833d8bf65633dd390ce728fc8fc`  
		Last Modified: Wed, 26 Jun 2024 00:03:40 GMT  
		Size: 8.0 MB (7992852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b82a7d83391675554902ac2ad1ac775af6315238e17ecff9ed4a5bb243d092`  
		Last Modified: Wed, 26 Jun 2024 00:03:39 GMT  
		Size: 1.5 MB (1515691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6973a07553a6c17a034fe61db42e2ece691dc07e4afed16213f919f9cf7d5660`  
		Last Modified: Wed, 26 Jun 2024 00:03:40 GMT  
		Size: 18.7 MB (18719569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ebaa1fcbfe66e1c64b2a7a05b0e3c54f5b6d6803e7203e452882e09bc9bcac`  
		Last Modified: Wed, 26 Jun 2024 00:03:40 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f93ab8cd0dd8045af4774c15e5b7039a5f0c79e0dbefd89fb9b9a80bb21285`  
		Last Modified: Wed, 26 Jun 2024 00:03:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c9a27163ef56283908f33f2def7f86c2e5b9f3ab4879a36d5ca44d2021348`  
		Last Modified: Wed, 26 Jun 2024 00:03:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ac46631b3e877f5a94cdb28ba17a68f66218723a27bb9a9efbb5ba6e536d`  
		Last Modified: Wed, 26 Jun 2024 00:03:42 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8be8a818e089ff58449386db7220828c61e8a79c68838aba52efca614275a2`  
		Last Modified: Wed, 26 Jun 2024 05:09:27 GMT  
		Size: 16.8 MB (16805318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:172b82fd5041ba87874d4e10dcbe1df9a2796233d7e233742cccafd046158dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2052805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1029a8674eb5e1cf8d9c3d2f1c88f2f6326117b65d4e4f2df38d724530496176`

```dockerfile
```

-	Layers:
	-	`sha256:a1641aee2a271fcaefdb61dac69652abe50484ea8f057f2143cf7296fa201b6d`  
		Last Modified: Wed, 26 Jun 2024 05:09:26 GMT  
		Size: 2.0 MB (2041553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892a3b2c926bd5213c3c0dec4f1858d8a67d10b1898658b06df8bfbbcc8fa426`  
		Last Modified: Wed, 26 Jun 2024 05:09:25 GMT  
		Size: 11.3 KB (11252 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:12922367f33352f2aa5ef94cdab352961eca449150726f29d1ea210843987cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80632663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3e20433bfe7def24d09e28565105ce426da296d66a1b33379bd405917196c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 22 Feb 2024 21:58:15 GMT
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
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb514cf9cc0400ae8f59fe2b584b752e933754ced33cbb35376883734256ed2`  
		Last Modified: Tue, 25 Jun 2024 23:41:59 GMT  
		Size: 33.7 MB (33686414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388c7766ea0499da7c3e9dbbd4300892650f6c1b9eaa0a3d36b487e0fe5d5e64`  
		Last Modified: Tue, 25 Jun 2024 23:41:58 GMT  
		Size: 6.7 MB (6721770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2305c5fef7855dc02807177ebb70af9ab8ba1b960e44f115234be9252fe4240`  
		Last Modified: Tue, 25 Jun 2024 23:41:58 GMT  
		Size: 1.5 MB (1496574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b97b3b76ffb09fc3a74baaa9eb6f3cf4dd811a9dbf651c45dce1bae8c0c85a3`  
		Last Modified: Tue, 25 Jun 2024 23:41:58 GMT  
		Size: 18.7 MB (18719471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e34340ffeb4765e4c3b8614e9e07f711aed5f98b3e8cde79df291ee98f250`  
		Last Modified: Tue, 25 Jun 2024 23:41:59 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b831429477c630a7cd77aec37fc76abe14a1c34e86bd57784479182ddf13260`  
		Last Modified: Tue, 25 Jun 2024 23:41:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffbf075cecb4c748d4fdd2655cad8370ad5e1ae0d818a7e2cd6fb676074d722`  
		Last Modified: Tue, 25 Jun 2024 23:41:59 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819e2e755a9f5489b3ef86bc083496e042d6edafe931bb7016ccb437d32fa696`  
		Last Modified: Tue, 25 Jun 2024 23:42:00 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9c5d2019ccb956d674418db5c602fe9ef141dd98c8e218062f147817c66457`  
		Last Modified: Wed, 26 Jun 2024 00:19:42 GMT  
		Size: 16.8 MB (16754193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:17874529ff4ff25ffef006a14dbe67195d9a6ff46893c1ad008cfd4f45fc735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2052217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ba744e5c258274af9b6848098e1d330c5071eacfeabfeef4a862530c59d2b1`

```dockerfile
```

-	Layers:
	-	`sha256:7f199f509d5d4a3174bf21a593c31909045e806a248011cc369406a8cc041e6d`  
		Last Modified: Wed, 26 Jun 2024 00:19:41 GMT  
		Size: 2.0 MB (2041009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd6f08ca9fe89fb2e7cce8cc43df892a8ce8f6f4ad0bcf240ed202aa2c02b4b`  
		Last Modified: Wed, 26 Jun 2024 00:19:41 GMT  
		Size: 11.2 KB (11208 bytes)  
		MIME: application/vnd.in-toto+json
