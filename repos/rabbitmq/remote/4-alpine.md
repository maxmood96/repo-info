## `rabbitmq:4-alpine`

```console
$ docker pull rabbitmq@sha256:2ed5394838c8062947c0b0f298f9fe0f623c8337c6e400dce91ef93c5c1f6c11
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
$ docker pull rabbitmq@sha256:95a0e44e1a320d773072c9caf4222fda2b729fa2a15e2d234e2de62cdfffb954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83463332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f4d47b08cfffeabca479bd0973166b12f57a7b7a87fa7f5e95bfab02f5e7d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 01:20:48 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 01:20:48 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 01:20:48 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 01:20:48 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 01:20:48 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:20:48 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:20:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Dec 2025 01:20:50 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 01:20:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 01:20:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 01:20:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:20:55 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 01:20:56 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 01:20:56 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 01:20:56 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:20:56 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 01:20:56 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 01:20:56 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 01:20:56 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 01:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:20:56 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 01:20:56 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76754f81e30e319e6c384e1bbe35c746500ee6f292af794e658d08364c03af5d`  
		Last Modified: Tue, 02 Dec 2025 01:21:36 GMT  
		Size: 42.9 MB (42857525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9ebdd02fde9716537202a3dbb3337446ed16b789bc30a24ef406d2675926ee`  
		Last Modified: Tue, 02 Dec 2025 01:21:32 GMT  
		Size: 9.1 MB (9143894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1bb203fa29dc1e07141693b72ee92677f78107f3f9507114be1e07596fe41a`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 2.4 MB (2374355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b918a3710bf2d62623eecde367a6d429cc86c9b96a07df8cc19ae82ee49f74f`  
		Last Modified: Tue, 02 Dec 2025 01:21:34 GMT  
		Size: 25.3 MB (25283360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0746859cd5f38587654f7002ee4455b50c94a15dac482b45ba24cbeade2df3fc`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9639f9da06f7de5b5745ed2305f809cdea2f2cfae6c55a6be7da32dcf321bc7`  
		Last Modified: Tue, 02 Dec 2025 01:21:32 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87c6e2195bdd9646b71f7b55461c42712c89db8adb43a88425bfb003c4ca947`  
		Last Modified: Tue, 02 Dec 2025 01:21:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07987d9d6cf001338555cd4c10d47d6cc42988fd4b39987eccabf1939d10b75d`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:787b26cb690373a6dd8ea49568c1484ba32f598057c6b81e01720875473fad60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787e0f2468be6dee63d25a5b432ea83596e2f8b2ec17818473e2c801dbb72f21`

```dockerfile
```

-	Layers:
	-	`sha256:741708f59eef1e29362e493e91e36f116bd593a7f989067120ff07356cd18da9`  
		Last Modified: Tue, 02 Dec 2025 04:55:01 GMT  
		Size: 675.3 KB (675260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3d2a76f01f9f3c0c10d4e89b11d8a945029ef499ab77ff0fd9f90a3d72a3e7`  
		Last Modified: Tue, 02 Dec 2025 04:55:02 GMT  
		Size: 3.1 MB (3102702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d075fe8caeaa94d62dd295dbfa0f28936c0ce1ee4facbb9d219e053ec5c3f981`  
		Last Modified: Tue, 02 Dec 2025 04:55:03 GMT  
		Size: 2.9 MB (2949137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3076103e0407724a2129345a1a0fb280efcb7b12bf984bc804acfed823462768`  
		Last Modified: Tue, 02 Dec 2025 04:55:04 GMT  
		Size: 60.2 KB (60202 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:473cd989b66401b14f920fd418e563bf9a7cd6015198d2336ace29df488b8e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71355537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f6a1833d9896639b5bd2a2ad3d61aa64ebee99b5554a712a1296f9933d3a4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 01:24:37 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 01:24:37 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 01:24:37 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 01:24:37 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 01:24:37 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:24:37 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:24:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Dec 2025 01:24:40 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 01:24:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 01:24:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 01:24:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:24:48 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 01:24:50 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 01:24:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 01:24:50 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:24:50 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 01:24:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 01:24:50 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 01:24:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 01:24:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:24:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:24:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 01:24:50 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907e2f48701b1da3d7f234a011bd13e0985294b4ea89b17afda5a0e09ad77d81`  
		Last Modified: Tue, 02 Dec 2025 01:25:24 GMT  
		Size: 33.4 MB (33447722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bfcd736f4fce6e91072bbd9c35281322f6fdc19b475c6f9f06c1e2e9030fb0`  
		Last Modified: Tue, 02 Dec 2025 01:25:19 GMT  
		Size: 7.8 MB (7788822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5aa6b7df36521a5caa3b7cb972b2012d12ea10a0c05f50a7746e1e23ce5625`  
		Last Modified: Tue, 02 Dec 2025 01:25:19 GMT  
		Size: 1.3 MB (1330059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd4736ee87d39db016f0964397f5a28c38c0ecf95e42a397a0edbd93cb6cc9a`  
		Last Modified: Tue, 02 Dec 2025 01:25:21 GMT  
		Size: 25.3 MB (25283112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e8ba73d09d6c760c88f93f80bf78368999c2fe628139cb45655e1fa650521e`  
		Last Modified: Tue, 02 Dec 2025 01:25:19 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cda988d81a705d751b4eae6903a902ac998f0e4529f6ec01939ecfb79ea1e8`  
		Last Modified: Tue, 02 Dec 2025 01:25:19 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa373a0125a84ca771225ad4cc682b784e428325b64df98aeab4d094a0081d0`  
		Last Modified: Tue, 02 Dec 2025 01:25:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d082e28040c72d736958f68d02be277ce774966361b51e2ab2b045e38bb96af`  
		Last Modified: Tue, 02 Dec 2025 01:25:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ce726de6bdcabc33894c360f794205ee3db8a5658bd4d8b5fe1c5c49d138bfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 KB (60183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e37e88635d0c075a382d4e5b50b49e02e023192468400c277ffaf210288f4`

```dockerfile
```

-	Layers:
	-	`sha256:7a727854852498f0691296976e66b9663e0d636109bb91277f06683652dfb14e`  
		Last Modified: Tue, 02 Dec 2025 04:55:09 GMT  
		Size: 60.2 KB (60183 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:db257a14bad8dde3015c8919cde471a3956c416c29cec4d44b849f890af8a98d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70515991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d22d9edd84aa83bcf0b734b28d45fcf3140d0c8e3a945352c8c304c464733e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 01:27:31 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 01:27:31 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 01:27:31 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 01:27:31 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 01:27:31 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:27:31 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:27:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Dec 2025 01:27:34 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 01:27:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 01:27:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 01:27:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:27:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 01:27:41 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 01:27:41 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 01:27:41 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:27:41 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 01:27:41 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 01:27:41 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 01:27:41 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 01:27:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:27:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:27:41 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 01:27:41 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee7abc4ea5c6857a738dbc85788bad9c2c71ecd8f16d3373c903c4da201db3`  
		Last Modified: Tue, 02 Dec 2025 01:28:19 GMT  
		Size: 33.4 MB (33392501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5692621dfea649dccad70552f57e03888f46e607b35f9bfb91193f9a450de7`  
		Last Modified: Tue, 02 Dec 2025 01:28:17 GMT  
		Size: 7.4 MB (7390639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4faaae5a3415213fcaddc35acd99addd91f677f5d2db9e73bd368527e3aef856`  
		Last Modified: Tue, 02 Dec 2025 01:28:16 GMT  
		Size: 1.2 MB (1227073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759c8479f7d5e3cc0b201189c992d84e1fda0e4708419bff2cdc4dda74baf361`  
		Last Modified: Tue, 02 Dec 2025 01:28:20 GMT  
		Size: 25.3 MB (25282473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb41308acbcb1f0ae1278e339d8be56bc5308d2718c5f2b4cd06d60732de534a`  
		Last Modified: Tue, 02 Dec 2025 01:28:16 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f6a5519116899a1b4dad382a282c965c934da68f58980e6c2cc5d35858568a`  
		Last Modified: Tue, 02 Dec 2025 01:28:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98591ac90f95ac6f646f6299d8ed48227813b3d44af2a7afe5b4f837af2c5057`  
		Last Modified: Tue, 02 Dec 2025 01:28:17 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5eed1ca42e4db016b27e8488f575030d10540cc23464eca2094edd640f925a`  
		Last Modified: Tue, 02 Dec 2025 01:28:17 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:58b84326068b6e08334c6b9ba006a01f4ecaa29addabc113d803eb8571efa8b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6551608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d267a1fbbdd71a1b8ba11233c24b2f469e5116c4c1904d899cd7b3b42d1166c2`

```dockerfile
```

-	Layers:
	-	`sha256:f93468a5f414714de34625a950b936b8ccda0faa661f705ae4c50bc6ba0785a8`  
		Last Modified: Tue, 02 Dec 2025 04:55:11 GMT  
		Size: 671.1 KB (671053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13859f79b4b6ba7ffe9d719f4f27fa6e54156f63ecc8cce9440a34f36ec2cae0`  
		Last Modified: Tue, 02 Dec 2025 04:55:12 GMT  
		Size: 3.0 MB (2987525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74ef741a7ff5817a182d3606caf925a64e01367f09a6cfacb03c214d488120a`  
		Last Modified: Tue, 02 Dec 2025 04:55:14 GMT  
		Size: 2.8 MB (2832631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2cbc474b309d2b741badfa23edbdd461b0ab752f20a4ee09964debfbc68cf18`  
		Last Modified: Tue, 02 Dec 2025 04:55:15 GMT  
		Size: 60.4 KB (60399 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:937c408261ec81e1970d65d3e77f88ef7a82ef33e8fabad1d2eb36a522403ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82526560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858aa0a5bf2ce7c11a8c2316c5b5098c611e0fda44e0b6a646630d61f7639385`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 02:37:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 02:37:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 02:37:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 02:37:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 02:37:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:37:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 02:37:58 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Dec 2025 02:37:58 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 02:37:58 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 02:37:58 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 02:37:58 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:38:05 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 02:38:06 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 02:38:06 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 02:38:06 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 02:38:06 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 02:38:06 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 02:38:06 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 02:38:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 02:38:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:38:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:38:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 02:38:06 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08952f9c36eb84cb040bed9b036bf58c1d0e0d8b401fa68e0b279f7c9af67f57`  
		Last Modified: Tue, 02 Dec 2025 02:38:35 GMT  
		Size: 40.9 MB (40854391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84bbd585c96345261296eb4e84d8685026a921e0a98d409ab0d8c334e5db47b`  
		Last Modified: Tue, 02 Dec 2025 02:38:33 GMT  
		Size: 9.8 MB (9824251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18df66cbfbfe7ece40876ed512aac805dca7c6288e89a178f27553e30c07e7e`  
		Last Modified: Tue, 02 Dec 2025 02:38:32 GMT  
		Size: 2.4 MB (2424769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe72c5895471110e91259e536729840065025172fd7da0430a20be5ad519852`  
		Last Modified: Tue, 02 Dec 2025 02:38:37 GMT  
		Size: 25.3 MB (25283337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33302a43c1b51c80eee368912daa07b8189b2a17ac6598f4156055014d2279ea`  
		Last Modified: Tue, 02 Dec 2025 02:38:32 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6150632b41975c3931a1e2c6d4e35a14e231bb326f971f6f67bf620c48fc30ad`  
		Last Modified: Tue, 02 Dec 2025 02:38:32 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1801bdc972f8f58e63736e6c55628c11f4a24856a2746a5cf779dcf092d07f`  
		Last Modified: Tue, 02 Dec 2025 02:38:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a47381dabf1e2b077123c5d52221edf9d9d9d03884725a06c53cba503f04114`  
		Last Modified: Tue, 02 Dec 2025 02:38:32 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fde1316d6ee38db32ae7e7b07a419239760f0ebae67e60217b8e2b0388b0f988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6895606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d334da1305e99e2d8afdb102713ebdbf077e2bbe77390b7ac8c23b6636f933`

```dockerfile
```

-	Layers:
	-	`sha256:3f6327f41918ee832e07b54bfe81af9fedabf93f21ee0d1914c2a7d3ad9a203b`  
		Last Modified: Tue, 02 Dec 2025 04:55:19 GMT  
		Size: 676.1 KB (676053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aeea48d25e02f2556205dd4133c4b2bd4b5fdf5d786a3bcdebf638e255503f5`  
		Last Modified: Tue, 02 Dec 2025 04:55:20 GMT  
		Size: 3.2 MB (3157000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b52530598e21621a57924e905d0b7630c7eee3f2366859230baaf4113f2037`  
		Last Modified: Tue, 02 Dec 2025 04:55:21 GMT  
		Size: 3.0 MB (3002112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f473a035fb017b05d2b311855b4f4105b452da617e832773540d36b6469d02ca`  
		Last Modified: Tue, 02 Dec 2025 04:55:21 GMT  
		Size: 60.4 KB (60441 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:a47ccc2bef87a2f08636e65d7ca75e2a8a9c84f1ba5f6904c6833599ebab8603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72931976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778c698a2a811433c081167f73b5038a5433e30aca5dbe64d5c20b5f88f07dbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 01:19:39 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 01:19:39 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 01:19:39 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 01:19:39 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 01:19:39 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:19:39 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:19:41 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Dec 2025 01:19:41 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 01:19:41 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 01:19:41 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 01:19:41 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:19:47 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 01:19:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 01:19:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 01:19:48 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:19:48 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 01:19:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 01:19:48 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 01:19:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 01:19:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:19:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 01:19:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b044db7fe75056686c0355ade89c95e4072d032dbb2a1ce3a1cf64134b75fc9`  
		Last Modified: Tue, 02 Dec 2025 01:20:13 GMT  
		Size: 33.5 MB (33537199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612a27ea3303e44664ab5500e89cc518ca446e43e04a76ef952bdcb842b3c6ef`  
		Last Modified: Tue, 02 Dec 2025 01:20:10 GMT  
		Size: 9.2 MB (9159127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327fc1c3008d2ba6b26c4853547976a80fc9b3e6f5b6860ed891b789e33ddccd`  
		Last Modified: Tue, 02 Dec 2025 01:20:09 GMT  
		Size: 1.3 MB (1332469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d237809b18ee3ef8208efbaaaa1d7a3b292864eac03cb98970c37b7f3a6170`  
		Last Modified: Tue, 02 Dec 2025 01:20:14 GMT  
		Size: 25.3 MB (25282501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d4da5b3e291513525f2ec75463c2c2f6c51da8d6ed321afbf6a8dfa1ac164`  
		Last Modified: Tue, 02 Dec 2025 01:20:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94929261962ab15a5e47ffeeb99dc8c66c040e1c7626c8dc34251c77be2734f7`  
		Last Modified: Tue, 02 Dec 2025 01:20:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbe55a419f7cffb14f7733e73582f1c47b65f8c8a763d0e13377f37d947a561`  
		Last Modified: Tue, 02 Dec 2025 01:20:09 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d8dc58d577465bc3b0ced391b31f7d0e7115af18a360ac51056f05af2794a`  
		Last Modified: Tue, 02 Dec 2025 01:20:09 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f4273994997e4eece5eb86e1c26eaf7ec1b1062223b525f76f5f0fcbf94258d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6760142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8424d0bda5d9371c2d6117c0d76afeb6cb8cfe21354b8b858dc5b89aa145a15c`

```dockerfile
```

-	Layers:
	-	`sha256:6d2c116550431aca8d37b92ba6418090074e048cc295a8da17e7177ef9e83272`  
		Last Modified: Tue, 02 Dec 2025 04:55:26 GMT  
		Size: 670.3 KB (670255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d739f9284aa8f12164a989c09556deb83d9d579df30c37511b2b4e32cd35e309`  
		Last Modified: Tue, 02 Dec 2025 04:55:28 GMT  
		Size: 3.1 MB (3091648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c2a17e39d8d9c49d3362fec430da168f36e30e698103aef23c662859551c61`  
		Last Modified: Tue, 02 Dec 2025 04:55:29 GMT  
		Size: 2.9 MB (2938087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dd89e12d4a283fc3c59b586b86b7b92dcced01b81f8cb4dfcdcf1430d38913c`  
		Last Modified: Tue, 02 Dec 2025 04:55:29 GMT  
		Size: 60.2 KB (60152 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:221f7c6766796d6f5c83ea830b9b04e6f32e0214fb590b30f6d595b05a7cf521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74171778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e130b4a45cc02797e5dbf0b579bbd6948d55841c933e14b5b3d45e5a233edda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 03:10:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 03:10:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 03:10:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 03:10:57 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 03:10:57 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 03:10:57 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 03:11:01 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Dec 2025 03:11:01 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 03:11:01 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 03:11:01 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 03:11:01 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 03:11:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 03:11:16 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 03:11:17 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 03:11:17 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 03:11:17 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 03:11:17 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 03:11:17 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 03:11:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 03:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 03:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 03:11:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 03:11:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb09f7881c47f349707667cdeb108b5f7867370368f6fb6aaebb0b4dcd62339`  
		Last Modified: Tue, 02 Dec 2025 03:12:12 GMT  
		Size: 33.9 MB (33928482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dec72143037c6806382c68e959103cd102180c0e0c918f116269664654c53`  
		Last Modified: Tue, 02 Dec 2025 03:12:09 GMT  
		Size: 9.8 MB (9774066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f3cf68ba59680c4112914fa5a96d9549456b3a6b7671878a4d775d79af5a3`  
		Last Modified: Tue, 02 Dec 2025 03:12:09 GMT  
		Size: 1.5 MB (1452634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c15eebd911fd50c7cfea65f8be2dd94aee390e1a430ee11932ed2f1a977860`  
		Last Modified: Tue, 02 Dec 2025 03:12:12 GMT  
		Size: 25.3 MB (25282596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e64c1997c64ef2803cc0dc00a350727dfcf05b4fdfc140260d2a4207850808`  
		Last Modified: Tue, 02 Dec 2025 03:12:09 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ef302a62da4e2430bfe986dc8fc40e1534654755b249570ec42b555f1e2594`  
		Last Modified: Tue, 02 Dec 2025 03:12:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39efb845f3a32676acb74c271c58ec227474617276c7f92821271712478b0f42`  
		Last Modified: Tue, 02 Dec 2025 03:12:08 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1986fa0060f535ed9c2442352b92b0bea1a4146836363018331c3dee15bfb714`  
		Last Modified: Tue, 02 Dec 2025 03:12:08 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:631ccf29f705d6d91835920287300225031d101f40c2bf260f2983c6b541a2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4120059df8fda14e03041a4a59cf0dba9487b81546e635add9e38a632224cce7`

```dockerfile
```

-	Layers:
	-	`sha256:1414cb7aa49c9eee6de685c94cd35f4b8ebd1e80dbc0b2f720bf31e68fc1ff78`  
		Last Modified: Tue, 02 Dec 2025 04:55:34 GMT  
		Size: 669.1 KB (669100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b01dfd2b6fbae38d39269d569d17919d8a93628c613bac8a4d23a84132b6d8`  
		Last Modified: Tue, 02 Dec 2025 04:55:35 GMT  
		Size: 3.1 MB (3108754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09bb21b635315e0c24613b979315871d3aa54258fb20ddbe3ef8e96fe3ad36d6`  
		Last Modified: Tue, 02 Dec 2025 04:55:36 GMT  
		Size: 3.0 MB (2953854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a969530625d779bc4365d286d67d24bdaf7b275d5e89ccd017b70cbe49521b`  
		Last Modified: Tue, 02 Dec 2025 04:55:36 GMT  
		Size: 60.3 KB (60264 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:5cade653123f5313dee5ee7099bff93ed318d042e0b2f2d4e9a6b18c67e599fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75965721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c416393a96e635de7e47b36cb0f2285d87a44c42ed8eb0554499df1ac175bd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 15 Nov 2025 12:40:37 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 15 Nov 2025 12:40:37 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 15 Nov 2025 12:40:37 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 15 Nov 2025 12:40:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 15 Nov 2025 12:40:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 12:40:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 15 Nov 2025 12:40:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 15 Nov 2025 12:40:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:20:39 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 03:20:48 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 03:20:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 03:20:48 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 18 Nov 2025 03:20:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:20:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 03:20:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e59a1c1b9f6e68d2e81dfe93f128277d090e8d42bb80d9fdce1bd0812253e90`  
		Last Modified: Sat, 15 Nov 2025 12:47:29 GMT  
		Size: 34.9 MB (34892992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b82b64d03f44428bb7c7c84bc38b196743066f1c2cd8073fa6e2958a1f2364`  
		Last Modified: Sat, 15 Nov 2025 12:47:25 GMT  
		Size: 10.9 MB (10906598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445ba2528747173700141a982a31baa29e2bb537c0faf37187397c5cef3d8ac0`  
		Last Modified: Sat, 15 Nov 2025 12:47:24 GMT  
		Size: 1.4 MB (1366487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ab85becded663592a6bc65df027d3b64784a81fde022e9ef0f2d593a067f8f`  
		Last Modified: Tue, 18 Nov 2025 04:39:50 GMT  
		Size: 25.3 MB (25282651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c6b0a6f4b731df4b2017078d1d133e2cbed722a0bca6e74485cc38e59b447f`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e1906d3f3c215386290a7ef260fba1c1a172ded9261e1333dfc67ea58d0473`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f065a8e08b979e6b746f95b8f4fc2e86e14d9b444bf9212b642e4e55b9c3833`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb79fb793b07ee339d044a1fe1e5e3f5dd9213f52951f7d84366dd805ae73a`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:53a741c41f73a58327d751bafcf55a28b79b7408e602d9b826fd9f6f51ee1896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6871306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d32d52fba2d8ab99a17f61818c0008cbbcbcdafc90b8bbf3ac6e77e9d741a28`

```dockerfile
```

-	Layers:
	-	`sha256:fb7d5bb6f27fb41df548cf4d7ef09809923c6f515cabc4e3e567caa3fece52a3`  
		Last Modified: Tue, 02 Dec 2025 13:53:12 GMT  
		Size: 672.1 KB (672069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75168eb38c6a68f809fa633e77bcb41800e6a43dea1d6ee64f55d172c5e13668`  
		Last Modified: Tue, 02 Dec 2025 13:53:13 GMT  
		Size: 3.1 MB (3146927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2027b801be77776683a9b2852cad0ef9eca1c10eb6c3ca44144143131ece7422`  
		Last Modified: Tue, 02 Dec 2025 13:53:15 GMT  
		Size: 3.0 MB (2992039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7daa45a745fec68dea6a2453843d531f45b9a9ae14a8cbfd65fb34d6d296349c`  
		Last Modified: Tue, 02 Dec 2025 13:53:16 GMT  
		Size: 60.3 KB (60271 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:c78d16adc1b5951316b4fa6095408b8064531426f08dfd5202789f980f418857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72675080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbf4a69c7ace961cc906bd3b16f98e6995788f2423c0895a7e8164d513a12a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 02:55:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 02:55:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 02:55:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 02:55:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 02:55:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:55:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 02:55:17 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 02 Dec 2025 02:55:17 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 02:55:17 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 02:55:17 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 02:55:17 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:55:41 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 02:55:44 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 02:55:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 02:55:45 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 02:55:45 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 02:55:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 02:55:45 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 02:55:46 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 02:55:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:55:46 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 02:55:46 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053dc0846d78dd576c9c92aa5cfbcf7f2abeb9a7a442e368caa520f7df52f4a5`  
		Last Modified: Tue, 02 Dec 2025 02:56:39 GMT  
		Size: 34.0 MB (33963558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde2085300070faeb8af6aff7e09a2ff1407172fcc3a63ea14e3870848f04bd2`  
		Last Modified: Tue, 02 Dec 2025 02:56:38 GMT  
		Size: 8.3 MB (8347197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d6ebc0d61496ec84604342d9868c4992e1e5b84daa2857c8ebb1627d29965d`  
		Last Modified: Tue, 02 Dec 2025 02:56:37 GMT  
		Size: 1.4 MB (1430648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54d8c09b0d6ca30a668c66c026ab0654473554271f8d4048de609de6a1cb996`  
		Last Modified: Tue, 02 Dec 2025 02:56:40 GMT  
		Size: 25.3 MB (25282677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43074ba2ba9779e4545d998d64f4ec9514edc95ff25cd7c0049460bd602adaf`  
		Last Modified: Tue, 02 Dec 2025 02:56:37 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01b9ae4eb769280a2f85fedf0b610e0787a670f290c0fd38bfa8914208ef8c0`  
		Last Modified: Tue, 02 Dec 2025 02:56:37 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d670d6c668d8ed1ec030e60b511fb9d7e838bd6e057fff4155473ea1581b0b81`  
		Last Modified: Tue, 02 Dec 2025 02:56:37 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab57336827d6bc4307243efdcc2186357f6f5bb216066e3fa829f694942a3a5`  
		Last Modified: Tue, 02 Dec 2025 02:56:37 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:59da99ae4cae9aaf3d6d3517ba94991e1e00441a8fd887535858e348a364e308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6570780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3922da5b63eae4c90b97a04b1e59749670a81664bc23c8e3a4ef12a71bab54e1`

```dockerfile
```

-	Layers:
	-	`sha256:ee853b00f071a5b4335dbefec5d85d66df54b6237f9184a65dc626b584c7a968`  
		Last Modified: Tue, 02 Dec 2025 04:55:45 GMT  
		Size: 669.1 KB (669066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf50f1d75c85ca92191297628a35166480534a3cd8d5307d72846a5958e905cf`  
		Last Modified: Tue, 02 Dec 2025 04:55:48 GMT  
		Size: 3.0 MB (2998191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:281e96d3a90d347c1ca92656f699f5ec6014b713479ca62f6f2e11cae4d818ef`  
		Last Modified: Tue, 02 Dec 2025 04:55:50 GMT  
		Size: 2.8 MB (2843321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:414c47440fedd742b26f83677d7c6ab63061122015ff747c592d6ab225f6bfa5`  
		Last Modified: Tue, 02 Dec 2025 04:55:50 GMT  
		Size: 60.2 KB (60202 bytes)  
		MIME: application/vnd.in-toto+json
