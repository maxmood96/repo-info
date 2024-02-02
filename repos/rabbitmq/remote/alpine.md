## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:cca2b06494c262e8fc1448087d3ef91968881f4dcb270a9da55e572b4d2e53cd
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

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:6f1a0ba45120f3eacc601d5c7077ce7e3ee24d16bd22e7dfec70078b007cf996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71031671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5c88804d92b2150b93b7bc6f570521cacf787e23ca2e924dff807904324c3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 30 Jan 2024 18:57:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_VERSION=3.12.12
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jan 2024 18:57:54 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 30 Jan 2024 18:57:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3fddea8cbf8d0039ec2b7ea577a3f845c95c936b6abebd3e13453488a9f6d8`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 39.9 MB (39897481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87904c1c30f73828f44552e5e853914eecae59ed2b5f85f718b1aba1c7f1146e`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856916e86e80c3a80455b51f68a09579099ac1e1dd21bb2154074075b81dc41`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 7.6 MB (7567780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d9d4619e5314a56fce3d850d3c47a7451c0f781652d7ad0a6e268bbc9e75cd`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c278258231657a965a66098523956cb8942c2320cec113319ae19f1ff9de35fe`  
		Last Modified: Thu, 01 Feb 2024 19:04:26 GMT  
		Size: 2.4 MB (2407915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093b0a1a17d7bb000107b414059b248366079c11394da24a51d79f4f86c225b4`  
		Last Modified: Thu, 01 Feb 2024 19:04:26 GMT  
		Size: 17.7 MB (17747240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a8d7c9658d666c0728e596ca45a6d41953399a4b21300ea5e222dc8eeefeb`  
		Last Modified: Thu, 01 Feb 2024 19:04:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986c4207d6db97b12c81ce7125c94181bb106a0228ecf7c0ad328114efa5b86f`  
		Last Modified: Thu, 01 Feb 2024 19:04:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf42a611102787f0ac7a1354926d0fa46025953b44190f17f4f22edc15f87d83`  
		Last Modified: Thu, 01 Feb 2024 19:04:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028c0985fff990d37d8b37f79beed749355cadee4542fdce40fea12c508f642a`  
		Last Modified: Thu, 01 Feb 2024 19:04:27 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b16b28435c038e0717f073fbe8c8b812915f29eb5b25e6b85f930a00d4be2d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37ca3411df95737526c2a69fc5524a542d3165590f0d387fcf1ae0a8419e44a`

```dockerfile
```

-	Layers:
	-	`sha256:4b60dfc3de0f7a56606b856cb0a37d89a6775f09117dad782321cd3e3b7e8a76`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 761.7 KB (761682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96682a40827e12629ef84026005edfe15de1bc4ab32853b5f2f3065d33487691`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 2.3 MB (2297904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0ba9bfc950532a78d73931a10cfa34bdf18f6d165ba1e0338093bc4e425ef2`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 2.3 MB (2297014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df45a8db11754e2a6d876a78381a43f7195e268480e1e4e021ad0e4e52ab6d6`  
		Last Modified: Thu, 01 Feb 2024 19:04:25 GMT  
		Size: 69.3 KB (69277 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:da0df2cc7887250fb4bb585dd64793ca2828373a85645b477ee094b0563fc183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61146731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03036fc73173954f6398058080b411e2a11aa30cdab8929113ee2d94ad2aae14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 30 Jan 2024 18:57:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_VERSION=3.12.12
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jan 2024 18:57:54 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 30 Jan 2024 18:57:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff26be4bf0ae00cae062d3c1e5ccc8e94e0acdaae952ee10863cfe699c2cfcf`  
		Last Modified: Thu, 01 Feb 2024 19:18:28 GMT  
		Size: 32.4 MB (32427017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d45b266fffa28354a7eafd941613665fad6b110e731276b7c4a0406279a7e78`  
		Last Modified: Thu, 01 Feb 2024 19:18:27 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb727a49f515121ddd9f0fa5ff2964cc5763ff04e08d507952ecf45e86951349`  
		Last Modified: Thu, 01 Feb 2024 19:18:28 GMT  
		Size: 6.4 MB (6400965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540a650fe488a617c865f8a0cd1b5edb5a970113a36db6d33a0caad7ca191a74`  
		Last Modified: Thu, 01 Feb 2024 19:18:27 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec7d8c72ad88109f038a6d66da573e1fde1d66ddb5d179ba7d86220278df0db`  
		Last Modified: Thu, 01 Feb 2024 19:18:28 GMT  
		Size: 1.4 MB (1403703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f55e7658aef99011d22d95f4853073b5a1cf68a4a289462667e501dc0c7cd8a`  
		Last Modified: Thu, 01 Feb 2024 19:18:30 GMT  
		Size: 17.7 MB (17747124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b993db0e550f9204dbaab7df6df77a166030cdcc09bbe56d3764714be9cb28`  
		Last Modified: Thu, 01 Feb 2024 19:18:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe7d926f8463ad6e64ea5204a7e3df0da3fac59a8f93a4af6fa06c1936d0d61`  
		Last Modified: Thu, 01 Feb 2024 19:18:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349701b6a216466b474d9a95ae560264dffe6853e322653445c3d5cc984f5cce`  
		Last Modified: Thu, 01 Feb 2024 19:18:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681e56aa533feb696611ae5b527f3e0cbd7b190fb7c8e351b5dce942abe25234`  
		Last Modified: Thu, 01 Feb 2024 19:18:30 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f05acc5f0d052d32459d6c62268af660d7d0b5c515b62f268fc75b57d730036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 KB (69275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8dc88eec78d13b9d24bc335493ce7a0c4c7c65cd9678c2915a96ada6c1f835`

```dockerfile
```

-	Layers:
	-	`sha256:be99b525e2b9e56391ced61a12666e43b365a48e09882c3b1011a969b7bbc7e8`  
		Last Modified: Thu, 01 Feb 2024 19:18:27 GMT  
		Size: 69.3 KB (69275 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:72832fb9b3afaea025ed462bfbc906f7bdd0b33d1ea56fb043ac8f3c09be067f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60412576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736bdbb80d397540f086952d87dc1fdf8dafa53a5e4b24749919ee62982f9b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 30 Jan 2024 18:57:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_VERSION=3.12.12
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jan 2024 18:57:54 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 30 Jan 2024 18:57:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9225f595343f45321f44479c7a9258eff26ac101b1f86d95539c9b7d38487f8`  
		Last Modified: Fri, 02 Feb 2024 09:49:09 GMT  
		Size: 32.3 MB (32336933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb964044625e07a36d0318501ca2d523e34167d2e868ec844a29b657cc03a201`  
		Last Modified: Fri, 02 Feb 2024 09:49:08 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98f7544180859eb674fdf173f5d8053feb57f0e022b40c7aaa914d00bff0301`  
		Last Modified: Fri, 02 Feb 2024 09:49:09 GMT  
		Size: 6.1 MB (6099273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739914bff9996a07fc73d2f578fb6e805759c8f66d69d89fb3f9f0e6c677414a`  
		Last Modified: Fri, 02 Feb 2024 09:49:09 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6729d20e3046f92f64c303f5bd4013b8cc80359cefb869ed1c9733afae1a11f3`  
		Last Modified: Fri, 02 Feb 2024 09:49:09 GMT  
		Size: 1.3 MB (1308048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e85f1325a4f68bc58c0e5b56208dc759ec62b9d93f36f27cf6806aaf3c2f3e9`  
		Last Modified: Fri, 02 Feb 2024 09:49:10 GMT  
		Size: 17.7 MB (17746892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3978f17b7644190d01adb433c802827486613fe34b30564d7111aa4b99ed4b`  
		Last Modified: Fri, 02 Feb 2024 09:49:10 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b00fb46432f1d1e1ef9203da6b407640a87bbf42dbc4669f0778154de9bb7`  
		Last Modified: Fri, 02 Feb 2024 09:49:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0b86c77458cba042e3fd41bf5146459e312230ed952eeee3e2ed6faf6432bb`  
		Last Modified: Fri, 02 Feb 2024 09:49:11 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b846637d29d7c8663f65f975c5df5ee87d910772c49d91703a1125704030a2`  
		Last Modified: Fri, 02 Feb 2024 09:49:11 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0232ee7fa23e44315c6f7241c9827440a63c98b09b98c32d6519163ec6f17474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261b056694b8a22b769aabd2407b9a26cbee7c57a5fa3814cd01c4f4f8fef782`

```dockerfile
```

-	Layers:
	-	`sha256:9ee369bf8b40437a24841c2cd58f39f9bc3338773e46e8db5cb4eb9606e4b4fa`  
		Last Modified: Fri, 02 Feb 2024 09:49:09 GMT  
		Size: 757.7 KB (757660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b92f05b4b1091faf82b76dbfd476d42e60e709dfda024dfaabe22ef44f46a10b`  
		Last Modified: Fri, 02 Feb 2024 09:49:08 GMT  
		Size: 2.2 MB (2216460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad9f30dafdda0a5073d487de92c84580f986e0851703b7b9b8f204959282ffb`  
		Last Modified: Fri, 02 Feb 2024 09:49:08 GMT  
		Size: 2.2 MB (2215570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:254f9853c5c14fd9928c84aea4eedbb8b936973d933a39f94022e91c4ea302f1`  
		Last Modified: Fri, 02 Feb 2024 09:49:08 GMT  
		Size: 69.5 KB (69490 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:2f9fcd514c95d3fb0c104eb4f9efb45b7fc9c302ea371a57fab53e8d6c6d6249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68691604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eeb081a48951536cc398a2b4bbec5e3c62f3e373f17ae05a2bdc296039084bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 30 Jan 2024 18:57:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_VERSION=3.12.12
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jan 2024 18:57:54 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 30 Jan 2024 18:57:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4fe0abe408e1518f9d5b17c3282b529a5b5ea981f2d8caa3a241204af6ada1`  
		Last Modified: Fri, 02 Feb 2024 18:25:29 GMT  
		Size: 37.9 MB (37914672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfae2bd54586df2e84e8a2cabe7b8e4dbf5d56771da6b185ca1de4795460b785`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b6347a3feb55b3e86c48d91f9615d3363a8e4b1affb0288e16dbf60a7bedc`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 7.2 MB (7189426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4251bd180856830ac9aca33b1d5c2af63839637ff081ebfb94d3d0b88da7b191`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eddc4aa204eee2adbabd308a49377fbfd78ed341a8002071cc8c3aa9d9c8e65`  
		Last Modified: Fri, 02 Feb 2024 18:25:29 GMT  
		Size: 2.5 MB (2489853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7d1598a3044dea21013914315fbba79a4e3b53d7690bf82a0a38f9f8690273`  
		Last Modified: Fri, 02 Feb 2024 18:25:30 GMT  
		Size: 17.7 MB (17747412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0988a9ba40162cf895f49fe14834dfe4734e70f486202f2ebec6982fd5e4c783`  
		Last Modified: Fri, 02 Feb 2024 18:25:30 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5451a31bb41ad7aab56109cf87a2120ba12ed8ae271ed0563c37936b859eb60d`  
		Last Modified: Fri, 02 Feb 2024 18:25:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f967db87b3560b8cdf30f3b3602840ec03fb5616a606394cae281730397f8bf`  
		Last Modified: Fri, 02 Feb 2024 18:25:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11d8755d99afa392c03184118d9ccd54061c848d3fa4cdd29e68ada2d503bbf`  
		Last Modified: Fri, 02 Feb 2024 18:25:31 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b6cadc747db97df29a8fba4800d5cc61634721bfc8d6a4ba8211769b04d5ffd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd6246f12fa9a754c45024fbe1a1cf5a07a9fd70426b7d2d7d859714aa217dd`

```dockerfile
```

-	Layers:
	-	`sha256:c54ec8c4853f06eb33ce3ad28dd065a90c15a7c64cbab7137f1d0f1f11099e06`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 761.7 KB (761693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4faa20ec72e22b86379d9a9d28660571081c68bd8518942cb67d0ebf742f3bfe`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 2.3 MB (2311350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80127f4072fe5454af3895b0ccca2cbfefb53b9494093cf5150d2c8aa63435b9`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 2.3 MB (2310460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f2abaff7cd2eec8a009319800c29a22254947b1b9d2a0052d1b4dd31b180be`  
		Last Modified: Fri, 02 Feb 2024 18:25:28 GMT  
		Size: 69.3 KB (69287 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:94f4402c573023bfa17c9021fb69602ba98bb6a6ea03f7ea3a62569925397f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62506530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7a61d22dafffbe46bc4063775b36b0c488a50e64eb65c2b1008a35f5d64189`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 30 Jan 2024 18:57:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.5","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_VERSION=3.12.12
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 Jan 2024 18:57:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jan 2024 18:57:54 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 Jan 2024 18:57:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 Jan 2024 18:57:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jan 2024 18:57:54 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 18:57:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 18:57:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 30 Jan 2024 18:57:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deb0d916d940ff67aa8c7e14831de6850ca4ec8f7d55d567a7a62278624b4f2`  
		Last Modified: Thu, 01 Feb 2024 19:03:58 GMT  
		Size: 32.6 MB (32612514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede568fbc99834c8ec9720843e00d1b2d3b8e6761e0a9bfad009ab0f96c81b64`  
		Last Modified: Thu, 01 Feb 2024 19:03:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abfcf725c88cb4028c0e505275a4c27690f78a906ea941682a99422ae4788a7`  
		Last Modified: Thu, 01 Feb 2024 19:03:57 GMT  
		Size: 7.5 MB (7493817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b703c8a37d15905b7aeac4f9aa3f933947b1d99dd070389d215ceed1e9809a`  
		Last Modified: Thu, 01 Feb 2024 19:03:57 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680cd2bc0842851124966c93d2eaec652e2f703ebcda58725d862ada9e7289b`  
		Last Modified: Thu, 01 Feb 2024 19:03:58 GMT  
		Size: 1.4 MB (1406670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eea14220dfc56a87670c9c53e7c6792f1ce3929e971bd1aab4d702adbd2e38`  
		Last Modified: Thu, 01 Feb 2024 19:03:59 GMT  
		Size: 17.7 MB (17746908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875fb2532c17b5e8acdcf27f0906526e97fc5913703f609ed809e36491b106e9`  
		Last Modified: Thu, 01 Feb 2024 19:03:59 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb3311456f41e30a2aaa8f77457b007b14e1aabaabd28c10ee4ea3422d6ce27`  
		Last Modified: Thu, 01 Feb 2024 19:03:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8f4a2f19f77a04b9703208eebe66fbd8ea655f0978936bd7c129146d8f8bcc`  
		Last Modified: Thu, 01 Feb 2024 19:04:00 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4489ab2d6f972039a832fbe16faaa0f4c8406ac213232bb295a506fa17ec6615`  
		Last Modified: Thu, 01 Feb 2024 19:04:00 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fac04dc5ea46c440af83d7436d9a3e68816ac83fc5548be738ea1f197f5e24ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5405371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b8712748fe5a5c6e227f38ac555b06d9de646deb8a552d753ea3fe44362a8e`

```dockerfile
```

-	Layers:
	-	`sha256:d2c15cbc61c5fdc799c33f0e2477ecbbaf5a90de0ff6e2b4ba840ebc8b36178c`  
		Last Modified: Thu, 01 Feb 2024 19:03:57 GMT  
		Size: 757.6 KB (757599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6971bb831a83df72436a14ed12ad02103543351e89b2d97b18b07635166f2794`  
		Last Modified: Thu, 01 Feb 2024 19:03:57 GMT  
		Size: 2.3 MB (2289718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b0a5436c281214971bcc78d12ba8aab58f121c91fc134edbe3bebe4c3aea572`  
		Last Modified: Thu, 01 Feb 2024 19:03:57 GMT  
		Size: 2.3 MB (2288828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d3ab90601e1c3c73f0e5e9972d9542d67e1a682a65963a1d2eecde432788a4`  
		Last Modified: Thu, 01 Feb 2024 19:03:57 GMT  
		Size: 69.2 KB (69226 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:ddb2f18d3b6eaa626629266a3f4e7d225c4e9623bde913bea2cda9bece6eb1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63422157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b253f493a9fce7a560017fb09615acb2af6fecb5ea12638520c35a9d1980c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 05 Jan 2024 21:27:24 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd166d066658e783452d8d56f4ec6a6d1a944e9a18ebfb18d519ee256d552939`  
		Last Modified: Sat, 27 Jan 2024 10:49:57 GMT  
		Size: 32.8 MB (32829760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e864e815722f30376bd746efa9ad350944e7eea3a74b848dca414051b50678`  
		Last Modified: Sat, 27 Jan 2024 10:49:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5388ba3eb362e8c3f00adf3c0465f6949dff40692a508185df472e0742a90`  
		Last Modified: Sat, 27 Jan 2024 10:49:56 GMT  
		Size: 8.0 MB (7967040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f87f6f4d148b930e114ccc09b2d223f9fce768a959ecee5c8ecc19541a2b32f`  
		Last Modified: Sat, 27 Jan 2024 10:49:55 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d265d5c5f15c200019bdceba79c39ed75f8e468e48c55b94a5eb5f6b53332c`  
		Last Modified: Sat, 27 Jan 2024 10:49:57 GMT  
		Size: 1.5 MB (1517734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8a812f43ad769b7e28077b4de3ea7a79d877231c46077397d95864728baa2`  
		Last Modified: Sat, 27 Jan 2024 10:49:57 GMT  
		Size: 17.7 MB (17746730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc5250ac6ef5989c94fd7f2c509d259654a3281dd4a85e8c33a0a44beb7740a`  
		Last Modified: Sat, 27 Jan 2024 10:49:58 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d7d5131021925c6eb237fa2e9a84227af0ab68334657ba7e1103465e7860f0`  
		Last Modified: Sat, 27 Jan 2024 10:49:58 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91099d23c78eadfb126bd06ee64ef24d1c569d0c78c056347941a2e8a249d48`  
		Last Modified: Sat, 27 Jan 2024 10:49:58 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f33064fb1d35fd117ac12d25ea9757b9b7b8352060493cffe17ceaec1883c39`  
		Last Modified: Sat, 27 Jan 2024 10:49:59 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b3e654918b95f655a2c16f07aff96383bf9d6e11286346b43b30e3fa6e3cd751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec65996de5dc3ebfaa3084984206897e0d4dd32a2995533f60ee92f8f152fbc`

```dockerfile
```

-	Layers:
	-	`sha256:9c000cfd55333ba44b9cfe646997090ef88a82b64ca5222409782af225182fff`  
		Last Modified: Sat, 27 Jan 2024 10:49:56 GMT  
		Size: 756.0 KB (756022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d0c55fb248a8de6fbe1845ad02fc8d39d0804498c007ec6ac45a3c870127825`  
		Last Modified: Sat, 27 Jan 2024 10:49:56 GMT  
		Size: 2.3 MB (2289369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c300a93aca89dc983e5fe318c49355f8cf6a4923d3c04bce1c6cb26223c17965`  
		Last Modified: Sat, 27 Jan 2024 10:49:56 GMT  
		Size: 2.3 MB (2288479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:199791e539e46e4ef2e67f528ebec831fdbc0db012613584fa316136a87bc4c9`  
		Last Modified: Sat, 27 Jan 2024 10:49:55 GMT  
		Size: 69.3 KB (69337 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:8b9fd893d3ca6ce7a084caabee33df1e3f2c5cffb106dffdddc833ac1da29316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62107389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79aa03c8f5de8c19e825d522a504672b7079f3247e4df65109f14d60b331fad1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 05 Jan 2024 21:27:24 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 05 Jan 2024 21:27:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.8","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.8?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_VERSION=3.12.12
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 05 Jan 2024 21:27:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 21:27:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.12","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.12?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 05 Jan 2024 21:27:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 05 Jan 2024 21:27:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 05 Jan 2024 21:27:24 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 21:27:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jan 2024 21:27:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 05 Jan 2024 21:27:24 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6851785cd78b9a7b68b35673a960d896b5d318e733303ed1a157dcdd5a1dbbfb`  
		Last Modified: Sun, 28 Jan 2024 15:40:02 GMT  
		Size: 32.9 MB (32919543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b59fd8fbe2e73f9494133db66ed1ecef7bdb6c8de47016796d65f9516abebe9`  
		Last Modified: Sun, 28 Jan 2024 15:40:02 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ae8fe9c2eeeccd526781f7549ffb388718cd5775a74b7821573b355587a2f9`  
		Last Modified: Sun, 28 Jan 2024 15:40:02 GMT  
		Size: 6.7 MB (6696966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32f60750bbec1a7ef9155fcb37317eeb49f811c57a6d225a5d0ba18f6528ba4`  
		Last Modified: Sun, 28 Jan 2024 15:40:02 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b53a5b3a5f9d6ba0c2cc308cb215a8bda573011e70b27f40e621a36c614a9f`  
		Last Modified: Sun, 28 Jan 2024 15:40:03 GMT  
		Size: 1.5 MB (1498801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d06e68658384e8ed34c62e3bf3b930e3fb82898b9d1c3b03237bfbe50f98542`  
		Last Modified: Sun, 28 Jan 2024 15:40:04 GMT  
		Size: 17.7 MB (17746910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdebd3da8b02909902e5a6e3a26b70ee70f0c8b3176c9e8b485975fce1d209`  
		Last Modified: Sun, 28 Jan 2024 15:40:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9261125a2c5bb497b01a42bd319bd3a97aa282658aec54b2aebd7d639f2e77`  
		Last Modified: Sun, 28 Jan 2024 15:40:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541c3a06dce9fd9c7c2c6ae4c8eede8195aad15f060827aa49f2d9030e3ac67`  
		Last Modified: Sun, 28 Jan 2024 15:40:04 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a28bf2cef11b5c8970218b2183bf6df2eeb7479dcd947e60cacea1837ac45d`  
		Last Modified: Sun, 28 Jan 2024 15:40:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1ace16834ddcd699e1194d3bc619658cbaef04668072fb1ee17e54b2d7361a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6755ec34bad28ad1141d08d87d70f5fecbc92be5804530240f4d97ec101adb7`

```dockerfile
```

-	Layers:
	-	`sha256:1418552a873bcc6b530c1f3b3c4c8812a55d0e967ded15bb9244ef4c57f2f5c0`  
		Last Modified: Sun, 28 Jan 2024 15:40:02 GMT  
		Size: 756.0 KB (755988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f911d8662740cce0a9283b44e7e022d22018aa1e7bcf7623bb15948bcf1530`  
		Last Modified: Sun, 28 Jan 2024 15:40:02 GMT  
		Size: 2.2 MB (2221404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98357f37c6efcdd59a4e5d694c33fb4263837e418350a20bb9a2fd6d0741e814`  
		Last Modified: Sun, 28 Jan 2024 15:40:02 GMT  
		Size: 2.2 MB (2220514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da27416ce119998e616038d0c9b571d0fe5ed150a44993ec748544ec1a30058`  
		Last Modified: Sun, 28 Jan 2024 15:40:02 GMT  
		Size: 69.3 KB (69277 bytes)  
		MIME: application/vnd.in-toto+json
