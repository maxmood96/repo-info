## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:7fd0a03ac9772b701248b3550fcef46ce486cd501133b1819d83772ec76c902f
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
$ docker pull rabbitmq@sha256:f1f43fa0d2b1a78eaea7eb8108401ba7dd1ba9b63b6840e5d4637e2950ea74ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75403261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be9f3b17300419149a9aa3302213f2609b1189a99102c1479a3a7765026e8fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 14 Apr 2025 17:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_VERSION=4.0.9
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 14 Apr 2025 17:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 14 Apr 2025 17:05:20 GMT
CMD ["rabbitmq-server"]
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

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:39489e1b1c741c4e859324f1a49b3b631331913efe78ada531b913ad41682579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6726524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931241ede8d334e586807199b4e5fdcc8aef79ea60b5c268dce45778d543da4b`

```dockerfile
```

-	Layers:
	-	`sha256:09940014ca0e369e00c5748ae7e60503c6e98b9ea2a78c6083dd11d394baf2b9`  
		Last Modified: Mon, 14 Apr 2025 23:07:02 GMT  
		Size: 657.2 KB (657214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e98c8dc73e2a21d96af364a4213aed9146aa112da0d8ea7aa4bd23246934fc`  
		Last Modified: Mon, 14 Apr 2025 23:07:02 GMT  
		Size: 3.1 MB (3081286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77a525ef5408fe78582a45a6828a837f8cd4302013907d149d8d846f6a5e299e`  
		Last Modified: Mon, 14 Apr 2025 23:07:02 GMT  
		Size: 2.9 MB (2928081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12565515e0434d2c625c719521e180dcfcc6ce2cd8967a411b06ff1a24d668c2`  
		Last Modified: Mon, 14 Apr 2025 23:07:02 GMT  
		Size: 59.9 KB (59943 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:ae8eddd6d49df91cd0af1d714013671977f5196f3e9134485479d2a391d5aefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63453466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51785111beaf3cccd8e93ea3d00609ffe7934cc7963c398ea8dddc84ee337177`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 14 Apr 2025 17:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_VERSION=4.0.9
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 14 Apr 2025 17:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 14 Apr 2025 17:05:20 GMT
CMD ["rabbitmq-server"]
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

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:31de3b69b43545c1b2dc048e9a138695add858e6cdb4160364517ce80d0f8cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 KB (59921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c4ae37b1f992c8737f7ca06d263cd8f5875a77ace72f19efbac4627046ab99`

```dockerfile
```

-	Layers:
	-	`sha256:abd42fcbb5b2be820193ee93cdd4cf222e8ef940373d648067308d08f373af10`  
		Last Modified: Mon, 14 Apr 2025 23:00:59 GMT  
		Size: 59.9 KB (59921 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:63033955d8a762ddd68a6fab0661e30ca2f1ca44a337de2f2b1b428600ff91f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62681417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef437d6b94fc1a167db98f1a9a94bff884af1ffb9a863a9a28af6a64b300b93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 14 Apr 2025 17:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_VERSION=4.0.9
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 14 Apr 2025 17:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 14 Apr 2025 17:05:20 GMT
CMD ["rabbitmq-server"]
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

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:18968d08221588caf1d32db36e4865f2bade3a397119668ea9d517511c4069ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6493245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299932f6e01335d9f4d33094cf8edb78fc1187c6a7c3457d42318641fa29a75c`

```dockerfile
```

-	Layers:
	-	`sha256:719a60f1d6799fce5223e445106190ab91664acb3c604a8d6dc95e9e360cc893`  
		Last Modified: Mon, 14 Apr 2025 23:16:30 GMT  
		Size: 653.4 KB (653359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bffb66baf6ad80c3cb16e04f69b9ca8575ea18bf153790eb1b229063bd69415`  
		Last Modified: Mon, 14 Apr 2025 23:16:30 GMT  
		Size: 3.0 MB (2967140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e23e7ab011a4df994e568419ec126876bb9f3083379c6f5af8113809843c71`  
		Last Modified: Mon, 14 Apr 2025 23:16:30 GMT  
		Size: 2.8 MB (2812610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bea490435d6a3e563e9826b85a6927bd5419265fbfa10b90a2455e9d94f8872`  
		Last Modified: Mon, 14 Apr 2025 23:16:30 GMT  
		Size: 60.1 KB (60136 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:fd836441257fec93b55a7db6f274f85345f84989daabd5b23352eebeac0cb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74516783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00ea7eca5b0d07e5aeadc6c9757cd52b28b24ff28a5a9a027fabe7a8fde4ab6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 14 Apr 2025 17:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_VERSION=4.0.9
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 14 Apr 2025 17:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 14 Apr 2025 17:05:20 GMT
CMD ["rabbitmq-server"]
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

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e5a6703bf9ea1cbe8b9eef5ed63ac9b92ab9a7608840af50d345570fed5271bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6835853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625a52ef01acd06e813d8c005e0de169e1f960461e823f5b12d352d0f3abb014`

```dockerfile
```

-	Layers:
	-	`sha256:8d3e27c6040124cba152551cad199e1ff3eaf6a2c7bb7d1a34ba22961e71fad3`  
		Last Modified: Mon, 14 Apr 2025 23:22:01 GMT  
		Size: 658.0 KB (658005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef170dd6e9367c7bc0a5c902096df072766bc5e54b5b0b9a731099a71c138c5`  
		Last Modified: Mon, 14 Apr 2025 23:22:01 GMT  
		Size: 3.1 MB (3136095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a0503366e161672181e9dad2849fc84363cdda3976e90a5663bd80925f8037d`  
		Last Modified: Mon, 14 Apr 2025 23:22:01 GMT  
		Size: 3.0 MB (2981571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ac8349b175c7f5539c0e8b18ff12e18465940ce5292ea02d0121999eb0da46b`  
		Last Modified: Mon, 14 Apr 2025 23:22:01 GMT  
		Size: 60.2 KB (60182 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:d256d19385a6bd456891f7cf65e3e51de578373fad91e1eeada4aa4950a2402e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64870965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35342390c0e29dd389d2e85a0d490c86d4b928c35d36de9ae5bbfd5b6a716b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 14 Apr 2025 17:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_VERSION=4.0.9
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 14 Apr 2025 17:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 14 Apr 2025 17:05:20 GMT
CMD ["rabbitmq-server"]
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

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8f7f8bdb3c094360280a6a63abd976d1f1c2b965899ffdc1069090f20a6b77e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6699719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c890623810b454be02624380e0d9ed18c8b795fdcb08f3a600274c72b94969b`

```dockerfile
```

-	Layers:
	-	`sha256:84499d62267d1b0e60b38dfee28464aaf9722c7b362f55931d9aee96127954cf`  
		Last Modified: Mon, 14 Apr 2025 23:07:03 GMT  
		Size: 652.6 KB (652563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a428caac3b5ef369f5e36e5437569c3f45b5bec0ba9b23ee792996e0a03681`  
		Last Modified: Mon, 14 Apr 2025 23:07:03 GMT  
		Size: 3.1 MB (3070232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082ff4669c925bf79637727aa52fe1d2424fa04b713581f01d80dd2aab0914f1`  
		Last Modified: Mon, 14 Apr 2025 23:07:03 GMT  
		Size: 2.9 MB (2917031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df63ce154f0ee9c7f4388670b96dfb15eff474f01378246796ea35c00a5f72da`  
		Last Modified: Mon, 14 Apr 2025 23:07:03 GMT  
		Size: 59.9 KB (59893 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:3a3073e17df609db6c205cb0537a1f50880977e758b64f38087d967cba23b3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66005259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e5d1b76e27cfbcd9d77b1eda4bc3fd0ebdfe43df264c1b1ea34bd5da6eab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 14 Apr 2025 17:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_VERSION=4.0.9
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 14 Apr 2025 17:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 14 Apr 2025 17:05:20 GMT
CMD ["rabbitmq-server"]
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

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d34d1b74c05310be8c22f01b78f59b8c8a126483a6554876a171ac804751830d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6731522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91806a98bb7ae700839b3856353f00b72b902cea1f05a58fc6c5b9598b08470`

```dockerfile
```

-	Layers:
	-	`sha256:42e3d42a16aeb699696926d602a654a6f249ad9264d493f164629bb4fe73388b`  
		Last Modified: Mon, 14 Apr 2025 23:20:53 GMT  
		Size: 651.4 KB (651406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfde2f3b55e4435a0abb0930113ff99b957c31cf2f8defd8f10c9088ac30b357`  
		Last Modified: Mon, 14 Apr 2025 23:20:53 GMT  
		Size: 3.1 MB (3087324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1bf623f5122b1bb65722a3a09ae770bc4065a89aece83a413e52370c84dfa1`  
		Last Modified: Mon, 14 Apr 2025 23:20:53 GMT  
		Size: 2.9 MB (2932788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151e4e43563029b8025a025c8fb65ebe30a255d470fc4aea7520d02e142c739e`  
		Last Modified: Mon, 14 Apr 2025 23:20:53 GMT  
		Size: 60.0 KB (60004 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:4ec8489652acba339c35cbe3264758d54fce5af2c1757cdbcfbd68c23ab1f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67688987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8005de5af2816e8c261ec5ae312883cbcdfbaacab31f1db08c3229c5a485973`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 14 Apr 2025 17:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_VERSION=4.0.9
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 14 Apr 2025 17:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 14 Apr 2025 17:05:20 GMT
CMD ["rabbitmq-server"]
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
	-	`sha256:bdb6cef25e62ec3572e4d324a2d8c0bc240aebafdb1c3b48dc1a42ff9e61495a`  
		Last Modified: Mon, 14 Apr 2025 23:34:08 GMT  
		Size: 18.3 MB (18334677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188ee6c7e2b9e4c0347eb5247515dbcb1e286395a70427258bcaa827b188ab7b`  
		Last Modified: Mon, 14 Apr 2025 23:34:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a100051fd76b5edef8832d7e53ec9b658d922675580d071ad751d094de706ff2`  
		Last Modified: Mon, 14 Apr 2025 23:34:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878bf76aa390b3d419a0f4c627d5c3eacf861c0989d071054df11c93c6f4fd81`  
		Last Modified: Mon, 14 Apr 2025 23:34:05 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77df670cbeaaba391b1638162d407abe81a59582255466e80c613a9041a9f845`  
		Last Modified: Mon, 14 Apr 2025 23:34:06 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f02de2538e5cfb196fa055c6d2526a5bcfb23b1905c5541a2fb9cfe7715f6ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6809637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc94471d4c1a3fb4358a5be53c28da766e3bdd98aa020aaa5dacac9dad6fcc4f`

```dockerfile
```

-	Layers:
	-	`sha256:431f86048076f593c59eeda7bd4e244baa8e384dc28451be1cbde984248caa5b`  
		Last Modified: Mon, 14 Apr 2025 23:34:05 GMT  
		Size: 654.2 KB (654198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ad4d42b4c40482b6b4f29904c19173dae8a10af7cfd06b7ea508fa3d52b56f`  
		Last Modified: Mon, 14 Apr 2025 23:34:10 GMT  
		Size: 3.1 MB (3124979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:317405e0392a675de37fd2821094e4a03d55935d7d41bdb7e6bce761939a17f2`  
		Last Modified: Mon, 14 Apr 2025 23:34:05 GMT  
		Size: 3.0 MB (2970455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:591c1c88629be3359d8876d5262bd1a80ee7959d4c28e1079cf07de848c6c624`  
		Last Modified: Mon, 14 Apr 2025 23:34:04 GMT  
		Size: 60.0 KB (60005 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:f5b3403959c779526e3c8a282a867feb45a0eaedcb68d38ba7853e62d5804726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64583347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedb4ca0d3c6b8bcb100cc1f4aed1129b58a05ed75349f1537bd9afafd252b86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 14 Apr 2025 17:05:20 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_VERSION=4.0.9
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 14 Apr 2025 17:05:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 17:05:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 14 Apr 2025 17:05:20 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 14 Apr 2025 17:05:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 14 Apr 2025 17:05:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 17:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 17:05:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 14 Apr 2025 17:05:20 GMT
CMD ["rabbitmq-server"]
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

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ebc2f160707d171305a6952a8debc84c176c1c482eb7af3e7088f855c057bb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c927c82cee95d39a2b70d46a7ba6366fb9ce2ce4a36b32051a4cde3fe6938c88`

```dockerfile
```

-	Layers:
	-	`sha256:f25db1c89059b3043cf1a43a9698d3d4ea7f186311fe0885d2873affed1b4a17`  
		Last Modified: Mon, 14 Apr 2025 23:54:14 GMT  
		Size: 651.4 KB (651372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb5b6f0715b8976fa2c2b3a9f293a260977a2e7eb9bfd68a9058e3d79d7c5bd3`  
		Last Modified: Mon, 14 Apr 2025 23:54:14 GMT  
		Size: 3.0 MB (2977291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5556c9889ecdb35e78a6e2d1012058cb5969a6bf126e18fa0d897b8a47efb87d`  
		Last Modified: Mon, 14 Apr 2025 23:54:14 GMT  
		Size: 2.8 MB (2822785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e7030306b2b948f2c1232bc0d54198c8f0ed3663e7bae7dbefefa4f2a88c33c`  
		Last Modified: Mon, 14 Apr 2025 23:54:14 GMT  
		Size: 59.9 KB (59943 bytes)  
		MIME: application/vnd.in-toto+json
