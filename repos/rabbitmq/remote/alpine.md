## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:f8b3601fba0bbda709a0ae23e5df9fc0155f301a0f515894fdbfd5bc229abb64
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
$ docker pull rabbitmq@sha256:af0ab0700df2a2725ae3c18ff3df313af878b75e5391b03f34b131fafecaeb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77580835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb34294c5bb20662271e07f2bc177922d0a5893e241f22aba3b8046e875ccf10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e907fb34e6bc18c69a602e0855ca77c9fa9acaa3d7b5a04ea5ce8e33a9c32884`  
		Last Modified: Thu, 19 Dec 2024 21:38:44 GMT  
		Size: 45.0 MB (44989091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2777f2942bec64f35192baa34c4a2e2d768313bd35262f499fd3fb92f5d8c132`  
		Last Modified: Thu, 19 Dec 2024 21:38:43 GMT  
		Size: 8.3 MB (8309031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec817ad43288cdd2ce0b70696a394de2206e1c26cc094eb7b4346191ff669ec`  
		Last Modified: Thu, 19 Dec 2024 21:38:43 GMT  
		Size: 2.3 MB (2277801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e643087122e467f201cae1aaae5019c32edb92c7171872c6d6a37c1c365862`  
		Last Modified: Thu, 19 Dec 2024 21:38:43 GMT  
		Size: 18.4 MB (18358734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cfbee5958681ebffc18761695a3ac44bed3c4df150018f4ac6acc261893c87`  
		Last Modified: Thu, 19 Dec 2024 21:38:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1227fab201d1716cb708df0bafb4208c275e6dfea5186c86d4dde1c1569deb`  
		Last Modified: Thu, 19 Dec 2024 21:38:44 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2918b652014ba49f4310454511a93e8ea451e8103eb89a8f2cd9677f65d6a407`  
		Last Modified: Thu, 19 Dec 2024 21:38:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665338a97ef892dced81092bcb9a626dc3bcd32a216294c0aed8a062b0e51edf`  
		Last Modified: Thu, 19 Dec 2024 21:38:45 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:44f5e33af8e7851e2c29703b6d40971d279eec504b98c591ca9ee6993bc866f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6727216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77edb475fe9035013de87c6e19db21845a93579d8725d188d69beeb636990fe2`

```dockerfile
```

-	Layers:
	-	`sha256:156894dfa934d4682899b03acd463337e81fbf92b9ee3771f7a42383b89f5258`  
		Last Modified: Thu, 19 Dec 2024 21:38:43 GMT  
		Size: 657.8 KB (657762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8371e3ebdd863663d82002a2b621165c44924e472b4356977310d6ea561b294`  
		Last Modified: Thu, 19 Dec 2024 21:38:43 GMT  
		Size: 3.1 MB (3081557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad4bbc1525d8ecd0d07fb47fdfb1c711a2d17ea132924dc5123bc801c2dbf0b1`  
		Last Modified: Thu, 19 Dec 2024 21:38:43 GMT  
		Size: 2.9 MB (2928053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8731bfe7162e440e1e21dff29eef527fecce6a3f5129a663fdcfd33ed498cf3a`  
		Last Modified: Thu, 19 Dec 2024 21:38:42 GMT  
		Size: 59.8 KB (59844 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:1e3e5b6f84f13a5501d7d14ecdc8fccfe89ae8b77910c223c7bc52ca4b4a648c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65652626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac147ce909156e3369d89b41f402e355d182069f5d0c3881af5c5a1de4f061d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f43b77c6b5dbe8fa8d2f1220c266d1c39dd7552db5064f73d9d7072712dfb59`  
		Last Modified: Sat, 14 Dec 2024 01:40:33 GMT  
		Size: 35.6 MB (35607436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c34796c76e4621e629db3513edaf0d979b7a27c760218d80dd593258db412f`  
		Last Modified: Sat, 14 Dec 2024 01:40:32 GMT  
		Size: 7.1 MB (7092017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b99dba44cbdabf43a01dcd7c35534b4d7c57547bbcc120e5b555da93dfa2f`  
		Last Modified: Sat, 14 Dec 2024 01:40:32 GMT  
		Size: 1.2 MB (1225386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5433bd9a22621d3ec4bce70891189338d3bbaa8c67fcb33595786cdfbccfd1b5`  
		Last Modified: Thu, 19 Dec 2024 21:34:09 GMT  
		Size: 18.4 MB (18358860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a4220c453713ea7898ede8762c944ebb974b73eae22a9ffb42bbc2e15a56f2`  
		Last Modified: Thu, 19 Dec 2024 21:34:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c52e159af917b25866e9f62ba1d03785ee35ec892c94984848a28913d7c9ae9`  
		Last Modified: Thu, 19 Dec 2024 21:34:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7117bb60db7c78b0914b3be3aaba94a4e8e0bd7b4352262af54736af52990fad`  
		Last Modified: Thu, 19 Dec 2024 21:34:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b8b2929c88eaf898747403c13ba4e636a57400f9cdc74550c8641dd6ea13cd`  
		Last Modified: Thu, 19 Dec 2024 21:34:09 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:764a86252e6f11afe99dcbbaf6b210fd54592f14ef6082f00166a91fbe04d8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e16324d3d0108a48d0fc13b9a73589f4368513196bfc5e4de6c3643a4fe26b`

```dockerfile
```

-	Layers:
	-	`sha256:c3e894f44332cebb5d80ee7972ad8690ae6533e4bc39925151624be70d9f64f8`  
		Last Modified: Thu, 19 Dec 2024 21:34:08 GMT  
		Size: 59.8 KB (59821 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:5eca1825f85ba4298a5bbff224434a41cb866d9a794ad896f2726dda7b89aea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64851087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac28755e6463773f31d1b361f8e276a54a0ff87da7e95371b61c7241c63a9275`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2b3721282056a0fbdf0b389f8240ea975c82b77984990f1d8480f41dabf5a9`  
		Last Modified: Sat, 14 Dec 2024 01:51:43 GMT  
		Size: 35.5 MB (35525480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b49e7d4cf7950ef2ecaae88c8aa09bded6033ff8154ea428b91f87f0d5649e`  
		Last Modified: Sat, 14 Dec 2024 01:51:42 GMT  
		Size: 6.7 MB (6731663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaabce4e233913d3a7d3fc8356167acf9062cc7024f5d7b53daae1bfc3500b0f`  
		Last Modified: Sat, 14 Dec 2024 01:51:42 GMT  
		Size: 1.1 MB (1133163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a7e4475a241c7e348dd4681d5e8957e2256397625be363ab56bb462f83cb9b`  
		Last Modified: Thu, 19 Dec 2024 21:41:22 GMT  
		Size: 18.4 MB (18359015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6037f5d0bf9be972c421689af3f0165af9a5bc68429ba3dd97c7b6aaf5da3f`  
		Last Modified: Thu, 19 Dec 2024 21:41:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280063e9c6321d523e8ec2bb6d87ab1e1eb7c76d09915f84f6427d3c5a7520f0`  
		Last Modified: Thu, 19 Dec 2024 21:41:20 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0467496ad0e3d726b44e31b9c376fa2c7ed5530dd45b3c0865efaa48221f2fcc`  
		Last Modified: Thu, 19 Dec 2024 21:41:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff14851dee66a29f9deb10ad19608e8198968dcaa4039c994bd4fb5deff16501`  
		Last Modified: Thu, 19 Dec 2024 21:41:21 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:899068631bb772e648f9dd597b4864ef1af53067354108df1324bd47b37f5e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6493931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4f674a38efc2fdca951d2c1ad633851d0bae6faa059f0cc2fa044e36561849`

```dockerfile
```

-	Layers:
	-	`sha256:205191bb2232bfa27050b9e59ed495481f427d3e41b73022c9735da0f8f8732d`  
		Last Modified: Thu, 19 Dec 2024 21:41:20 GMT  
		Size: 653.9 KB (653905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c104e092c2741cb5ea2aed92a503a2800c3c28aa0dcc1b90405f2de468f2c91`  
		Last Modified: Thu, 19 Dec 2024 21:41:21 GMT  
		Size: 3.0 MB (2967407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf51c11a8e80322cdafd49fdfd72c4c25f8e5b0acc265bef8ee4fe190af639c`  
		Last Modified: Thu, 19 Dec 2024 21:41:20 GMT  
		Size: 2.8 MB (2812582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3356fb4ae8412393df9759504cfc6cac43820590020a0c47472e3c6aea65dcc9`  
		Last Modified: Thu, 19 Dec 2024 21:41:20 GMT  
		Size: 60.0 KB (60037 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:892e1a11b110526cfd0c5643d00e10c4584673fee3a29f5b09384d95c84aa3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76710545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd1efe43f369795186652efafc91f6fa382804cc8f985c9d5cc69e7e6c3fbd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4238ad45379eedef68550f708ba0b66ebf0966969211d3f98dd5cd48580c85f`  
		Last Modified: Sat, 14 Dec 2024 01:49:23 GMT  
		Size: 43.0 MB (43002128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48299d35c659b6409c1cce3634fda16fefc1d027d69e4982af580262fa43b98`  
		Size: 9.0 MB (9031962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c289f326f6712b60e1def2ef3a349f4342d63432909457e67a851f40b21e022`  
		Last Modified: Sat, 14 Dec 2024 01:49:22 GMT  
		Size: 2.3 MB (2322570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2887b587ab562ae474fcdcf80f8ee2b5ef890c8e068ac7dcacb44e74fcb68a00`  
		Last Modified: Thu, 19 Dec 2024 22:46:30 GMT  
		Size: 18.4 MB (18358955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eed70cfe90941ba276cc6e602b3093d8d4fa652fdb22c1ed8e444374d57b20b`  
		Last Modified: Thu, 19 Dec 2024 22:46:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dd71c231555c60b0f5de3677a3caa53997bba2802962b5e77c7f21cc899be4`  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1285d662420bd0a73bfd9ec0e465b1c3e5894a69f2f586dc3d5afc10488833`  
		Last Modified: Thu, 19 Dec 2024 22:46:29 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d119eb53d1374b947c29fa739791e4ff1fe613b04e7803f7966e1f5758f13b36`  
		Last Modified: Thu, 19 Dec 2024 22:46:30 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:90e8056ec148bac5c87737ef63c01f51e3830a74e98b34e1f9e73316831eb279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6836539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa8e60cd14fa916a7cdba2c52f6fd1917578999cfa4bd3c44d814cbd35eee51`

```dockerfile
```

-	Layers:
	-	`sha256:d60217eed5c80ffb320fe2f5f35e3cb34583e41e739e0e507645239fe6789c0b`  
		Last Modified: Thu, 19 Dec 2024 22:46:29 GMT  
		Size: 658.6 KB (658551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f1d7eff3867ef3148dc5012fd4e39a522551d4ca6f9811201e97607dd8c1fc7`  
		Last Modified: Thu, 19 Dec 2024 22:46:30 GMT  
		Size: 3.1 MB (3136362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d1dba8c19e6f0236f522ce526bf875bea7ee761c7ac1de67e0bb7f668069c6`  
		Last Modified: Thu, 19 Dec 2024 22:46:30 GMT  
		Size: 3.0 MB (2981543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0e19b8cba8c2f5c2089fc385a77888211ad542b2d1b96c5091b555bf0cc129`  
		Last Modified: Thu, 19 Dec 2024 22:46:29 GMT  
		Size: 60.1 KB (60083 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:cbb253ef5c1b0aaa26018d7165b2999e712322e53a339c9ed8f99fe3a3d38c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67061351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16696b0453c8c6bf0e2f4e45272020fa240c7ca2a39eedeb5007a277dabe5c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db9fc14965806d89c7c445a6013184372339f9286c08050ce2e365d96055fcd`  
		Last Modified: Thu, 19 Dec 2024 21:38:04 GMT  
		Size: 35.7 MB (35684325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484db9460efa3950edef40f713642675789d98ba6505198f133fd59a3c8da1ba`  
		Last Modified: Thu, 19 Dec 2024 21:38:04 GMT  
		Size: 8.3 MB (8320817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6227325681dbe15422a7a7e6ba61182ec6ad74712e9f86c048763a6c7bfd797`  
		Size: 1.2 MB (1229364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed7f9b5890cae4383ea83f236c9d95b4f5c1954f20821248472795c7b695b7b`  
		Last Modified: Thu, 19 Dec 2024 21:38:04 GMT  
		Size: 18.4 MB (18359020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d134a6a805921305322f3eeb733da5a6064271edd8c988615a624baef09562ee`  
		Last Modified: Thu, 19 Dec 2024 21:38:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac0f9f92a7f0867c526b0a54fcb3795278415d84ae836caf07b48443549c400`  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5868ef92ca1387be47d4e7ba7976c015577b17bfc706a16e8136ae484bf0bfde`  
		Last Modified: Thu, 19 Dec 2024 21:38:05 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda47255bb9912e1bbf39e0df4522d267bacd1f12aa9e685b04ee29996339f09`  
		Last Modified: Thu, 19 Dec 2024 21:38:05 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:874d36fac703eb53e053a96dfa47902b7a45bb40e7a487f5db84f41436df78d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6700411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acccc8a9b7f8a15d8ca0256f7a201f7a2c1742a85bfb82fbfff68bd634c2979`

```dockerfile
```

-	Layers:
	-	`sha256:6b5727f4d24ed1598705d0f3559c92dea27a3c9754136b6760af3cad2ba2dfd2`  
		Size: 653.1 KB (653111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec32b5e287c42712b3030b1fe8d6e1730c71bc3e9e0b7910c6b3d5fd260e48ec`  
		Last Modified: Thu, 19 Dec 2024 21:38:03 GMT  
		Size: 3.1 MB (3070503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9fa1b41d2b2f7d8c7a18a09059146d87b4453a7de45f31fb2590485b22c5e5`  
		Last Modified: Thu, 19 Dec 2024 21:38:03 GMT  
		Size: 2.9 MB (2917003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ba1e75b4f672d88a37215800d82856d72abda1736acca7e58cf89fb7f09511`  
		Last Modified: Thu, 19 Dec 2024 21:38:03 GMT  
		Size: 59.8 KB (59794 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:ae2ceec8e9e7ece230184cc9ddde298cf7c96d0c500511a3cc520e10496903ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68213520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e891a9bddca8e21b66cb7d0a6a62795021b219589aa70ea1a5298239f28b17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae669fa4c5857c6d1aa412cad83cc689814c39d34d04706f2ad8b1d4cdfe75`  
		Size: 36.1 MB (36086068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fd4f386fc168cc8ea2c2b838896d544e94a415dc6ff0615006587c747a31ce`  
		Last Modified: Sat, 14 Dec 2024 01:47:19 GMT  
		Size: 8.8 MB (8844392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c16c84696303b681eb233651db78c833f843c3f64da1fe2476b19a618e78099`  
		Last Modified: Sat, 14 Dec 2024 01:47:19 GMT  
		Size: 1.3 MB (1345139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04c79a600e50e21e69fd274a29da8f4593eddb866c84d3054c2277c9d56b73`  
		Last Modified: Thu, 19 Dec 2024 23:04:42 GMT  
		Size: 18.4 MB (18359061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ca58e0cdf49f0f87d65f09386117de828312014754c613ce4d5c640ffebb8`  
		Last Modified: Thu, 19 Dec 2024 23:04:41 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787a0dd93063d1d9b17855d554e5057f17f9c49e747b041ad0deca4d55bd7e75`  
		Last Modified: Thu, 19 Dec 2024 23:04:41 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30201452b03fda8840d66a6f449cd69cce633ee444c738406e82331fce89215a`  
		Last Modified: Thu, 19 Dec 2024 23:04:41 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d500cf88bf3cbc4c8bff7502f81bab6a363b5011b98ebd11de071c91d4412`  
		Last Modified: Thu, 19 Dec 2024 23:04:42 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e85840dc25b1b3b1320ed800228d4eea8fba9c14912d0d52f81507d527b71fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6732209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7112daa53ab3e9bc348d031511a78e94644b4afb3abbb2583967aebedcbffbc2`

```dockerfile
```

-	Layers:
	-	`sha256:55c5e090662813e01c37f9cad048bd1cf76e71da449fbc56ac07dd3fe7d9e15a`  
		Size: 652.0 KB (651952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9167d50f9ba9c4cbe234a224bfe4da975585b51c6a5bf7e1a086f2b6fe36a188`  
		Last Modified: Thu, 19 Dec 2024 23:04:42 GMT  
		Size: 3.1 MB (3087591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7b7e6354e2e4ad3d1ce30b81e6f40d151d3ac7dea96020449f5d96d9a4c9ba`  
		Last Modified: Thu, 19 Dec 2024 23:04:42 GMT  
		Size: 2.9 MB (2932760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9882be4f94532c46eb9da8fdba05ebf85f8b0e5bdaedfc290536ea20581e1985`  
		Last Modified: Thu, 19 Dec 2024 23:04:41 GMT  
		Size: 59.9 KB (59906 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:893d3ad6b9696092c1addee1ed3beab1c4183da00ba1a14f140ff5995050afde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69862279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007f74ab4fece4bfde638807fe9bbab7b40a034cd2aecdf870af607665bf188f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f359027c27b19d95fc947dcd7e167020faf9ba96fa247b2f309772108cf5c0`  
		Last Modified: Sat, 14 Dec 2024 03:43:41 GMT  
		Size: 37.0 MB (37028323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2c797e41b0fb5384ce013ea72f66a5625585169049f297885e7c2061072ca0`  
		Last Modified: Sat, 14 Dec 2024 03:43:37 GMT  
		Size: 9.9 MB (9854310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48c2e72bba74432ea92c840dc923373673e2146e559cb70493f77492e6f6c41`  
		Last Modified: Sat, 14 Dec 2024 03:43:35 GMT  
		Size: 1.3 MB (1265041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f43ac3104e3c0b35911a978dab456856e20e3efb4b0373957cf0c3ee51d1f54`  
		Last Modified: Fri, 20 Dec 2024 00:19:55 GMT  
		Size: 18.4 MB (18358836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb17ab1e423e7a0e66fd9d9c5058cb7debe65ac636049590413b80e4f9430a8a`  
		Last Modified: Fri, 20 Dec 2024 00:19:52 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9316d5c73b3073322d90c5118045f53b352833ab23e4a2935f92e9aba8300fc9`  
		Last Modified: Fri, 20 Dec 2024 00:19:52 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f615432c00c0bc33c10ef0d45da09ec9abc6ac6d888285dba276340b599d8`  
		Last Modified: Fri, 20 Dec 2024 00:19:53 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3185baf7f69d1eceefb37f84b921fb25f00fbcd2a85981ad3ec43bb92b0fa6`  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:06cb80319c09cac68ce0482c7b0e7306837b5fd54629f749f3ce46b768dbf22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6810323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58dbc38c39f44b0b1c18e447d7e6b090827dd8e48d2153a6ecec7225027f5beb`

```dockerfile
```

-	Layers:
	-	`sha256:5ed80b3e8cb1cd2054c92cdbddc7cb94435e7cd09c482629e6ce96db466d265b`  
		Last Modified: Fri, 20 Dec 2024 00:19:52 GMT  
		Size: 654.7 KB (654744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b29095b8b693f8759a81a95e0da251e810046c6e9558183f66aa10b6b0040b`  
		Last Modified: Fri, 20 Dec 2024 00:19:53 GMT  
		Size: 3.1 MB (3125246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a089e01847cf56f38c3757c7783a706916dfd0e52d186fedcdf719ed3f13207`  
		Last Modified: Fri, 20 Dec 2024 00:19:53 GMT  
		Size: 3.0 MB (2970427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e9fc7fc89ee246cd7656ec36768b8f803a3aedc61e5707ae39bbffd8ad54f72`  
		Last Modified: Fri, 20 Dec 2024 00:19:52 GMT  
		Size: 59.9 KB (59906 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:1c8d477ceff27620d259b6079016fe162dab9f33c926fdaa4ee03678cb2270d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66764635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03915d21274cc5702eb94daf0b5c95e4c5f61a681c35f45e09e3e2a3ce66ab2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e3a99aef2640ce207c9f308d5206d6e3ca989e9abd51f58ad3645764d95821`  
		Last Modified: Sat, 14 Dec 2024 01:49:03 GMT  
		Size: 36.1 MB (36102528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82de821cdbc35512b8f2c1255c8f4f64656454ab15159ff36d8cf7f4aaa2bd8c`  
		Last Modified: Sat, 14 Dec 2024 01:49:03 GMT  
		Size: 7.5 MB (7508430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ff993f646b00bc883ab6125009bdbacc49033662b2b42969a7373114affa9d`  
		Last Modified: Sat, 14 Dec 2024 01:49:03 GMT  
		Size: 1.3 MB (1323335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240aa07519f279976ad51d540f8b99a024ec98d9583bd6e4263fbad6978baa78`  
		Last Modified: Thu, 19 Dec 2024 22:36:30 GMT  
		Size: 18.4 MB (18359080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06bc2b802161b41ac78d00abc01f7d707737ef7c0b969e55782210a605a0b3f`  
		Last Modified: Thu, 19 Dec 2024 22:36:30 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7b2b9aaae28db8aa6213fa418e3d39078b47dd31137d8dd19d2e9f60c826d9`  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b63c4b4da289e1725652831f2cbb7fb18bcad9e084f7feb701974c5f874cd8`  
		Last Modified: Thu, 19 Dec 2024 22:36:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a875dd5faba2d9811cda01e92cfd0e0b728235ccd9d08e54adb0b68f9fbf32`  
		Last Modified: Thu, 19 Dec 2024 22:36:30 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:37580a0d0f1c2bf51088d1c7f513c11a209038c1fa4d245e389dfbf2e9d9f0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6512077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057661171bb26a5b5ce19cda2cb51a917e95752e3dc0ffbdc1fd25a7f4653216`

```dockerfile
```

-	Layers:
	-	`sha256:bcadc4c1d17aee27f426890765f63f76492764f29d77f7f7d5587129936d6a73`  
		Last Modified: Thu, 19 Dec 2024 22:36:30 GMT  
		Size: 651.9 KB (651918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27736675f322c11ce6bcc24aa2fb72f3488a396d3192210dbf9a3dd086a8fdc4`  
		Last Modified: Thu, 19 Dec 2024 22:36:30 GMT  
		Size: 3.0 MB (2977558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4192aa8523f3a59cd1c43c6439e19828b1957b86999f5afd7e31f4af055ac0e`  
		Last Modified: Thu, 19 Dec 2024 22:36:30 GMT  
		Size: 2.8 MB (2822757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559797edd8a425dec61a813c9ab8595753d5184173f9604e578e93ad4439ef45`  
		Last Modified: Thu, 19 Dec 2024 22:36:29 GMT  
		Size: 59.8 KB (59844 bytes)  
		MIME: application/vnd.in-toto+json
