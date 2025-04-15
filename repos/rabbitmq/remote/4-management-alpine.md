## `rabbitmq:4-management-alpine`

```console
$ docker pull rabbitmq@sha256:c1266e1991737c12a2e8cb89a51019948f7f1287a86b6c14af33c6e2b017b4b4
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

### `rabbitmq:4-management-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:842426090c43c2b351dc84da848ecc8659905b7888098c4eb57d159e70ba2a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89170642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad792055940806a1e6422efd3d0fbe668267e471e31e2808a584b90729b9510`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=4.0.9
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd61554b7deb09b7e61aa5ea8f23c6690dc072fa309d8806afcd2f4e1bd4d5f0`  
		Last Modified: Mon, 14 Apr 2025 23:07:02 GMT  
		Size: 42.8 MB (42833505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6ba7c6b43978499dd2adddf70e482d27704c2fed09feaf7ef4a35e513a2856`  
		Last Modified: Mon, 14 Apr 2025 23:07:02 GMT  
		Size: 8.3 MB (8311596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e9749cf4230bb57bfbd846cf8db3bf56a555da8fdc5f209cedb0dfc2e1c785`  
		Last Modified: Mon, 14 Apr 2025 23:07:02 GMT  
		Size: 2.3 MB (2279352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124147449ee78d659db8840b0e2e0b84eb72e332733759db5367a76d52877d3`  
		Last Modified: Mon, 14 Apr 2025 23:07:02 GMT  
		Size: 18.3 MB (18334812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc63f8a58bba6dab8f7db76b24df5b2062902beb4df54367638b9f56406b7137`  
		Last Modified: Mon, 14 Apr 2025 23:07:03 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4218106201da69727b385a7243d84234ecdf3cd002bc0366f9852af6b1ca0b64`  
		Last Modified: Mon, 14 Apr 2025 23:07:03 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5e9e2366ad9a6b6d071405552f9bb611263c83b31c7cc87867258768cf8a4a`  
		Last Modified: Mon, 14 Apr 2025 23:07:03 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69635d97eb2bdaab0bd4515aa3cb64294911472534890c37c1414b2d1c5d3bc`  
		Last Modified: Mon, 14 Apr 2025 23:07:04 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26609137b8bdd64075dac1f9070b24c28897e686824baee8ac74f719541e3660`  
		Last Modified: Tue, 15 Apr 2025 00:05:25 GMT  
		Size: 13.8 MB (13767381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f5fb2eaa9e4cebaf3e00b93b405a8dc4fd2ee3b4fb30518a8b04cd22081f2566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1641766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5fb3f36dd8128bd680d18a0903e1b48fd2ea5c83e548318cdb8292034d1573`

```dockerfile
```

-	Layers:
	-	`sha256:3801b475b5dfee75007858b90085779724c12ee1b012b8c08b1bd38a25f5e167`  
		Last Modified: Tue, 15 Apr 2025 00:05:25 GMT  
		Size: 1.6 MB (1630544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e621386b41fe7ed437e25d4318c0580d6493d1f566ec0d0b688488f8a3969f`  
		Last Modified: Tue, 15 Apr 2025 00:05:25 GMT  
		Size: 11.2 KB (11222 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:4fbb3f88b06f5d1087898a8e60dad42fae9ab1256ecef291a530ed415ae4522a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77858033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741d7fa72506dfdae51bbf1a24e35c4c5fdb17bfac0afc44b2d460aedbc307ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=4.0.9
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fc7de5297f460eb8edbb34d2fa88470349312b717c45c18d4cccc10ef15f94`  
		Last Modified: Fri, 04 Apr 2025 17:30:56 GMT  
		Size: 33.4 MB (33427362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41b00ee5464b93d67fdf77837de86033b382261212c42a17526a10a5bbf3f0e`  
		Last Modified: Fri, 04 Apr 2025 17:30:56 GMT  
		Size: 7.1 MB (7097958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6196f0e9a4a2e32bae325452b9da3e6ef9f612848be7ccf84ab3446472ba0a8`  
		Last Modified: Fri, 04 Apr 2025 17:30:55 GMT  
		Size: 1.2 MB (1226979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1af2a7286196b8337c1d064c2260656e76051ddcf63ebfc1c538741cde0c431`  
		Last Modified: Mon, 14 Apr 2025 23:01:00 GMT  
		Size: 18.3 MB (18334696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce853c07252cb1d8a029347426f6e01d9d52b93fe40e4f3a77eaf3bad9572d6e`  
		Last Modified: Mon, 14 Apr 2025 23:00:59 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ed07ce31ea8f4e6f071206d054da447929989886f10a3694e7dc5bb0ad57f`  
		Last Modified: Mon, 14 Apr 2025 23:00:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97246acde4e405a0212d59c50b3169d0b2dcb8c401ac7c8de47dcd5a24b0f449`  
		Last Modified: Mon, 14 Apr 2025 23:00:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68620eb3789cfc6f686acb2b098743d38a87554314c150993f14777b3ab00ebc`  
		Last Modified: Mon, 14 Apr 2025 23:01:00 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2302bbea6a6084a5bcafc6e4847f0927d5a555dc2ebd930693893121f453da`  
		Last Modified: Mon, 14 Apr 2025 23:07:51 GMT  
		Size: 14.4 MB (14404567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0113d2fae338c5c017418db4d9ff974912b614478b83b4f9f016e5508d3fb6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 KB (11084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f364d06539bf71c426ca413b0978ee2c4c27bcb2d70179314f1465c8c6dfea9b`

```dockerfile
```

-	Layers:
	-	`sha256:40ef63c0d952cca805d538c6952645963ea5da07a791c118872f5421823ee2d3`  
		Last Modified: Mon, 14 Apr 2025 23:07:48 GMT  
		Size: 11.1 KB (11084 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:8639e6b8993ca2686a083b42b94cf9db99624587cb53e8e0d46a80926b337a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76725253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447934290ca2af5a1475fa9c110fb68068e05b725c11615c9338e52114112cd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=4.0.9
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180687ec158ecb9d2287088070115c5d94d14aea357ed2cb35ec5a1fd15a1a84`  
		Last Modified: Fri, 04 Apr 2025 17:35:53 GMT  
		Size: 33.4 MB (33370046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8497ebbbc56f64557a9607867ff3739a5e4a1df46ed0cf9df1c0f271463ad5ae`  
		Last Modified: Fri, 04 Apr 2025 17:35:52 GMT  
		Size: 6.7 MB (6742225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91faa9fbaa189690893c27b0422c385dd52ef1dfd84283d57cd33790ff76a365`  
		Last Modified: Fri, 04 Apr 2025 17:35:52 GMT  
		Size: 1.1 MB (1134773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a2527fa0507fadb97655e9dab5b7673c0ebb3af658b24118961f91615d1052`  
		Last Modified: Mon, 14 Apr 2025 23:16:31 GMT  
		Size: 18.3 MB (18334506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc33b0cbe9b1e3a19b8cb05641f0287e199008351d7b0bb6bb978cc484f030b`  
		Last Modified: Mon, 14 Apr 2025 23:16:30 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7392c33f2c878ddddb5c2a9de285aba803fac154eecf5f390ce00311097e2c25`  
		Last Modified: Mon, 14 Apr 2025 23:16:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebfda414e09147cc977a82301a8d251ad5c18d8fe68ce7956d96b52b2fdbf85`  
		Last Modified: Mon, 14 Apr 2025 23:16:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbfb3af56c8c3de18680597e3b7c3f0346c2e8f17ab8747b2d72971e2d64081`  
		Last Modified: Mon, 14 Apr 2025 23:16:31 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdea0447e25713654256c232fd16e4b353311ca01cea4ccdacf483fc2b3cacb`  
		Last Modified: Tue, 15 Apr 2025 00:05:25 GMT  
		Size: 14.0 MB (14043836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:570ad2a8d313775280d8f4a8638f48e59b61a11f0a7ac6baa2359ab58a7dd23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1642872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da52ead0ab14ac0c28c477b8b781b07fa38614dd994d367d19d7769986417bc9`

```dockerfile
```

-	Layers:
	-	`sha256:55b5b2775e67626de46d43efb6e62dbb8bb3ba841bbd4aafaaf49a2f519555a9`  
		Last Modified: Tue, 15 Apr 2025 00:05:24 GMT  
		Size: 1.6 MB (1631573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adc38a758b35de8dad8ff15a37dfa4eae0b532b8e563203dc2368d3b67f98447`  
		Last Modified: Tue, 15 Apr 2025 00:05:24 GMT  
		Size: 11.3 KB (11299 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:c55ffef20fbf9439ce5cb57e63ad284a72fd44a77650a2fbe316ac1d3ae4388c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88242401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffeec66dcb09dfde4afc7957ea82a0bdab73564be4e7ea7d4e181e3c3e630eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=4.0.9
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c537f47f7bcc53c0caeabd81742dd023240f01e2016c548caf8f514027a3f9b`  
		Last Modified: Fri, 11 Apr 2025 23:44:24 GMT  
		Size: 40.8 MB (40828401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8d1d435fcd2d2c8403e1bf93b37f09e04a064bd1112b689c67ca308056ca74`  
		Last Modified: Fri, 11 Apr 2025 23:44:23 GMT  
		Size: 9.0 MB (9034861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f84000cc2bf3c11d836c512660669140dfb20cea51299a83861de750611e5`  
		Last Modified: Fri, 11 Apr 2025 23:44:23 GMT  
		Size: 2.3 MB (2323914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0160e3c7dbe52c830a611888bb1a32fcf7ff32cbaf2a760ae1f37bd7e9ef9cb5`  
		Last Modified: Mon, 14 Apr 2025 23:22:02 GMT  
		Size: 18.3 MB (18334838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd10b80a0dd02aa4289bc0ffec5fabd66b1ddbc3857e026a3cf966d24ea8b934`  
		Last Modified: Mon, 14 Apr 2025 23:22:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c60e8ad1773d011f8b63fcae5339b7748916a45ca239d9721223d3d10865ad`  
		Last Modified: Mon, 14 Apr 2025 23:22:01 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814b444e5abb38df73d7d7c322a3c9b6d27bbb714fd4c8291efc75ac1e8383e2`  
		Last Modified: Mon, 14 Apr 2025 23:22:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94c8f14c9c79d9791d9ad3904373aabbd46045bf0e88aca516f21e03c6218c8`  
		Last Modified: Mon, 14 Apr 2025 23:22:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaf8af2e6f25670cdde5839a18ffa2d04b45b05b46e347c4f8b40ff45279a3a`  
		Last Modified: Tue, 15 Apr 2025 00:07:58 GMT  
		Size: 13.7 MB (13725618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e491dec8147c8f5554651a414ad751d09f90bf05cab98a8f26933c80e2706983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1642747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c592fe7193c8a6c7ad05daf16bf03eb9be64bd9846e93ac1365eee653292eb`

```dockerfile
```

-	Layers:
	-	`sha256:e02e8087def9aaa4fcff4e5daa11e016a6aec0d282cc158639bf417cebcbf20f`  
		Last Modified: Tue, 15 Apr 2025 00:07:57 GMT  
		Size: 1.6 MB (1631421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04bb364e1b8609cd38e1748aa7e42f2b27f27fd9b06ccffeee8135de3378ebd3`  
		Last Modified: Tue, 15 Apr 2025 00:07:57 GMT  
		Size: 11.3 KB (11326 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:8b88523c496f5b46ea9a6bdb85befea51c016c2752dfaf3a5932f0b8f380c96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80143379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1362f8efe0e1a1bd72933ff6d993d87b76ef3383edce21e24ff7dca8511ab34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=4.0.9
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c28f23d3b9f60379173f2df0cd7a794da42549de5aa7c6c9f0a1f5e295ec18`  
		Last Modified: Mon, 14 Apr 2025 23:07:04 GMT  
		Size: 33.5 MB (33515645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4448ff457a717e28c108143c5a6800d12beb7e84aeb84485ced778c4bbe7f45`  
		Last Modified: Mon, 14 Apr 2025 23:07:03 GMT  
		Size: 8.3 MB (8324829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ee5a553d5cd050ff3247a30f23c5e51186e64088c321c8ae830ae4c408813e`  
		Last Modified: Mon, 14 Apr 2025 23:07:03 GMT  
		Size: 1.2 MB (1230622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b19e6d9b20b3bb92d6cd8f8e37dfa8d4e6546d1d79e6bb1832225e0cab047`  
		Last Modified: Mon, 14 Apr 2025 23:07:04 GMT  
		Size: 18.3 MB (18334496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa9c9a8ba191ac88a6b4597b83af3e598bf268e297026ce0f95c890edf527c`  
		Last Modified: Mon, 14 Apr 2025 23:07:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9e1b60c6d1cb96c6fbcb4c64e56dbce574a61aff05b66cd5d8e9cb5fd5c9e5`  
		Last Modified: Mon, 14 Apr 2025 23:07:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef791588225fa15f91787f67da419397496b9bf2825a65b29bc320a2d3b56a1`  
		Last Modified: Mon, 14 Apr 2025 23:07:05 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cefc24c3909ab398de4c9ec43bc593ce623567c78f9b16fc53748bd1149f27b`  
		Last Modified: Mon, 14 Apr 2025 23:07:05 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728acd33794a9a9daf8d4961ac24fd64081c408fa0cf8d981e39ed97c3506b0e`  
		Last Modified: Tue, 15 Apr 2025 00:05:31 GMT  
		Size: 15.3 MB (15272414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0e5f0ecb200baebeae2034b9a26e6f657fe09ec7062533b390858a5c7e8d43c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1641538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb1af49ee2ca1088ff15aa49a99983fd935441d3e9f04fbbeac5aafa4d08d46`

```dockerfile
```

-	Layers:
	-	`sha256:6874b95071d8735fe30b0651cd56daad1581c8435b497d8de8a8fc8a322b4329`  
		Last Modified: Tue, 15 Apr 2025 00:05:30 GMT  
		Size: 1.6 MB (1630347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:049bd2eb82109a5671f4ca398d7819e71d1590c622699904bded3d21aa7c9612`  
		Last Modified: Tue, 15 Apr 2025 00:05:30 GMT  
		Size: 11.2 KB (11191 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:c06bdca79449a4408568e04fc2b4300c4f57dfe2d2d770721108258a8c51b05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81280501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf67f3aea482242d5df54813668458db20eba1feead335a4f3e33d2b6c876a59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=4.0.9
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba56643b135045f7aee8b7a22b6cd6fb39a4c8acd1ae6f4406c25f70c5f1e37b`  
		Last Modified: Fri, 11 Apr 2025 23:45:24 GMT  
		Size: 33.9 MB (33899840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b74af34c0b18b147f270503c139ea0dd5f8acacfdfafa57c8920e756e9311`  
		Last Modified: Fri, 11 Apr 2025 23:45:23 GMT  
		Size: 8.8 MB (8848295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4077528002c281b6c0be1f39ee7c02d85fd31a5d2bcb1a11b1546b895e007237`  
		Last Modified: Fri, 11 Apr 2025 23:45:23 GMT  
		Size: 1.3 MB (1346534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769a8e361c6b3c2fbb18ee1fe19115ef8abfbc8e42bdc68d3c3e3d6d30245fee`  
		Last Modified: Mon, 14 Apr 2025 23:20:54 GMT  
		Size: 18.3 MB (18334488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b09e872d1774e1d78c38d110db89b3f933f9048809a1528c095baf9a48219c`  
		Last Modified: Mon, 14 Apr 2025 23:20:53 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14b07fbbc19fc7cb3acdebb5d2503bc0f3ab5ae2f46c5b222149d6af1aca912`  
		Last Modified: Mon, 14 Apr 2025 23:20:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec1b2373716fcf553f4324d9d52e1de789d0b1f6c8fdd048209a41bff899753`  
		Last Modified: Mon, 14 Apr 2025 23:20:53 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770a4bb63c13ca46bcd5c2b5f4e1bd7b3be7accf11f141caae50c09cf5c4ae66`  
		Last Modified: Mon, 14 Apr 2025 23:20:54 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a18e68021079e2a4241f6af15d2b1a0edbb2a9c14e42720664cf4aebd5d99c`  
		Last Modified: Tue, 15 Apr 2025 00:06:41 GMT  
		Size: 15.3 MB (15275242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e3fc5ae46d3fc09d93448c713a4fae06c9f53601838787efb4aafeb2a638d15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1641058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac3739c27e0d154b4fbcf847075bfa435f119e136dbfeb0f6bc3d94a77147c1`

```dockerfile
```

-	Layers:
	-	`sha256:ed62c6ce23eb1bb8fbb11f0b9fcd60c2faedcef8e8de5a5270a80229719d347c`  
		Last Modified: Tue, 15 Apr 2025 00:06:40 GMT  
		Size: 1.6 MB (1629792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a189322ca76a14f249a4d5b2a31f2a3e41f9f723c32b1a4e8ba4b98ebeb282bc`  
		Last Modified: Tue, 15 Apr 2025 00:06:40 GMT  
		Size: 11.3 KB (11266 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:8f315d757ca11e10fc973e68a65c610c28599689a18494e1322bcea31cb86207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82509012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80ce386664557f6f6d73e3f500aed23e16837d2a24b495872406c1c0deecf4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=4.0.8
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8886d26542841afc2fd7344a23ab629abee86f99bf07c7ee3f47d014de361885`  
		Last Modified: Fri, 04 Apr 2025 20:00:13 GMT  
		Size: 34.9 MB (34875773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df45b7bcc69afd85ac4e88ea60a44663dce9bbfbf75ec31959b089c20e93cda1`  
		Last Modified: Fri, 04 Apr 2025 20:00:10 GMT  
		Size: 9.9 MB (9858933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3097f20b70883b87845ed897d900aec16949918e53ec654caaf91b8be2df99f1`  
		Last Modified: Fri, 04 Apr 2025 20:00:08 GMT  
		Size: 1.3 MB (1266419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359234632a4bec4c6246e8f9e02429494e90adf2eca184b05c9d4bbc27b06e76`  
		Last Modified: Fri, 04 Apr 2025 20:17:34 GMT  
		Size: 18.3 MB (18334782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f1d2f0597f8b823a2f51fe6453fa3544d906939d8debc075a44ad9e943ab09`  
		Last Modified: Fri, 04 Apr 2025 20:17:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934d0aa37ee13a6e53da76376ab781479c0901e7a1ea028646c548b0a00efbf1`  
		Last Modified: Fri, 04 Apr 2025 20:17:31 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea7ce21102ddd861491a57aabaaef4f0dfbae16aab1aa751380c40d4a2f06c9`  
		Last Modified: Fri, 04 Apr 2025 20:17:32 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265b8c06c4a7e86cbe0d04e87f0f2c2fc808357457c2246986e4faae8ff82874`  
		Last Modified: Fri, 04 Apr 2025 20:17:33 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684034c16d7cc4c095178b6dfc432299c63d91add700028dead4f7f46d7a5cad`  
		Last Modified: Fri, 04 Apr 2025 21:28:06 GMT  
		Size: 14.8 MB (14819917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:180a7869287f96fe86ab0601e0f65c835cc666cb885e32af937a995d1b95caec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1642481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7480783099452d1fff182da413c37ca411af966d6c4ed724fedf7ba9ee3368f8`

```dockerfile
```

-	Layers:
	-	`sha256:165367846b6060f863d7fb489b5eafaa0db3661428f4ecec0cf7fb91480ff6ea`  
		Last Modified: Fri, 04 Apr 2025 21:28:04 GMT  
		Size: 1.6 MB (1631214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910388aa5808ec5e0dfc6864140c19d3078d6e05e3c8db59a074a6b8c716f430`  
		Last Modified: Fri, 04 Apr 2025 21:28:03 GMT  
		Size: 11.3 KB (11267 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:ae096f0d952333948e8975726bdf8fa76a7a52f60d41c622e03a434f5536aa63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79886178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe0a87b48c8f55988586c15d62f9b22d349fa0b5f960c51d7e331b61498df3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=4.0.9
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3e7f6067fc1a3d3d2bda8f4122c972e45c09b2e028e96a56d5ddbb715b848d`  
		Last Modified: Fri, 11 Apr 2025 23:46:19 GMT  
		Size: 33.9 MB (33943904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeff32fa4eaf3d0d5fcaad2d7f19d69e3e91be5bbf478a3eef2da0065b505ac4`  
		Last Modified: Fri, 11 Apr 2025 23:46:18 GMT  
		Size: 7.5 MB (7510932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c1829a44d8e1bc5107a40881692f85084556cdd949623fed76314f050f543a`  
		Last Modified: Fri, 11 Apr 2025 23:46:18 GMT  
		Size: 1.3 MB (1324690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2574ef8667c8f9615e4f103f6543bcc82dc2c7c097717c2309657cf643fa575`  
		Last Modified: Mon, 14 Apr 2025 23:54:15 GMT  
		Size: 18.3 MB (18334510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa9ef5c0f06c9e6ed985116c06eb39b1dc6fa9a982b30784ab7c23c1079e896`  
		Last Modified: Mon, 14 Apr 2025 23:54:14 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abbdfb1d336086bfcefa62d9b68bc9699eef516f5245c9888aada0aad21f1ef`  
		Last Modified: Mon, 14 Apr 2025 23:54:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93ecef7a00fa6887b9b772e975ba2b2819b673271a9fc4911c6da1aa051b64e`  
		Last Modified: Mon, 14 Apr 2025 23:54:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65734bea3eae285038f88abe504ee787afea8e82b7d1540e8b7e540e6552045a`  
		Last Modified: Mon, 14 Apr 2025 23:54:15 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83336b04824e4d8e6c625267976223c0dd1e88ee4484b41fa8848d8d6bf0af6a`  
		Last Modified: Tue, 15 Apr 2025 00:06:16 GMT  
		Size: 15.3 MB (15302831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:20b9114f494271111762577928f3d90cd3ebbf48ff0eeb7cd06c2edd117601a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1640465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d10088fec27addad509fd817952dfe993d731182205c7d56a578d910377a9e`

```dockerfile
```

-	Layers:
	-	`sha256:e1af180796da054b4ab66193b60f1ce4fa33826a68cefe92dbb7fedc85489870`  
		Last Modified: Tue, 15 Apr 2025 00:06:15 GMT  
		Size: 1.6 MB (1629242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a37bca45e4b009b38ad945b4032c2a009c051b0434c56a84a1bffe2d6825d9`  
		Last Modified: Tue, 15 Apr 2025 00:06:15 GMT  
		Size: 11.2 KB (11223 bytes)  
		MIME: application/vnd.in-toto+json
