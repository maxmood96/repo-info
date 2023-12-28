## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:94bb258b4f294eb80c85ac745219b1d8f0cb771d0c2c518b439be986a15f41d6
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
$ docker pull rabbitmq@sha256:85cfb96a5b63e52b0e845bcfbd615f7b5161ddc4fe6d717c273c8c9ec0d1d963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71017360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b35fff820218310a408b753c83c740f397697add1ea9b0ea40fc0758d363986`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Dec 2023 12:05:27 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_VERSION=3.12.11
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.11","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.11?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Dec 2023 12:05:27 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Dec 2023 12:05:27 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31e6620c95c38f14fd8e44d6bd4ce5baf007aebb15c9f9733a3f1563e53faa1`  
		Last Modified: Wed, 27 Dec 2023 22:00:03 GMT  
		Size: 39.9 MB (39897482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7309b4d89af9e44829768cefe0593ccefc27b546dafdaf43ee6c781768435f2`  
		Last Modified: Wed, 27 Dec 2023 22:00:01 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa469e313de72af2386283fecaeaf87f473a3b984fb78d05a4b1aec3d0cdfd2b`  
		Last Modified: Wed, 27 Dec 2023 22:00:02 GMT  
		Size: 7.6 MB (7554076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef35895329dc06c1afd6f5e90c8754b8b22e71decafe372d86dd5d1e91e7bd4`  
		Last Modified: Wed, 27 Dec 2023 22:00:01 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5862d67acb66f999a0ec2f2960819cc9fccc25773cf9ec62bb1239760dda13ce`  
		Last Modified: Wed, 27 Dec 2023 22:00:04 GMT  
		Size: 2.4 MB (2407909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fee1ee0ba30ae43d6da15263886376d54692857c66480e5a3bd667127b5a0e`  
		Last Modified: Wed, 27 Dec 2023 22:00:04 GMT  
		Size: 17.7 MB (17746879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2cb1adf49e9c45306a37e0db49da1b2fda87286cf1316b62e618751a703a64`  
		Last Modified: Wed, 27 Dec 2023 22:00:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726a02b078848ad7d81846192b8a5422944bc6d48341440bb781d452f17b65c6`  
		Last Modified: Wed, 27 Dec 2023 22:00:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71dcdf753e9775f9c85bb847d616741db34d0a3ad1caf91bcd92fe042601ee3`  
		Last Modified: Wed, 27 Dec 2023 22:00:05 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b462c61f3b1a8d639313b7f644bd1bd877cf78707461c8516c44c89a6bd0b0e`  
		Last Modified: Wed, 27 Dec 2023 22:00:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:37374b959170d2fa43c4a65aef7e2a85f86726252cace9f978790baf57e78671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b21da7619adf7721ee07c52b8c10b7e00f6fac55e518d68b46bd50ebbb6f12`

```dockerfile
```

-	Layers:
	-	`sha256:00642a009729c77bf7ffcfa65bdb7759f326c276f88abe15e1cbef30e53c8748`  
		Last Modified: Wed, 27 Dec 2023 22:00:02 GMT  
		Size: 760.7 KB (760731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1cff769d3c0d88b3060c2f1914e652dff67bb88bdf018b83102b3cb4edce1f5`  
		Last Modified: Wed, 27 Dec 2023 22:00:02 GMT  
		Size: 2.3 MB (2296534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8bcf4535c3e4bf01aeea7712bca7b0f2882252becc13c817d767072dce31b7`  
		Last Modified: Wed, 27 Dec 2023 22:00:02 GMT  
		Size: 2.3 MB (2295644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c36b0d6628118fc5faeee94177ebdc2004b6c779bfe3581f10ec818759398549`  
		Last Modified: Wed, 27 Dec 2023 22:00:01 GMT  
		Size: 69.3 KB (69277 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:a3dd8423d89ffd9233504967796ccf0df39f61ee3cbb88a70e2620d012133c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61114196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb0085904746c5bd14127a351e1aab173a38abd4c659842bf7a064a7e4ee651`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 18 Dec 2023 19:34:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_VERSION=3.12.10
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 18 Dec 2023 19:34:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 19:34:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 18 Dec 2023 19:34:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc08d73f9a4d73dd47cecaf45f755b0e88ea2c797d387a5105a62fa5eeb7bc3`  
		Last Modified: Tue, 19 Dec 2023 01:09:49 GMT  
		Size: 32.4 MB (32426935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d0ffffeabd24513832e80d6a238083897695f421a9381a9e0e4780ba8fc57a`  
		Last Modified: Tue, 19 Dec 2023 01:09:47 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5028c85a3955ca00cfa249ad5ad9df07ae8d2a7b2c659d6f431916c893050`  
		Last Modified: Tue, 19 Dec 2023 01:09:47 GMT  
		Size: 6.4 MB (6384110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e62a5dd115c90935ff8b32a506529a1085bb2aeaa0d0e51dbe542026934bbaa`  
		Last Modified: Tue, 19 Dec 2023 01:09:47 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b339d2f0ee461d71095a2548176fbd10b91dd0d91978867e5e5420e09963ab`  
		Last Modified: Tue, 19 Dec 2023 01:09:49 GMT  
		Size: 1.4 MB (1403271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0cdc3348fe1601843e7d5a78cce60ad0cb822df0a675953288b67bf420eeae`  
		Last Modified: Tue, 19 Dec 2023 01:09:49 GMT  
		Size: 17.7 MB (17732214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125ee97b40ce5e3038ecb9cca386dafca66c0d79f733183061357bbd08362cf`  
		Last Modified: Tue, 19 Dec 2023 01:09:48 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be2690a3387df70b8898e76254d61f1c5a0bda49f86209f7948d2d862748c44`  
		Last Modified: Tue, 19 Dec 2023 01:09:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfc5e85825301e55c3024492d1fb46dfda100ffedf7da4ccbe07e0b223a3147`  
		Last Modified: Tue, 19 Dec 2023 01:09:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603a5dba64bdcee1b0c8fdc10c5bd262e059dae5b3b65eeba2ca83460e90828a`  
		Last Modified: Tue, 19 Dec 2023 01:09:51 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:36d3bf2e33aededf59bc9ec130f331321b20ffde217055796c35de52dd13d3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 KB (69275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb677bc5c6543bed0d01d20db6c977f770d2c70ef4624537fc3912788dff80f`

```dockerfile
```

-	Layers:
	-	`sha256:b313fbc70c18f6fa59fb3405f902cde8e3f50d36a1bfbe423320547b0f948991`  
		Last Modified: Tue, 19 Dec 2023 01:09:47 GMT  
		Size: 69.3 KB (69275 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:57944bebf2612ea373855881ef97454200c434cba61feb256820f747f47b258d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60382353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c131ada8b52046cdc2c056775987a778e451cc5b047e4ca0735981a31f4778e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 18 Dec 2023 19:34:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_VERSION=3.12.10
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 18 Dec 2023 19:34:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 18 Dec 2023 19:34:09 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 18 Dec 2023 19:34:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 18 Dec 2023 19:34:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 19:34:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 19:34:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 18 Dec 2023 19:34:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2392e2c9d27e86124ca7e8e6a0f8e6ae052123d885444509a1fac73ce0fa7f08`  
		Last Modified: Tue, 19 Dec 2023 01:26:18 GMT  
		Size: 32.3 MB (32336634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d31b1b1875ee7752972c089ac2a1990838ee6b4c04981fa600d1c32c4fa74d`  
		Last Modified: Tue, 19 Dec 2023 01:26:16 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f06f5129e16dbc73acb1254dd9c908107b7dc088d0dd307bcc182e64da6d19d`  
		Last Modified: Tue, 19 Dec 2023 01:26:17 GMT  
		Size: 6.1 MB (6084850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd949a9b4bc330156c73ab7ee9f7affe6fa421db97c0d064d0b4f28624a253e5`  
		Last Modified: Tue, 19 Dec 2023 01:26:16 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c53431e47c14b95636fbeb22d913d94ece94cd5a6dbb12269ceaec34e78b657`  
		Last Modified: Tue, 19 Dec 2023 01:26:18 GMT  
		Size: 1.3 MB (1307590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1f254e3c540587164eeac9c6deaa02ba99c2444339c524a80ea91b5e14b636`  
		Last Modified: Tue, 19 Dec 2023 01:26:18 GMT  
		Size: 17.7 MB (17732054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a63a98dc08abad2d8577e491c7f7a986e84d374f2883a4a586cf340d3ac492`  
		Last Modified: Tue, 19 Dec 2023 01:26:18 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7577105ca4b9c5297234ea1662246a70054503d07198120aae754339f2c9be15`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c8c0c9b495576102e010ae82b7cfd484472171504ed879e297ff5a81f6c892`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799530acf872fb92bd486f47aef9bb0e6b0fb90d1a75664b92e9ef51dfc973a2`  
		Last Modified: Tue, 19 Dec 2023 01:26:20 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d6e771f3c738aaae133527860239cf8e5bc1acc48d8a3fdbdd84141c90cf7420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee60f061b27a8ec1bcc1059c889317d5384706adadbc89fd3d699bbd47500ce9`

```dockerfile
```

-	Layers:
	-	`sha256:ab6925600b6cc66bdd91757bc8903e9ff51e080b19555d480d725792706d81a2`  
		Last Modified: Tue, 19 Dec 2023 01:26:17 GMT  
		Size: 756.7 KB (756709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2aceb894be17569bdfdc31657a9b9a09b250a5b4f134b1da037f9b8bbadf1c7`  
		Last Modified: Tue, 19 Dec 2023 01:26:17 GMT  
		Size: 2.2 MB (2215090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:defa283335e9b1dd208759dd755dc39ffb464b7e2bc9f620a67ac68fa70a7e24`  
		Last Modified: Tue, 19 Dec 2023 01:26:17 GMT  
		Size: 2.2 MB (2214200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220db2bc4e80d85e2f8048cddd69602fd8f6753644a7c1b7b540596ddaa0273c`  
		Last Modified: Tue, 19 Dec 2023 01:26:16 GMT  
		Size: 69.5 KB (69489 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:b730733e856975bca6c771d927b28376857039140be817300e52e42079cb65ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68683608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99f9980469a92c9d847601519e1a52241e648ace4964c3787d9b45b45281780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Dec 2023 12:05:27 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_VERSION=3.12.11
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.11","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.11?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Dec 2023 12:05:27 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Dec 2023 12:05:27 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3f6c6b83152805eb2e5113d6eb35b1475c7cd6bd414ae39919369ea34e0ea6`  
		Last Modified: Tue, 19 Dec 2023 01:20:06 GMT  
		Size: 37.9 MB (37914616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca704a5a588c3767cf6f69498f4c9e85a976ec5bfdda313b9050bb1833bdb147`  
		Last Modified: Tue, 19 Dec 2023 01:20:05 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b89a80bec3b69ea5002a141e2c4fc630b976ffbdb45ee29851eb2fc1d42c3`  
		Last Modified: Tue, 19 Dec 2023 01:20:05 GMT  
		Size: 7.2 MB (7180445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568af80e8a6742fd91184ce4ad0e61d63f8b6f8192b2b4705a0d36f03c47c32c`  
		Last Modified: Tue, 19 Dec 2023 01:20:05 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67066722dee8291e4296eef6b885d1a22003c86a74397dca6fd3333b804423af`  
		Last Modified: Tue, 19 Dec 2023 01:20:06 GMT  
		Size: 2.5 MB (2491581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61b901405da28b31370eea34fa6602de6e838d30920b72426424e44e95c4573`  
		Last Modified: Thu, 28 Dec 2023 05:17:58 GMT  
		Size: 17.7 MB (17746648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c03336e95c1ae9f89cffa8bf2694b869057be9896d17e4bbdcdf0f85db6ec7`  
		Last Modified: Thu, 28 Dec 2023 05:17:57 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961ade427640b7a64630f5ef00198d22359419028aa7d5134c63ffd431edf3b1`  
		Last Modified: Thu, 28 Dec 2023 05:17:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17db03816d0fed08dd64a00643261374109d1e7450efbaecb984a56fdcaaf525`  
		Last Modified: Thu, 28 Dec 2023 05:17:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24980fb35644ce5071055a49308050cafe2cd6a8bd9efd7c1bcca3ab2abe8da8`  
		Last Modified: Thu, 28 Dec 2023 05:17:58 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6d552696d7d111d53c64c09a9556152d2dd3b172c8adff06de8f25e6b2479369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f00ac76e4ca694bfca73a77155b5c533e04ec8f9b6e65034a7dfa336154577`

```dockerfile
```

-	Layers:
	-	`sha256:51843b9cf6a3aea68a16f60f74030d52d9ed2dd83efa2acf6247ee3bda184a2b`  
		Last Modified: Thu, 28 Dec 2023 05:17:57 GMT  
		Size: 760.7 KB (760742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50df6db958ec03994c37364dfc92c565510a5fd4c1fe151c2c5546353dfb4685`  
		Last Modified: Thu, 28 Dec 2023 05:17:57 GMT  
		Size: 2.3 MB (2309980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb06a87a66e07e4d136adf86becaf3928531e6a58a98401077a02e921cd3d25d`  
		Last Modified: Thu, 28 Dec 2023 05:17:57 GMT  
		Size: 2.3 MB (2309090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28415adea5832901569c1d2d40bee4b96ecfbd631054a03616a287722a852563`  
		Last Modified: Thu, 28 Dec 2023 05:17:57 GMT  
		Size: 69.1 KB (69121 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:f4da199440249a1196592c2633fe19ba1d6cc7ec0e9c33c852c1012d10693ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62493210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a439ad80fe22bbf42fb9e37a51801cea086f8dc84f17c480399cba353fb080c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Dec 2023 12:05:27 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_VERSION=3.12.11
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.11","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.11?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Dec 2023 12:05:27 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Dec 2023 12:05:27 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9d914949c2cf59dc1292338ca975ce3e56b8e7905509a7d2dcac33a14bfd45`  
		Last Modified: Wed, 27 Dec 2023 21:59:26 GMT  
		Size: 32.6 MB (32612669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da94a11163a1bda694cfc6df9b49a4d7889cfb1622be36bd359509a476d80940`  
		Last Modified: Wed, 27 Dec 2023 21:59:25 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ff85ff447b70726bac3b1ab04408184622392d5490f5c9a08f91c0343a9286`  
		Last Modified: Wed, 27 Dec 2023 21:59:25 GMT  
		Size: 7.5 MB (7481065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c64323e89a33a196e0b769ed7423c601d3be986e7f5695ba50b7b3f5b2e93`  
		Last Modified: Wed, 27 Dec 2023 21:59:25 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a07f1f368c7ea4e12dab9a62c47d856ca915fbde08ca3fd1f7ebfeea4a2c837`  
		Last Modified: Wed, 27 Dec 2023 21:59:26 GMT  
		Size: 1.4 MB (1406646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fdc8ffd528f579660a96f65b91d7a4cba1fccb1dd62cec44ac379508b1708c`  
		Last Modified: Wed, 27 Dec 2023 21:59:26 GMT  
		Size: 17.7 MB (17746191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea33d1b02bd27a70fa05525fff6abfd62006fcbc2b79f3124d52ae20f8c3904`  
		Last Modified: Wed, 27 Dec 2023 21:59:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886985cc1a35b0530de849e7184dcf932a50310783d5d9ccab6face1ba2333f`  
		Last Modified: Wed, 27 Dec 2023 21:59:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cec37ee4e75d3db0b2b3e55838c0ea5c6cc1f91af9390a48507d5fbeaa198e`  
		Last Modified: Wed, 27 Dec 2023 21:59:27 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206fb33c6859f25d4f802a4f17c54e8f8f4f529f56b5c7c7fd86c9b9ca865d39`  
		Last Modified: Wed, 27 Dec 2023 21:59:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:717a3f19479ce5922c1d5cce17db6890bf57704c5954f814bdaac9778aaaa437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5401678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4668822b0b33f69b3690b0427cb620b535a6d71dfd390923f9025dfff2cc4104`

```dockerfile
```

-	Layers:
	-	`sha256:58605696fc19dda09d871993b863922921ed10b4012283a99fa17baa76b29661`  
		Last Modified: Wed, 27 Dec 2023 21:59:25 GMT  
		Size: 756.6 KB (756648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ba8b79894408f2d51ecc313e13baab0ed3afbab42dcd65e1a90061ac7adb64`  
		Last Modified: Wed, 27 Dec 2023 21:59:25 GMT  
		Size: 2.3 MB (2288348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eb89a4a276e2d2fe4748c10d07048773136a915c19ae8e2dc7c8616309cff20`  
		Last Modified: Wed, 27 Dec 2023 21:59:25 GMT  
		Size: 2.3 MB (2287458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1a04c1be6cdd8ca79cbbcc754403152e1af8d46e2cafb9a09025e69e7a026e5`  
		Last Modified: Wed, 27 Dec 2023 21:59:25 GMT  
		Size: 69.2 KB (69224 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:5b7deed1108850ed6cc62e3a2160095ba506b7d66888071cf08d43b7f62b7238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63420950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bf1f4ab439b57222e45335ec1854897cf9036376a4d611d37fd39153600c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Dec 2023 12:05:27 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_VERSION=3.12.11
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.11","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.11?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Dec 2023 12:05:27 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Dec 2023 12:05:27 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e18033781df51e3a28370871ffe433ee3c517e63d80002f10780a329d62897d`  
		Last Modified: Tue, 19 Dec 2023 01:19:06 GMT  
		Size: 32.8 MB (32829753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee5a9a206848b8435df614c1a9656e406c359fc8ac8376e4a8bc94c9af4a0ed`  
		Last Modified: Tue, 19 Dec 2023 01:19:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e2d79d5d6d4f38ded59ba485831dd4f4481b9410ec6292125ff803ab0bfd00`  
		Last Modified: Tue, 19 Dec 2023 01:19:06 GMT  
		Size: 8.0 MB (7967022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2b74c9fb3275044cc54e33ab263b71c298a38d41b07e7b5a83ed932e446fdc`  
		Last Modified: Tue, 19 Dec 2023 01:19:05 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef336b46c5c7e058ac6048ad1763b4a7f56213bf84e57c6c6dc46b0b97f5e1d`  
		Last Modified: Tue, 19 Dec 2023 01:19:07 GMT  
		Size: 1.5 MB (1517323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaaebe38f863ede3de69d647c6407c4250c0318dc2539617e25aa7bc1c278e1`  
		Last Modified: Wed, 27 Dec 2023 22:27:32 GMT  
		Size: 17.7 MB (17746081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60afae68ac0900145c46b4839053f80938453ffd02e03a5b9aec49fca9eba720`  
		Last Modified: Wed, 27 Dec 2023 22:27:31 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1b6b2b475fead8ae3b53e7bc2f5ef4196e9fef0ee7d6c8fbf6eb582fb38811`  
		Last Modified: Wed, 27 Dec 2023 22:27:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17239bb61eeee154cdbeceeccc196140f24407fd2d4fa0ee4dc9eaa066ffed0c`  
		Last Modified: Wed, 27 Dec 2023 22:27:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb293b1a6c61a05a82e661fed6e7ab15c9364561e0612b175327d699008adf`  
		Last Modified: Wed, 27 Dec 2023 22:27:32 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e573b26881e079194177d954c24afd58ae5d6288b0dfb63abec22cb107cd508c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72319375db19b556ae78c13c06c34446e2c906f3a3d8b2da969df0b92e2aa4b7`

```dockerfile
```

-	Layers:
	-	`sha256:5843388868f9f6b398d656f8da5193d24fef41939cbc1216b7b56f69341f4daf`  
		Last Modified: Wed, 27 Dec 2023 22:27:31 GMT  
		Size: 755.1 KB (755071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4ee5aa023f3cf4604b12502b28e2e665f5a3ab1f5bea378d579b9d8e0397450`  
		Last Modified: Wed, 27 Dec 2023 22:27:31 GMT  
		Size: 2.3 MB (2287999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae55bd0e08b584e77f9941c06b220937de812133773b8bc9458e16d5bae3b58`  
		Last Modified: Wed, 27 Dec 2023 22:27:31 GMT  
		Size: 2.3 MB (2287109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb25ea544c46c3c3d1a36d433564f22718aa3b595f6c46736769ccefb063406`  
		Last Modified: Wed, 27 Dec 2023 22:27:31 GMT  
		Size: 69.2 KB (69171 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:5873e9cbccc89b0d184b59f8c43a5c441f806cc1ba215e62326a99e73d047f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62105297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee70335aaece7c074ea93f83b48b5683efb77f19662fe83b0dbaecb73a640b3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Dec 2023 12:05:27 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_VERSION=3.12.11
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Dec 2023 12:05:27 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 12:05:27 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.11","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.11?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Dec 2023 12:05:27 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Dec 2023 12:05:27 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Dec 2023 12:05:27 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 12:05:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 12:05:27 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Dec 2023 12:05:27 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bab8234efa28a5ccfce9900554b077de591980001319c90390fb819b20f4d2`  
		Last Modified: Tue, 19 Dec 2023 01:18:19 GMT  
		Size: 32.9 MB (32919466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aec38dd8d2c55f0f0080cd935b4310f66cf0c3349f086a43755025dc7fdfb2`  
		Last Modified: Tue, 19 Dec 2023 01:18:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e15625661b90cb4afdcd50046b0bcad43c979843e122cfcac13d3ba813c27e`  
		Last Modified: Tue, 19 Dec 2023 01:18:18 GMT  
		Size: 6.7 MB (6696961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa90cb02b56a7344049c65e2b68b2b90aec741d3e6754b1019b8ec4f57eb1590`  
		Last Modified: Tue, 19 Dec 2023 01:18:19 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320b826531725b3ea40023906d3b5490a123bdd16b32146a0669fd70af58fdfd`  
		Last Modified: Tue, 19 Dec 2023 01:18:19 GMT  
		Size: 1.5 MB (1498160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29d2f5da2629e8cbffb9a10b4d1023442560343779ff26178c20ece7329c77f`  
		Last Modified: Thu, 28 Dec 2023 01:48:32 GMT  
		Size: 17.7 MB (17745842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3026cddab63835eecff7fa5b64ad6bb7f124c42ed54d0656a505071814b034f`  
		Last Modified: Thu, 28 Dec 2023 01:48:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6173cec4dd633004df3985b470768b53652930b9aefed78762e8bea69f282e`  
		Last Modified: Thu, 28 Dec 2023 01:48:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1cd6fad65981dd95fd9bb7e4c91b35f1a07f5c0078020c0a64e83f1188c41a`  
		Last Modified: Thu, 28 Dec 2023 01:48:31 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5818869fcfa1d46c5b4bbbd811e04539ae41fb4e341356f5ef9a069ce7fc4d`  
		Last Modified: Thu, 28 Dec 2023 01:48:32 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:80b7529536eac3d8278fd1a4c4ef17a972edbcaf78507fcc113df1800da394c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bac18965162627f7e36ab948ec97f5c5fd94cc725c1bfa95d24cffaab2b0f8c`

```dockerfile
```

-	Layers:
	-	`sha256:ce5440291f3d2bb425ffde8529e7ba81c5f66e18ae76a9ee94083f81c3e4c4f6`  
		Last Modified: Thu, 28 Dec 2023 01:48:31 GMT  
		Size: 755.0 KB (755037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619611d118c7c337b171d3d9b9377570fa57cea5a5b24c71e0c062e73ce44590`  
		Last Modified: Thu, 28 Dec 2023 01:48:31 GMT  
		Size: 2.2 MB (2220034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a964f19def441c4c92f984ff468879bf6ab8ab4a713447dc15663936fa091c3c`  
		Last Modified: Thu, 28 Dec 2023 01:48:31 GMT  
		Size: 2.2 MB (2219144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027ce3ab54853d433cc29f9a564887d6d65524117bc7be80cc1c8eab565fbea7`  
		Last Modified: Thu, 28 Dec 2023 01:48:31 GMT  
		Size: 69.1 KB (69110 bytes)  
		MIME: application/vnd.in-toto+json
